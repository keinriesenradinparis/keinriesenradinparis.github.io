---
title: Solidity Basics
date: 2025-08-02
last_modified_at: 2025-10-18
categories: 
  - "web"
# layout: page_light
---

<!-- # Solidity Basics -->

## Hack Solidity

> [!NOTE] 
> 这篇笔记跟着 Youtube 视频学习 [Solidity by examples](https://solidity-by-example.org/) 网站上一些基本的合约攻击（安全漏洞、防范方法）。

Source:
- Youtube [playlist](https://youtube.com/playlist?list=PLO5VPQH6OWdWsCgXJT9UuzgbC8SPvTRi5&si=FvNewFGwPBjNsAI-) of [Smart Contract Programmer](https://www.youtube.com/@smartcontractprogrammer).
- The **Hacks** part on the website [solidity-by-example](https://solidity-by-example.org/).

### Solidity 0.6
#### Reentrancy 

#### Arithmetic Overflow and Underflow

#### Forcefully Send Ether with selfdestruct

#### Accessing Private Data

Private state variables can still be read on the blockchain, since state variables (no matter public or private) are stored in a linear order of slots, computable by their respective types and byte-size.

#### Unsafe Delegate Call

#### Insecure Source of Randomness

#### Denial of Service

#### Phishing with `tx.origin`

#### Hiding Malicious Code

在一个合约里，声明一个变量`a`为类型`A`不代表调用函数`a.test()`时`a`使用的是`A`合约代码里函数`A.test()`的代码。这个声明只是告诉系统：`a`地址中可以调用的函数名和`A`的函数名两者的名称（或者说接口）应该是一致的。

因此，如果`a`已经在（你不一定晓得的）某一地址部署为`B`的实例，并且`B`含有函数`B.test()`，那么以类型`A`的名义调用`a`时调用的是`a`所在地址部署好的名为`test()`的函数。既然`a`是用`B`的代码部署的，而不是`A`的代码，那么`a.test()`调用的就是`B.text()`的代码。

实操上，你可能会需要调用一个合约`C`，它其中有一个变量为`a`，声明为类型`A`。但etherscan只显示`C`和`A`的代码给你看，也会告诉你`a`属于类型`A`。即使对方事先将`a`在别处部署为某个恶意合约`B`的实例，etherscan也只会告诉你`a`属于`A`类型，所以你下意识会觉得他们的代码是一样的。所以要小心检查部署合约`C`时已经提前部署好的所有合约地址（比如`a`），到它们相应的地址检查它们的代码（比如`a`的地址检查`a`部署时用的代码），而不是在合约`C`和`A`里检查代码（你不会检查出恶意代码的问题）。

#### Honeypot

这可以针对reentrancy attack：可以通过上一段所说的方式来将可以事先反击reentrancy attack的`Honeypot`合约部署在别的地址，然后在容易被reentrancy attack攻击的合同部署时将这个地址赋予`logger`（自定义日志`Logger`类型的变量）。这样上当者会天真的以为`logger`就是普通的日志类型`Logger`，但是实际上`logger.log()`的代码是`Honeypot`的代码，它会`revert`本次调用以来的所有的状态。

#### Front Running

抢到block的记录权力，然后通过观察现有的（未排序的）交易，将它们排序然后（在前面或后面）插入自己的交易来进行短期套利。

#### Block Timestamp Manipulation

系统的两个要求：
- 时间戳必须比上一个时间戳晚，
- 时间戳不能过于晚于上一个时间戳。

但在这两个条件下，时间戳对于本区块的验证者而言仍有很大的修改区间。

#### Signature Replay

可以通过将`nonce`（该合约地址累计交易次数）加入需要哈希的交易信息中来防止签名的重复使用。

然而对于那些用`create2`创建于同一地址的、含有`selfdestruct()`的合约，`nonce` 可以被重置，所以无法防止签名重用。

### Solidity 0.7
#### Contract With Zero Code Size

调用`constructor()`的过程中， 合约的`extcodesize` 为0。所以合约`extcodesize`等于0并不意味着合约里没有代码。

### Solidity 0.8

#### Read Only Reentrancy

In a Curve contract, the virtual price during removing liquidity might be higher than the virtual price before removing liquidity. 原因是remove liquidity的时候，函数会在尚未完全结束调用前就将ETH转给提款地址。所以我们可以利用这个漏洞，在`receive()`函数中植入恶意代码（转款的时候，remove liquidity的函数尚未结束调用）。

因此，如果想要攻击一个依赖于virtual price的合约时，我们可以在`receive()`里调用这个合约，以使得在remove liquidity时转款时自然而然调用`receive()`使得其中的代码来攻击它。

#### Tornado Cash Hack - How to Deploy Different Contracts At the Same Address | DeFi

攻击者提供位于地址`0xABC`的合约提案`a`，Tornado治理组织认为合约没问题，一致通过。然后攻击者删除位于地址`0xABC`的合约`a`，在同一地址`0xABC`部署恶意合约`b`，然后提议执行提案`a`，于是治理组织通过`delegatecall`（它可以获取很高的权限！）来调用地址`0xABC`的合约，殊不知此时的代码已被换成了`b`的恶意代码。

如何在同一地址部署不同的合约？
首先，用`create`部署合约的合约地址是如下计算的：
```
/*
contract address = last 20 bytes of sha3(rlp_encode(sender, nonce))
*/

// 假设我们要部署一个Deployer合约
address addr = address(new Deployer());
```
其次，用`create2`部署合约的合约地址是利用给定盐值`salt`进行如下计算的：
```solidity
// 假设我们要部署一个Deployer合约

bytes32 salt = keccak256(abi.encode(uint256(123))); // 设定盐值
address addr = address(new Deployer{salt: salt}()); // create2需要传入盐值参数{salt: salt}
```

于是总的攻击是这样的：
- 让`DeployerDeployer`用`create2`部署一个傀儡合约`Deployer`，后者用`create`部署`Proposal`。
- 这时`Deployer`的`nonce`从0增加为1，所以不能立马让`Deployer`用`create`部署一个新的`Proposal`（这样地址会变）。
- 用`create2`重新部署`Deployer`于同一地址，因为这个重置过程，`Deployer`的`nonce`又变成了0，这时候再让`Deployer`用`create`部署一个新的`Proposal`（根据`create`的计算方法，既然`nonce`没变，所以依然部署在以前的地址）。
流程步骤重述如下：
```solidity
/*
Called by Alice
0. Deploy DAO

Called by Attacker
1. Deploy DeployerDeployer
2. Call DeployerDeployer.deploy()
3. Call Deployer.deployProposal()

Called by Alice
4. Get DAO approval of Proposal

Called by Attacker
5. Delete Proposal and Deployer
6. Re-deploy Deployer
7. Call Deployer.deployAttack()
8. Call DAO.execute
9. Check DAO.owner is attacker's address


DAO -- approved --> Proposal
Delete Proposal and Deployer
DeployerDeployer -- create2 --> Deployer -- create --> Proposal
DeployerDeployer -- create2 --> Deployer -- create --> Attack
*/
```

#### Vault inflation attack:

Vault 计算新 mint 的 token（或者说计算新增的 share）的公式是会取整的，这样子就可以（通过 front running）让别的用户存钱的时候的 share（小于 1）取整变为 0。具体操作是：
- 攻击者通过突然存入大量的钱让每份 share 变多（变为 $P_1$）。
- 这个时候别的用户存钱金额$P_2$要是小于每份share的价值（$P_2 < P_1$），那么他新增的 share 数量为 $P_2/P_1$ 取整，所以为 0。因此这个 $P_2$ 平摊到现有的每个 share 里。
- 然后攻击者立马取出刚存入的大量钱，分走了平摊到的 $P_2$ 的份额。

#### WETH permit

`ERC20Bank` 合约的 `depositWithPermit` 函数会调用 `token.permit()` 函数来检查使用 token 的许可然后再给 spender 充值。通常来说这个函数都是存在的，如果没有 permit 的话会直接 revert。然而，如果某个 token 没有相应的函数（比如说 WETH），那么会调用 `token.fallback()` 函数并且不会 revert、继续执行给 spender 充值——这就是一个可被攻击的漏洞。

#### 63/64 gas rule 

以太坊的规则：External calls receive max $63 / 64$ of gas left in current contract, and $1 / 64$ gas is kept in the current contract (for potential usage afterwards).

```solidity
/*
# 63 / 64 gas rule
g0 = call to gasleft() somewhere in A
g1 = call to gasleft() somewhere in B
g* = Actual gas left immediately before call to B

  g*    63/64 g*
A |---->| B
|         |
g0        g1
*/
```

The actual amount of gas used between $g_0$ and $g_1$ is $dg = g_0 - g^* + \frac{63}{64} g^* - g_1 = g_0 - g_1 - \frac{1}{64} g^*$, which is less than $g_0 - g_1$.

如果合同 B 包含返还多余的 gas 的机制，可能会被攻击：例如，如果合同 B 代码里写的是 refund $g_0 - g_1$ 给调用合同 A 的地址，那么攻击者可以反复调用合同 A 并且提高 $g_0$（从而提高 $g^*$）来从合同 B 中抽取 gas。

