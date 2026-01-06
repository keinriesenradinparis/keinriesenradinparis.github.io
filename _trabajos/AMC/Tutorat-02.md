---
title: Tutorat AMC 8
date: 2025-09-13
last_modified_at: 2025-09-14
---

# 14 sept 2025

## 比例和百分比

### 比例是用来表示`相对`数量的

**Exemples d'usage :**
- 你的身高是我的两倍。
- 你的身高是我的二分之一。
- 成本占收入的百分之四十。

**Notion :** 
`fraction = ratio = rapport = proportion ≈ fréquence ≈ pourcentage ≈ taux`,
tout cela pour exprimer une quantité `relative` (pour exprimer une proportion dans un total, ou pour exprimer la grandeur relative).

**Expressions mathématiques：**
$$
a/b = \frac{a}{b} = a : b = \frac{c}{100} = c \%.
$$

比例定义等式：
$$
\text{rapport} = \frac{\text{quantité}~A}{\text{quantité}~B}
$$
知道其中两者就能求出第三个数。

###  分数的运算

加法：先通分再做加减法：
$$
\frac{a}{b} + \frac{c}{d} = \frac{ad + cb}{bd}.
$$

乘法：分别对分子和分母做乘法：
$$
\frac{a}{b} \cdot \frac{c}{d} = \frac{ac}{bd}.
$$

### Exemples

> [!NOTE] Example
> Il y a 600 élèves au collège. Il y en a un tiers en 6ème.
> 那么 6e 有多少人？

> [!NOTE] Example
> Dans un bocal il y a $n$ balles, dont 15% sont rouges. Si l'on compte et trouve 3 balles en total, alors combien vaut $n$ ?

> [!NOTE] Example 
> Il y a 500 élèves au collège. Il y en a une moitié en 6ème, un $1/4$ en 5ème, un $1/5$ en 4ème, et les autres sont en 3ème.
> 那么每个年级有多少人？
> > Hint:
> > 250, 125, 100, 25.

**相对比例可以做乘法：**
$$
\text{rapport}~\alpha = \frac{\text{Grande}}{\text{Total}}, \quad \text{rapport}~\beta = \frac{\text{Grande verte}}{\text{Grande}} \implies \alpha \beta = \frac{\text{Grande verte}}{\text{Total}}.
$$

> [!NOTE] Example 
> Sohil a un bocal avec beaucoup de billes. 20 % d'entre elles sont petites, 40 % sont moyennes et 40 % sont grandes. Pour chaque taille, 30 % des billes sont rouges, 20 % bleues, 40 % vertes et 10 % jaunes. La moitié des billes jaunes de grande taille et des billes vertes de petite taille ont un motif spécial. Quelle est la proportion (en pourcentage) de billes ayant un motif spécial parmi l'ensemble des billes ?
> > Hint:
> > 列表格，知道要求什么量。
> > $1/2 \times 10\% \times 40\% + 1/2 \times 40\% \times 20\% = 2\% + 4\% = 6\%$.

**抽样问题：**
- 残次品检验。
- 生态学的例子：标记重补法（capture-marquage-recapture）来统计物种数量。

> [!NOTE] Example 
> La société *Calculatrice Dix Doigts* vérifie périodiquement au hasard des calculatrices avant d'expédier les caisses aux clients. Mercredi, 12 calculatrices ont été testées dans chacune des 64 caisses contenant 144 calculatrices. Deux des calculatrices testées se sont révélées défectueuses. Sur la base de ce taux de défaut, combien de calculatrices au total sont susceptibles d'être défectueuses ?
> > Hint:
> > $2/(12 \times 64) \times (144 \times 64) = 24$.

**比例换算的问题：**

> [!NOTE] Example 
> $2a = 3b = 5c \implies a : b : c = ?$
> > Hint:
> > 
> > 方法一：通分：
> > $a : b : c = 1/2 : 1/3 : 1/5 = 15 : 10 : 6$.
> >
> > 方法二：特殊值方法（因为比例是相对大小，每个数可以同时翻倍而不改变比例）：假设 $2a = 3b = 5c = 30$ （或者 $2, 3, 5$ 的其他公倍数），然后做计算。

> [!NOTE] Example 
> Le rapport de $w$ à $x$ est $4 : 3$, le rapport de $y$ à $z$ est $3 : 2$, et le rapport de $z$ à $x$ est $1 : 6$. Quel est le rapport de $w$ à $y$ ?
> > Hint:
> > $w / y = w / x \cdot x / z \cdot z / y = 4/3 \times 6/1 \times 2/3 = 16/3$.

### Exercices

**Exercice simple**
Supposons que $15\%$ de $x$ soit égal à $20 \%$ de $y$. Quel pourcentage de $x$ représente $y$ ?

**AMC 8 - Problem 11 (variation)**
Le sommet d'un arbre est à $15$ mètres plus haut que celui d'un autre arbre. Les hauteurs des deux arbres sont dans le rapport $2:5$. En mètres, quelle est la hauteur de l'arbre le plus grand ?

**AMC 8 - Problem 17**
Le diagramme montre un octogone constitué de $10$ carrés unitaires. La partie située sous $\overline{PQ}$ est un carré unitaire et un triangle de base $5$. Si $\overline{PQ}$ divise l'aire de l'octogone en deux parties égales, quel est le rapport $\frac{XQ}{QY}$ ?

