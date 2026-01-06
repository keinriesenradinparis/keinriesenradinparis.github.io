---
title: Tutorat-05
date: 2025-10-05
last_modified_at: 2025-11-16
---

# 12 et 19 oct 2025

## Somme et série

### Somme et série téléscopiques

Il faut savoir compter le nombre de termes !

### Somme et série d'une suite arithmétique

### Somme et série d'une suite géométrique (plus difficile, donc omise)

### Exercices

Exercices sur la somme (et la série) :

| Année | Nº question | Point clé                      |
| ----- | ----------- | ------------------------------ |
| 2019  | 17          | téléscopique                   |
| 2018  | 2           | téléscopique                   |
| 2017  | 5           | somme d'une suite arithmétique |
| 2016  | 8           | téléscopique                   |
| 2015  | 13          | somme d'une suite arithmétique |
| 2015  | 18          | suite arithmétique             |
| 2013  | 3           | téléscopique                   |
| 2013  | 17          | somme d'une suite arithmétique |

## Combinatoire

**Arrangement** 排列 : choisir $m$ parmi $n$ - en tenant compte de l'ordre.

**Combinaison** 组合 : choisir $m$ parmi $n$ - en étant indifférent de l'ordre.

Applications :
- Remettre $n$ objets `identiques` dans $m$ boîtes, tel que aucune boîte ne soit vide : **méthode des barres** 隔板法.
- Remettre $n$ objets `identiques` dans $m$ boîtes : rajouter un objet dans chaque boîte, puis appliquer la 隔板法。
- Remettre $n$ objets `distincts` dans $m$ boîtes.

### Exercices

#### 10月12日作业：

等差数列求和：
1. 求和：3+7+11+15+19+23
2. A4纸上还有一道剩下的习题

排列组合问题：知道怎么算arrangement（排列）和combinaison（组合）的种数。
并考虑以下问题（只需要列出表达式）：
3. 5个人坐5张椅子有几种坐法？5个人坐3张椅子呢？
4. 一副扑克有54张牌，洗牌结果总共有几种？
5. 一个人连续投五次硬币，总共有三次是数字朝上的可能性有几种？
6. 两个人Alice和Bob坐在5张椅子上，总共有几种坐法？其中Alice坐在Bob左边的可能性有几种？

#### 10月19日作业：

**Méthode du « complémentaire » (compter le contraire).**

Exercice 1

On forme des nombres à trois chiffres (avec les chiffres 0, 1, 2, 3,… , 9).

1. Combien de nombres à trois chiffres peut-on former au total ? (N.B. Ils ne commencent pas avec le zéro, et peuvent avoir des chiffres répétés.)
2. Combien de ces nombres ne contiennent pas le “7” ?

Exercice 2

On choisit 3 élèves parmi A, B, C, D, E, pour former un groupe. 

0. C’est une question de combinaison ou d’arrangement ?
1. Combien de façons de former un tel groupe ?
2. Si A et B ne peuvent pas être choisis ensemble, combien de façons reste-t-il ?

Exercice 3

On choisit 3 lettres parmi A, B, C, D, E, puis on les met dans un ordre pour former un mot (peut-être n’existant pas dans le dictionnaire).

0. C’est une question de combinaison ou d’arrangement ?
1. Combien de mots peut-on former ?
2. Combien de mots ne contiennent pas A et B à la fois ?

**Exercice 4 (méthode de barres)**

On distribue 7 pommes à trois élèves, chacun recevant au moins une pomme. Alors il y a combien de moyennes de distribution ?

# 26 oct 2025 (relâche vacances)

Relâche vacances de toussaints.

# 2 nov 2025

## Complément sur la permutation/combinatoire

### Exercices issus d'ACM 8

| Année | Nº question | Point clé                                                   |
| ----- | ----------- | ----------------------------------------------------------- |
| 2020  | 17          | combinaison + factorisation                                 |
| 2020  | 21          | combinaison (un peu difficile), ou le triangle de Yang Hui  |
| 2020  | 23          | combinaison avec certaines conditions                       |

> [!NOTE]
> Le triangle de Yang Hui (appelé aussi le triangle de Pascal) : c'est une méthode graphique et **inductive** pour compter le nombre de **chemins menant d'un point à un autre point sur un graphe**.
> 
> Par exemple, on peut se demander :
> - Combien de chemins pour aller du bas gauche au haut droite d'un carré $5 \times 5$ tout en évitant une partie de sommets de ce carré ?
> - Combien de déroulements des scores dans un jeu de pingpong ?
> - Combien de façons de monter un escalier de 6 marches, si dans chaque étape on monte 1, 2 ou 3 marches ? （Cela fait $1+7+10+5+1 = 24$ façons comme on le lit bien sur le dessin.)

### 11月2日补充作业：

**Méthode des barres 隔板法：**

**Exercice 1**

4 personnes Alice, Bernard, Cécile, Dorian partagent 10 bonbons.

1. Il y a combien de façons pour leur distribuent les bonbons ?
2. Si chacun demande au moins 1 bonbon, alors il en reste combien de façons ?
3. Si Alice, Bernard et Cécile demandent au moins 2 bonbons, mais Dorian demande au moins 1 bonbon, alors il en reste combien de façons ?
4. Si tout le monde demande au moins 2 bonbons, alors il en reste combien de façons ?
5. (plus dur) Si Alice n'a pas de préférence, Bernard et Cécile demande au moins 1 bonbon, Dorian demande au moins 2 bonbons, alors il y a combien de façon de distribution ?

