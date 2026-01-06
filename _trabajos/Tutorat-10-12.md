---
title: Tutorat-05
date: 2025-11-16
last_modified_at: 2025-11-16
---
# 16, 30 nov, 7 déc 2025

## Exercices supplémentaires pour réviser

### ... sur le comptage

**Exercice 1 (AMC 8)**

Il y a combien de nombres à 4 chiffres distincts ?

**Exercice 2 (AMC 8)**

Le photographe veut prendre une photo de 2 garçons et 3 filles. On veut que les deux extrémités soient des garçons. Il y a combien de photos qu'il peut faire ?

**Exercice 3 (AMC 8)**

Élise a 2 livres en arabe, 3 livres en allemand, 4 livres en espagnol à remettre sur une étagère. Il y a combien de façon de les ranger (linéairement) tels que les livres en arabes sont tous ensemble, ainsi que les livres en espagnol sont tous ensemble ?

**Exercice 4 (AMC 8-2020)**

Combien d’entiers compris entre 2020 et 2400 ont quatre chiffres distincts disposés dans l’ordre (strictement) croissant ?
(Par exemple, 2347 en est un.)

**Exercice 5 (AMC 8)**

Combien de façons peut-on arranger les lettres du mot BEEKEEPER de sorte que deux E ou plus ne se trouvent pas côte à côte ?

**Exercice 6 (AMC 8-2017)**

Peter, Emma et Kyler ont joué aux échecs entre eux. Peter a gagné 4 parties et en a perdu 2. Emma a gagné 3 parties et en a perdu 3. Si Kyler a perdu 3 parties, combien de parties a-t-il gagnées ?

<!-- 
$1$
--> 

**Exercice 7 (AMC 8-2008)** 

Il y a combien de $n$ tel que $n/3$ et $3n$ soient tous les deux à trois chiffres ?

<!-- 
$100 \times 3, \dots, 111 \times 3$
--> 

### ...sur la probabilité

> [!NOTE]
> La fréquence, le rapport, le pourcentage, ce sont des concepts similaires lorsqu'on parle de la probabilité, notamment quand on parle d'un échantillonage.
> 
> Imaginons que le responsable d'une usine de chaussures voudrait savoir combien de chaussures parmi les 10,000,000 chaussures fabriquées peuvent passer un certain test. Cela revient au même de connaître **le taux de réussite** pour ce test. C'est le rapport
> $$
> \frac{\text{le nombre de chaussures qui ont réussi}}{\text{le nombre total des chassures}}.
> $$
> Ce rapport reflète aussi **la chance ou la probabilité de réussite** pour chaque chaussure individuelle, si on en choisit une **au hasard**.
>
> <!-- Idéalement, ce n'est pas la peine de faire passer toutes les chaussures pour connaître ce rapport. Par exemple, on peut choisir au hasard 1,000 chaussures pour tester. Si 30 chaussures passent le test, alors on peut dire que la probabilité de réussite est environ $3\%$. C'est la méthode d'**échantillonnage**.--> 

**Exercice 8 (AMC 8-2018)**

Sur une plage, 50 personnes portent des lunettes de soleil et 35 personnes portent des casquettes. Certaines portent à la fois des lunettes de soleil et des casquettes. Si l’on choisit au hasard une personne portant une casquette, la probabilité qu’elle porte aussi des lunettes de soleil est de 0.4.

1. Si, au contraire, une personne portant des lunettes de soleil est choisie au hasard, quelle est la probabilité que cette personne porte également une casquette ?
2. S'il y a au total 100 personnes sur la plage, quelle est la probabilité qu'une personne choisie au hasard ne porte ni lunettes de soleil ni casquette ?

<!-- 
$14/50$
$29/100$
--> 

> [!NOTE]
> Dessine le **diagramme de Venn**.

**Exercice 8 (AMC 8-2016)**

On choisit au hasard deux nombres différents dans l'ensemble $\{-2, -1, 0, 3, 4, 5\}$ et on les multiplie. Quelle est la probabilité que le produit soit égal à 0 ?

<!-- 
$1/3$
--> 

---

## Théorie des nombres

### Premiers v.s. nombres composés

> [!NOTE]
> Un nombre premier = nombre $p$ qui a seulement et exactement deux facteurs : $1$ et $p$.
> Un nombre composé = nombre $n$ qui a d'autres facteurs que $1$ et $n$.
> 
> En particulier $1$ n'est pas un nombre premier, ni un nombre composé.
> 
> Les premiers nombres premiers : $2, 3, 5, 7, 11, 13, 17, 19, 23, 29$, etc.