![|400](attachments/Pasted%20image%2020250906221248.png)
$$\textbf{(A)}\ \frac 25 \qquad \textbf{(B)}\ \frac 12 \qquad \textbf{(C)}\ \frac 35 \qquad \textbf{(D)}\ \frac 23 \qquad \textbf{(E)}\ \frac 34$$

> [!TIP] Hint
> 方法：分步考虑：
> - 面积的一半是多少？
> - **割补法**求斜线下方的面积和 $YQ$ 长度的关系？
> - 求出 $YQ$ 的长度。
> - 求出比例 $\frac{XQ}{QY}$。

**AMC 8 - Problem 20**
Dans une pièce, $2/5$ des personnes portent des gants et $3/4$ des personnes portent des chapeaux. Quel est le nombre minimum de personnes dans la pièce portant à la fois un chapeau et un gant ?
$$\textbf{(A)}\ 3 \qquad\textbf{(B)}\ 5\qquad\textbf{(C)}\ 8\qquad\textbf{(D)}\ 15\qquad\textbf{(E)}\ 20$$ 

> [!TIP] Hint
> 房间里的人数被 $5$ 整除，被 $4$ 整除。
> 房间里有 $n$ 个人，$a$ 个人戴手套，$b$ 个人戴帽子。

**思考题**
Steph a marqué $15$ paniers sur $20$ tentatives lors de la première mi-temps, et $10$ paniers sur $10$ tentatives lors de la deuxième mi-temps. Candace a tenté $12$ tirs lors de la première mi-temps et $18$ tirs lors de la deuxième mi-temps. Dans chaque mi-temps, Steph a obtenu un pourcentage de réussite plus élevé que Candace. Étonnamment, elles ont terminé avec le même pourcentage global de paniers réussis. Combien de paniers de plus Candace a-t-elle marqué dans la deuxième mi-temps par rapport à la première mi-temps ?

|  nom  |   1er mi-temps  | 2e mi-temps |
| --- | --- | --- |
|  Steph   |  15/20   | 10/10 |
| Candace | ?/12 | ?/18 |

> [!TIP] Hint
> 把问号处的所有可能性都写出来。
> 然后观察一下，看看有没有想法。
> 答案：8/12, 17/18.

## 行程问题

### 比例=速度

`taux = vitesse` :  elle mesure la quantité de travail réalisé par unité de temps.

La vitesse pourrait désigner :
- la distance traversée par heure = km/h,
- l'angle tourné par seconde d'une machine (e.g. d'une grande roue),
- le nombre de problèmes résolus par minute,
- le nombre de voitures passant un carrefour par minute.

### Exemples

> [!NOTE] Example 
> Joe doit se rendre à son bureau, situé à $40$ km. S'il conduit à $60$ km par heure, combien de minutes lui faudra-t-il pour arriver au travail ?

> [!NOTE] Example 
> Bob va chez Alice à vélo à $15$ km/h, et le chien de Bob court sans arrêt en avant et en arrière à une vitesse de $5$ km/h. Le chien court jusqu'à chez Alice, puis revient vers Bob ; lorsqu'il le rencontre, il repart vers Alice, et ainsi de suite. Quelle distance le chien a-t-il parcourue ?

**AMC - Problem 8**
Alors qu'Emily fait du vélo sur une longue route droite, elle aperçoit Emerson en train de patiner dans la **même** direction à $\frac{1}{2}$ km devant elle. Après l'avoir dépassé, elle peut le voir dans son rétroviseur jusqu'à ce qu'il se retrouve à $\frac{1}{2}$ km derrière elle. Emily roule à une vitesse constante de **$12$ km par heure**, et Emerson patine à une vitesse constante de **$8$ km par heure**. Pendant combien de **minutes** Emily peut-elle voir Emerson ?
$$\textbf{(A)}\ 6 \qquad\textbf{(B)}\ 8\qquad\textbf{(C)}\ 12\qquad\textbf{(D)}\ 15\qquad\textbf{(E)}\ 16$$

> [!TIP] Question
> 单位换算：把下面时间换算成分钟：
> - $1$ 小时，$0.5$ 小时，$2/3$ 小时，$1/3$ 小时，$1/4$ 小时，$2/5$ 小时，$1/6$ 小时。

**Solution par vitesse relative :**
因为是**同方向**行走，所以：
- Emily 和 Emerson 靠近到相遇花了 $1/2 \div (12 - 8) = 1/8$ 小时。
- Emily 和 Emerson 相遇到远离花了 $1/2 \div (12 - 8) = 1/8$ 小时。
- 总共 $1/8 + 1/8 = 1/4$ 小时。
- 换算成多少分钟？

**Solution par équation :**
假设用了时间 $t$ 赶上了 $1/2$ km。列方程并解方程：
$$
12t = 8t + 1/2 \implies t = ?
$$

### Exercice

**两人面对面运动，速度相加**
上面 Emily 和 Emerson 的问题，两者**反方向**运动的话，总时间应该是多少？

**两者协作，速度相加**
Alex, en utilisant la méthode de substitution ou d'élimination, peut résoudre $20$ équations à deux variables en $10$ minutes. Bob, qui utilise la méthode du produit diagonal, peut résoudre $20$ équations à deux variables en $2$ minutes. Combien de temps leur faudra-t-il pour résoudre $60$ équations à deux variables en travaillant ensemble ?

> [!TIP] Hint
> $60/(20/10 + 20/2) = 5$.

> [!TIP] Question
> 列方程怎么解：
> $20/10 \times t + 20/2 \times t = 60 \implies t = ?$

