---
title: Tutorat AMC 8
date: 2025-09-15
last_modified_at: 2025-09-15
---

# 21 sept 2025

## 三角形

凸 $n$ 边形内角和等于 $(n-2) \times 180^\circ$。如何通过外角和 $360^\circ$ 推导内角和公式？

### 三角形面积公式 $S = \frac{1}{2} ah$

**割补法（découpage et recomposage）**：回顾如何利用长方形面积公式证明三角形面积公式。

> [!NOTE] AMC 8 (2015)
> Un triangle dont les sommets sont $A = (1,3)$, $B = (5,1)$ et $C = (4,4)$ est tracé sur une grille de $6\times5$. Quelle fraction de la grille est recouverte par ce triangle ?
> 
> ![|200](attachments/Pasted%20image%2020250915232141.png)

> [!NOTE] AMC 8 (2018)
> La figure à douze côtés ci-contre a été tracée sur du papier quadrillé de $1~\text{cm} \times 1~\text{cm}$. Quelle est l'aire de cette figure en $\text{cm}^2$ ?
> 
> ![|200](attachments/Pasted%20image%2020250915231852.png)

> [!NOTE] AMC 8 (2011)
> Chacun des quatre grands carrés congruents suivants est subdivisé en combinaisons de triangles ou de rectangles congruents et est partiellement en gras. Quel pourcentage de la surface totale est partiellement en gras ?
> 
> ![|200](attachments/Pasted%20image%2020250916000023.png)

> [!NOTE] AMC 8 (2024)
> Quatre carrés de côtés $4$, $7$, $9$ et $10$ sont disposés par ordre croissant de taille de sorte que leurs bords gauche et bas soient alignés. Les carrés alternent en couleur blanc-gris-blanc-gris, respectivement, comme montré sur la figure. Quelle est l'aire de la région grise visible en unités de surface ?
> 
> ![|200](attachments/Pasted%20image%2020250915234858.png)

> [!NOTE] AMC 8 (2024)
> Les coordonnées du triangle $\triangle ABC$ sont $A(5,7)$, $B(11,7)$, $C(3,y)$, avec $y>7$. L'aire du triangle $\triangle ABC$ est $12$. Quelle est la valeur de $y$ ?
> 
> ![|200](attachments/Pasted%20image%2020250915235007.png)

### 直角边中点和直角相连，长度为直角边的一半

> [!NOTE] AMC 8 (2014)
> Dans le triangle $\triangle ABC$, le point $D$ est situé sur le côté $\overline{AC}$ de telle sorte que $BD = DC$ et que l'angle $\angle BCD$ mesure $70^\circ$. Quelle est la mesure en degrés de l'angle $\angle ADB$ ?
> 
> ![|300](attachments/Pasted%20image%2020250915235902.png)

### 勾股定理 $c^2 = a^2 + b^2$ (théorème de Pythagore)

逆定理也成立：如果一个三角形的三边满足勾股公式，那么它是直角三角形，直角边为 $c$。

Triplets pythagoriciens importants :  
- $3, 4, 5$ ; 
- $5, 12, 13$ ; 
- $7, 24, 25$ ;
- $8, 15, 17$ ;
- $9, 40, 41$ ; 
- $20, 21, 29$.
  
> [!NOTE] AMC 8 (2015)
> Dans le triangle $\bigtriangleup ABC$, on a $AB = BC = 29$ et $AC = 42$.  
> Quelle est l'aire du triangle $\bigtriangleup ABC$ ?

> [!NOTE] AMC 8 (1998)
> Quel est le rapport de l'aire du carré ombré sur l'aire du grand carré ?  
> 
> ![|200](attachments/Pasted%20image%2020250916000446.png)

### 特殊边长的三角形

三边长比例为 $13 : 14 : 15$：把边长 $14$ 的边拆成 $5$ 和 $9$ 两段得到两个直角三角形，公共边长为 $12$。

### 相似三角形 (théorème de Thalès)

平行线 $\implies$ 等比例。

逆定理也成立：等比例 $\implies$ 平行线（相似三角形）。

### 特殊角的三角形

等边三角形：三边长相等。

直角三角形：
- $30^\circ$：三边长比例为 $1 : \sqrt{3} : 2$。
- $45^\circ$：三边长比例为 $1 : 1 : \sqrt{2}$（刚好是正方形沿斜对角切一半）。
- $60^\circ$：同 $30^\circ$，三边长比例为 $1 : \sqrt{3} : 2$。

### 三角形任意两边之和大于第三边 $a + b > c$


> [!NOTE] AMC 8 (2015)
> Quel est le plus petit nombre entier supérieur au périmètre de tout triangle ayant un côté de longueur $5$ et un côté de longueur $19$ ?

### 运动坐标图

路程-时间：速度为斜率
速度-时间：路程为面积

> [!NOTE] AMC 8 (2022)
> Par une journée ensoleillée, Ling décida de faire une randonnée en montagne. Elle quitta sa maison à $8~\text{h}$, conduisit à une vitesse constante de $45$ miles par heure, et arriva au sentier de randonnée à $10~\text{h}$. Après avoir randonné pendant $3$ heures, Ling rentra chez elle en voiture à une vitesse constante de $60$ miles par heure. Lequel des graphiques suivants illustre le mieux la distance entre la voiture de Ling et sa maison au cours de son trajet ?
> 
> ![|400](attachments/Pasted%20image%2020250915235303.png)

## 圆

半径 $r$
直径 $d = 2r$
周长 $C = 2 \pi r = \pi d$
面积 $S = \pi r^2$

弧度占 $360^\circ$ 的比例 = 扇形周长占圆周长的比例 = 扇形面积占圆面积的比例