> [!TIP]
> Le premier $2$ est pair, les autres premiers sont impairs. Cette parité est utile !

> [!TIP]
> Pour vérifier qu'un entier $n$ est un premier, il suffit de vérifier $p \nmid n$ pour tous les premiers $p \leq \sqrt{n}$. 

**Exercice 1**

Déterminer si les nombres suivants sont premiers :
- $85$
- $87$
- $91$
- $97$
- $109$

**Exercice 2 (AMC 8-2015)**

La somme des deux nombres premiers fait $85$. Que vaut leur produit ?

(Indication : parité.)

**Exercice 3 (AMC 8)**

Trois membres de l’équipe féminine de softball du collège Euclid ont eu la conversation suivante.  
- **Ashley :** Je viens de réaliser que nos numéros de maillot sont tous des nombres premiers à deux chiffres.  
- **Brittany :** Et la somme de vos deux numéros de maillot est la date de mon anniversaire plus tôt ce mois-ci.  
- **Caitlin :** C’est drôle. La somme de vos deux numéros de maillot est la date de mon anniversaire plus tard ce mois-ci.  
- **Ashley :** Et la somme de vos deux numéros de maillot est la date d’aujourd’hui.  
Quel numéro porte Caitlin ?

(Indication : commencer par énumérer les nombres premiers à deux chiffres $11, 13, 17, 19, 23, 29$, etc.)

### Critères de divisibilité

> [!NOTE]
> - Divisibilité par $1$ : triviale, toujours vraie.
> 
> - Divisibilité par $2$ $\iff$ $2$ divise **le dernier chiffre** (le chiffre des unités).
> 
> - Divisibilité par $3$ $\iff$ $3$ divise **la somme de tous les chiffres**. Par exemple, pour $abc$, il faut $3 \mid a + b + c$.
> 
> - Divisibilité par $4$ $\iff$ $4$ divise **les deux derniers chiffres**. Par exemple, pour $abcd$, il faut regarder $cd$.
> 
> - Divisibilité par $5$ $\iff$ $5$ divise **le dernier chiffre** $\iff$ le dernier chiffre est $0$ ou $5$.
> 
> - Divisibilité par $6$ $\iff$ divisibilité par $2$ et par $3$.
> 
> - Divisibilité par $7$ : pas de critère facile !
> 
> - Divisibilité par $8$ $\iff$ $8$ divise **les trois derniers chiffres**. Par exemple, pour $abcd$, il faut regarder $bcd$.
> 
> - Divisibilité par $9$ $\iff$ $9$ divise **la somme de tous les chiffres**. Par exemple, pour $abc$, il faut $3 \mid a + b + c$.
> 
> - Divisibilité par $10$ $\iff$ divisibilité par $2$ et par $5$.
> 
> - Divisibilité par $11$ $\iff$ $11$ divise **la somme altérées de tous les chiffres**. Par exemple, pour $abcdef$, il faut que $11 \mid (a-b+c-d+e-f)$.
> 
> - Divisibilité par $12$ $\iff$ divisibilité par $3$ et par $4$.
> 
> - Divisibilité par $13$ : pas de critère facile !
> 
> - Divisibilité par $14$ $\iff$ divisibilité par $2$ et par $7$.
> 
> - Divisibilité par $15$ $\iff$ divisibilité par $3$ et par $5$.
> 
> - Divisibilité par $16$ $\iff$ $16$ divise **les quatre derniers chiffres**.
> 
> - Divisibilité par $17$ : pas de critère facile !
> 
> - Divisibilité par $18$ $\iff$ divisibilité par $2$ et par $9$.
> 
> - Divisibilité par $19$ : pas de critère facile !
> 
> - Divisibilité par $20$ $\iff$ divisibilité par $4$ et par $5$.
> 
> - Divisibilité par $21$$\iff$ divisibilité par $3$ et par $7$.



**Exercice 4 (AMC 8-2014)**

Les nombres à 7 chiffres $74A52B1$ et $326AB4C$ sont chacun multiples de 3. Quelle(s) valeur(s) de $C$ pourraient convenir ?

<!-- 
1
--> 

**Exercice 5 (AMC 8-2016)**