**Exercice 2**

100 élèves votent pour choisir un représentant parmi 3 candidats. Chacun vote une seule fois.

(1) Si les papiers de vote de chaque élève sont tous distincts (par exemple s'il sont marqués par un nombre), alors il y a combien de possibilités de résultat dans les boîtes de vote ? (Non seulement les nombres de votes obtenus comptent.)

Supposons maintenant que les votes sont indiscernables, alors seulement les nombres de votes obtenues compte.

(2) Il y a combien de possibilités de résultat ?
- Indice : réfléchir pourquoi c'est comme avoir trois nombres $a$, $b$, $c$ associés aux trois boîtes tels que $a + b + c = 100$.

(3) Il y a combien de possibilités de résultat où (au moins) 2 candidats ont obtenu le même nombres de votes ?

**Méthode inductive 递推法**：

甲乙比赛，5 局 3 胜，有几种比分变化的情况？

方法一（稍难）：
- 提示：画个 $3 \times 3$ 格子，左下角格点对应比分 $0:0$，用递推的方法算从左下角走到各个（比分对应的）格点的方法数。
- 注意：只要其中一人比分到达 3，游戏就结束，所以不可能出现比分 $3:3$ 的情况，也不可能从比分 $1:3$ 变为 $2:3$。

方法二：
- 提示：另画一个$3 \times 2$ 格子，用递推的方法计算甲获胜的比分变化情况，然后乘以 $2$（为什么可以这么做？）。

比较两种方法得到的结果。


# 9 nov 2025

## Arrangement circulaire

Il y a $n$ personnes qui s'assoient autour d'une table ronde.
1. Il y a combien de façons ?
2. Si seulement l'ordre compte, alors il y a combien de façons ?

## Probabilité/comptage sous contrainte

| Année | Nº question | Point clé               |
| ----- | ----------- | ----------------------- |
| 2018  | 11          | compter sous contrainte |

> [!NOTE]
> Par définition :
> $\text{la chance} = \frac{\text{possibilité}}{\text{nombre de choix total}}$.

**AMC 8**

On lance une pièce équilibrée trois fois. Quelle est la probabilité d’obtenir au moins deux faces consécutives ?

**AMC 8**

On lance un dé équilibré à 6 faces deux fois. Quelle est la probabilité que le premier nombre obtenu soit strictement plus grand que le deuxième ?

**Exercice :**

甲乙比赛，5 局 3 胜，有几种比分变化的情况？

如果甲能获得两分，那么就能获得奖金。那么甲获得奖金的概率是多少？

### 11月9日作业

**Exercice 1**

Il y a $5$ personnes qui s'assoient autour d'une table ronde.
1. Il y a combien de façons ?
2. Si seulement l'ordre compte, alors il y a combien de façons ?

<!-- 
$5!$
$5!/5$
-->


**Exercice 2**

Il y a $26$ petites pièces en lettres, à en choisir $6$ pour former un bracelet de longueur $6$.
- On peut former combien de bracelets ? (Cela correspond à la deuxième question précédente.)
- Si les lettres A et B ne peuvent pas être mis côte à côte, alors combien de bracelets peut-on former ?

<!-- 
$26 \times 25 \times 24 \times 23 \times 22 \times 21 / 6$
$26 \times 25 \times 24 \times 23 \times 22 \times 21 / 6 - 2 \times 24 \times 23 \times 22 \times 21$
--> 

**Exercice 3 (AMC 8)**

Une boîte contient cinq cartes numérotées 1, 2, 3, 4 et 5. On tire au hasard trois cartes sans remise. Quelle est la probabilité que 4 soit la plus grande valeur parmi les cartes tirées ?

<!-- 
$\frac{3}{10}$
--> 

**Exercice 4 (AMC 8-2018-Q11)**

Alice, Bob et 4 amis s'assoient sur les 6 sièges dans la disposition suivante :

|     |     |     |
| --- | --- | --- |
|     |     |     |

Quelle la chance où Alice et Bob sont dans le même rang ou dans le même colonne ?

<!-- 
$\frac{6 \times 3 \times 4!}{6!} = \frac{18}{30} = \frac{3}{5}$
--> 

Et adjacent ?

<!-- 
$\frac{2 \times 7 \times 4!}{6!}$
--> 

**Exercice 5**

On lance un dé équilibré à 6 faces deux fois.
- On calcule leur somme. Quelle est la probabilité de chaque résultat obtenu ?
- On calcule leur différence. Quelle est la probabilité de chaque résultat obtenu ?

<!-- 
| Somme | Proba (/36) |
| ----- | ----------- |
| 2     | 1           |
| 3     | 2           |
| 4     | 3           |
| 5     | 4           |
| 6     | 5           |
| 7     | 6           |
| 8     | 5           |
| 9     | 4           |
| 10    | 3           |
| 11    | 2           |
| 12    | 1           |

| Diff | Proba (/36) |
| ---- | ----------- |
| 0    | 6           |
| 1    | 10          |
| 2    | 8           |
| 3    | 6           |
| 4    | 4           |
| 5    | 2           |
--> 