Les chiffres 1, 2, 3, 4 et 5 sont chacun utilisés une seule fois pour former un nombre à cinq chiffres $PQRST$.  
Le nombre à trois chiffres $PQR$ est divisible par 4, le nombre à trois chiffres $QRS$ est divisible par 5, et le nombre à trois chiffres $RST$ est divisible par 3.  
Quelle est la valeur de $P$ ?

<!-- 
$PQRST = 12453$
--> 

**Exercice 6 (AMC 8-2018)**

Le nombre à 5 chiffres $2018U$ est divisible par 9. Quel est le reste de la division de ce nombre par 8 ?

<!-- 
$U=7$, donc le reste modulo $8$ vaut $3$.
--> 

### Factorisation en facteurs premiers

> [!NOTE] Exemple
> Factoriser $420$.

> [!NOTE] Exemple
> Factoriser $117$.

> [!NOTE] Exemple
> Factoriser $1001$.

> [!NOTE] Exemple
> Factoriser $101$.

**Exercice 7 (AMC 8-2011)**

Que vaut la somme des facteurs premiers de $2010$ ?

> [!NOTE] Rappel sur le comptage
> Nombres de facteurs de $12$ = ?
> 
> Nombres de facteurs de $p^a \times q^b \times r^c = (a+1) (b+1) (c+1)$.
> (Ici, $p, q, r$ sont des nombres premiers **distincts**.)

**Exercice 8 (AMC 8-2018)**

$23232$ admet combien de facteurs (positifs) ?

<!-- 
On a $23232=2^6 \times 3 \times 11^2$, donc il a $7 \times 2 \times 3 = 42$ facteurs.
--> 

**Exercice 9 (AMC 8-2018)**

Soit $N$ le plus grand nombre à cinq chiffres dont le produit des chiffres est égal à 120.  
Quelle est la somme des chiffres de $N$ ?

<!-- 
$120 = 2^3 \times 3 \times 5$, donc seulement $2, 3, 4, 5, 6, 8$ peuvent apparaître. Mais il n'y a que cinq facteurs premiers (avec multiplicités).
On a donc $N = 85311$, dont la somme des chiffres fait $18$.
--> 

**Exercice 10 (AMC 8-2003)**

Lequel parmi $55, 57, 58, 59, 61$ possède le plus petit facteur premier ?

<!--  
$58$, car $2$ en est un facteur premier.
--> 

**Exercice 11 (AMC 8-2007)**

Quelle est la somme des deux plus petits facteurs premiers de 250 ?

<!-- 
$250 = 2 \times 5^3$, donc la somme fait $2+5 = 7$.
--> 

**Exercice 12 (AMC 8-2017)**

Donner un facteur de $ABCABC$.

<!--  
$1001 = 7 \times 11 \times 13$.
--> 

### Puissance

> [!NOTE] 
> - $x^a \cdot x^b = x^{a+b}$
> - $(x^a)^b = x^{ab}$
> - $x^{-a} = 1/x^a$
> - $\sqrt[n]{x} = x^{1/n}$

**Exercice 12.5 (AMC 8-2013)**

Si $3^p + 3^4  = 90$, $2^r + 44  = 76$ et $5^3 + 6^s = 1421$, quel est le produit de $p, r, s$ ?

## Congruence/arithmétique modulaire

### Division

> [!NOTE]
> On divise $n$ par $m$, on obtient **le quotient** $q$ et **le reste** $r$, c'est-à-dire :
> $n = m \cdot q + r$.
> Si on veut se concentré sur le reste, on peut écrire
> $n \equiv m \pmod r \quad \text{ou} \quad n \equiv m~[r]$.

**Exercice 13 (AMC 8-2016)**

Soit $N$ un nombre à deux chiffres.
- Quand on divise $N$ par 9, le reste est 1.
- Quand on divise $N$ par 10, le reste est 3.  

Quel est le reste de la division de $N$ par 11 ?

<!-- 
Regarder $10, 19, 28, 37, 46, 55, 64, 73, 82, 91$ et $13, 23, 33, 43, 53, 63, 73, 83, 93$.
Donc $N = 73$, et le reste modulo $11$ fait $7$.
--> 

**Exercice 14 (AMC 8-2012)**

Quel est le plus petit $n > 1$ qui a un reste de $1$ lorsqu'il est divisé par $2, 3, 4, 5, 6$.

<!-- 
$61 = \mathrm{ppcm}(2, 3, 4, 5, 6) = 60$.
--> 

**Exercice 15 (AMC 8-2018)**

Combien de $n > 1$ à trois chiffres sont congruents à $2$ modulo $6$, à $5$ modulo $9$, et à $7$ modulo $11$ ?

<!-- 
Ça veut dire congruent à $-4$ modulo $\mathrm{ppcm}(6,9,11)$, donc on a $198n-4$ $\implies$ $5$
--> 

### Trouver le pgcd (et le ppcm)

> [!NOTE] Division euclidienne
> 又叫辗转相除法。
> 原理：si $d = pgcd(a,b)$, alors $d$ divise $a, a-b, a-2b, \dots$, en particulier $d$ divise le reste de $a$ pour sa division par $b$.

> [!NOTE] 
> Calculer $d = pgcd(123,108)$.
> - $123$ divisé par $108$ $\implies$ le reste est $15$.
> - $108$ divisé par $15$ $\implies$ le reste est $3$.
> - $15$ est divisible par $3$ sans reste !
> 
> Donc $3 = pgcd(123,108)$.

**Exercice 16**

Calculer :
- $pgcd(108,78)$,
- $pgcd(36,44)$,
- $pgcd(36,78)$.

### Cycle des restes

> [!NOTE]
> Fixons des entiers $a$ et $N$.
> Alors le reste de $a^n$ modulo $N$ est cyclique par rapport à $n$.

**Exercice 17 (AMC 8-2012)**

Quel est le dernier chiffre de $13^{2012}$ ?

<!-- 
1
--> 

**Exercice 18**

Quel est le dernier chiffre de $2^{1026}$ ?

<!-- 
4
--> 

**Exercice 19 (AMC 8-2000)**

Quel est le dernier chiffre de $19^{19} + 99^{99}$ ?

<!-- 
8
--> 

**Exercice 20 (AMC 8-2011)**

Quels sont les derniers deux chiffres de $7^{2011}$ ?

<!-- 
43
--> 

**Exercice 21 (AMC 8-2007)**

Quels sont les quatres derniers chiffres de $30303030303030303 \times 505050505050505050505$ ?

<!-- 
3015
--> 

## Divers

**Exercice 22 (AMC 8-2014)**

Un nombre à deux chiffre est égal au produit de ces deux chiffres. Quel est le dernier chiffre ?

<!-- 
9
--> 

**Exercice 23 (AMC 8-2009)**

Les deux entiers $x, y > 0$ sont les nombres minimaux tels que $360 \times x$ soit un carré et que $360 \times y$ soit un cube.  Que vaut la somme $x + y$ ?

<!-- 
10 + 75
--> 

**Exercice 24 (AMC 8-2006)**

Si $ABA \times CD = CDCD$, alors que vaut $A + B$ ?

<!-- 
ABA = 101
--> 

**Exercice 25 (AMC 8-2017)**

<!-- $$\newcommand{\abs}[1]{\left|#1\right|}$$ -->

La **valeur absolue** $\abs{a}$ d'un nombre $a$ est égale à $a$ si $a$ est positif, et est égale à $-a$ si $a$ est négatif, par exemple : $\abs{25} = \abs{-25} = 25$.

Combien de résultats peut-on obtenir pour $\frac{a}{\abs{a}} + \frac{b}{\abs{b}} + \frac{c}{\abs{c}} + \frac{abc}{\abs{abc}}$ ?

<!-- 
0, ±6
--> 

**Exercice 25 (AMC 8-2012)** 

Quel est le plus petit $n > 2$ qui a un reste de $2$ lorsqu'il est divisé par $3, 4, 5, 6$.

<!-- 
62
--> 

**Exercice 26 (AMC 8-2017)** 

Il y a combien de cubes entre $2^8+1$ et $2^{18}+1$ ?
Indication : $x^{3n} = (x^n)^3$ .

<!-- 
$7^3, \dots, 64^3$
--> 

**Exercice 27 (AMC 8-2010)** 

Comparer $10^8, 5^{12}, 2^{24}$.

<!-- 
$5^{12} > 10^8 > 2^{24}$
--> 

**Exercice 28 (AMC 8-2011)** 

$4^5 \times 5^{10}$ est à combien de chiffres ?
Indication :  $10 = 2 \times 5$.

<!-- 
$100^5 = 10000000000$
--> 

**Exercice 29 (AMC 8-2000)**

Quel est le dernier chiffre de $13^{17} + 17^{13}$ ?

<!-- 
0
--> 

