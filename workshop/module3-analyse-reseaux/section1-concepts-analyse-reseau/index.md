---
layout: default
title: "Concepts de l'analyse de réseau"
parent: "Analyse des réseaux"
grand_parent: "Traitements du langage et Social media"
nav_order: 1
---
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Analyse de réseaux

## Introduction à l'analyse de réseaux

### Qu'est-ce que l'analyse de réseaux ?
L'analyse de réseaux est une méthode qui étudie les relations entre des entités appelées **nœuds** et les connexions entre elles, appelées **arêtes**. En modélisant les réseaux sociaux, biologiques, et autres, l'analyse de réseaux utilise la **théorie des graphes** pour comprendre la structure et la dynamique des réseaux.

### Applications
- **Sociologie** : étude des réseaux sociaux, interactions entre individus
- **Biologie** : réseaux de protéines, interactions génétiques
- **Informatique** : réseaux de communication, Internet
- **Épidémiologie** : propagation des maladies

### Importance dans le contexte des médias sociaux
L'analyse de réseaux permet de comprendre comment l'information se diffuse, d'identifier les influenceurs, et de cartographier les communautés en ligne.

---

## Concepts fondamentaux de la théorie des graphes

### Définitions de base
- **Nœuds (sommets)** : les entités du réseau (ex: utilisateurs Twitter)
- **Arêtes (liens)** : les connexions entre nœuds (ex: suivre, mentionner)
- **Graphe dirigé** : les arêtes ont une direction (ex: A suit B)
- **Graphe non dirigé** : les arêtes n'ont pas de direction (ex: A est ami avec B)
- **Graphe pondéré** : les arêtes ont un poids (ex: nombre d’interactions)

**Notation d'un graphe** : un graphe \( G = (V, E) \) est défini par :
- **\( V \)** : ensemble de nœuds ou sommets (Vertex)
- **\( E \)** : ensemble d’arêtes connectant les sommets (Edges)

### Degrés des nœuds
- **Degré (non dirigé)** : nombre total d'arêtes connectées à un nœud \( v \), noté $$\text{deg}(v)$$
- **Degré entrant** $$\text{deg}^{-}(v)$$ : nombre d'arêtes pointant vers le nœud dans un graphe dirigé
- **Degré sortant** $$\text{deg}^{+}(v)$$ : nombre d'arêtes partant du nœud dans un graphe dirigé

### Notions de chemin et de distance
- **Chemin** : séquence de nœuds connectés par des arêtes
- **Cycle** : chemin qui commence et se termine au même nœud
- **Distance géodésique** : longueur du plus court chemin entre deux nœuds \( u \) et \( v \), notée  $$d(u, v)$$

**Exemple de calcul de distance moyenne** :
Pour un graphe avec \( n \) nœuds, la distance moyenne \( D \) est :

$$
D = \frac{1}{\binom{n}{2}} \sum_{i < j} d(v_i, v_j)
$$

où $$d(v_i, v_j)$$ est la distance entre les nœuds $$v_i$$ et $$v_j$$.

### Décomposition de la formule

1. **Distance entre les nœuds** : $$d(v_i, v_j)$$ représente la distance la plus courte entre les nœuds $$v_i$$ et $$v_j$$. Cette distance est souvent mesurée par le nombre d'arêtes sur le chemin le plus court qui les relie dans le graphe.

2. **Somme sur les paires de nœuds** : 
   $$
   \sum_{i < j} d(v_i, v_j)
   $$
   signifie que l'on additionne les distances entre toutes les paires de nœuds $$(v_i, v_j)$$ avec $$i < j$$. Cela permet d’éviter les doublons, car $$d(v_i, v_j)$$ est la même que $$d(v_j, v_i)$$.

3. **Nombre de paires de nœuds** : 
   $$
   \binom{n}{2} = \frac{n(n-1)}{2}
   $$
   est le nombre total de paires de nœuds dans le graphe. Cela représente le nombre de façons de choisir 2 nœuds parmi $$n$$.

4. **Calcul de la distance moyenne** : en divisant la somme des distances par le nombre total de paires de nœuds, on obtient la distance moyenne $$D$$. Cela donne une mesure globale de la ***distance*** dans le graphe, ce qui peut être utile pour évaluer la connectivité et l'efficacité du réseau.

### Interprétation

La distance moyenne $$D$$ permet d'avoir une idée de la "compacité" du graphe : une distance moyenne faible indique que, en général, les nœuds sont proches les uns des autres, tandis qu'une distance moyenne élevée suggère que les nœuds sont éloignés, ce qui pourrait signifier une structure moins efficace ou plus dispersée.

---

## Mesures et statistiques des réseaux

### Centralité
La centralité mesure l'importance d'un nœud dans le réseau.

#### Centralité de degré
Le **degré** $$\text{deg}(v)$$ d'un nœud $$v$$ représente son nombre de connexions :

$$
\text{deg}(v) = \sum_{u \in V} A_{vu}
$$

où \( A \) est la matrice d’adjacence.

#### Centralité d'intermédiarité (betweenness)
Mesure combien de fois un nœud se trouve sur le plus court chemin entre deux autres nœuds. Autrement dit, elle calcule combien de fois 
$$v$$ joue un rôle de pont ou d'intermédiaire dans les connexions entre les autres nœuds du réseau. La centralité d'intermédiarité $$C_B(v)$$ pour un nœud $$v$$ est :

$$
C_B(v) = \sum_{s \neq v \neq t} \frac{\sigma_{st}(v)}{\sigma_{st}}
$$

où $$\sigma_{st}$$ est le nombre de plus courts chemins entre \( s \) et \( t \), et $$\sigma_{st}(v)$$ est le nombre de ces chemins passant par \( v \).

##### Analogie 

Imaginez un graphe orienté (Twitter/X) ou non orienté (Meta (profil normal)) où chaque nœud représente un **utilisateur**, et chaque connexion directe entre deux utilisateurs indique qu’ils se mentionnent dans leurs tweets/posts.

Posons que les utilisateurs $$s$$ et $$t$$ sont deux comptes Twitter qui ne se suivent pas directement, mais qui peuvent interagir indirectement via d'autres utilisateurs.

La centralité d’intermédiarité $$C_B(v)$$ mesure alors **combien de fois un utilisateur** $$v$$ se trouve sur le **chemin le plus court** des échanges ou interactions entre les autres utilisateurs $$s$$ et $$t$$.

Dans ce contexte, un utilisateur ayant une **forte centralité d'intermédiarité** est souvent **mentionné ou retweeté** par plusieurs personnes, le plaçant comme un **influenceur clé** ou **relai** dans le réseau de communication. Ce rôle est essentiel pour faciliter les échanges d’information, et cet utilisateur peut donc influencer la manière dont les informations se propagent à travers le réseau.

#### Centralité de proximité (closeness)
Indique à quel point un nœud est proche des autres :

$$
C_C(v) = \frac{1}{\sum_{u \in V} d(u, v)}
$$

La centralité de proximité $$C_C(v)$$ pour un utilisateur $$v$$ de X mesure à quel point cet utilisateur peut **accéder rapidement aux autres utilisateurs** du réseau, c’est-à-dire combien de tweets d’autres utilisateurs sont à faible distance de lui.

Si cet utilisateur $$v$$ a une **centralité de proximité élevée**, il est probablement **suivi par des comptes influents** ou bien **suivi par de nombreux utilisateurs** qui sont eux-mêmes bien connectés. Cela permet à cet utilisateur d'accéder rapidement à une large gamme de contenu sur Twitter, car les tweets ou les informations publiées par les autres utilisateurs atteignent rapidement son flux.

#### Centralité de vecteur propre (eigenvector)
Prend en compte non seulement le nombre de connexions d’un nœud, mais aussi l'importance des nœuds auxquels il est connecté :

$$
x_i = \frac{1}{\lambda} \sum_{j} A_{ij} x_j
$$

où :
- $$\lambda$$ est une constante (la plus grande valeur propre du graphe),
- $$A_{ij}$$ est un élément de la matrice d'adjacence qui indique la présence d'une connexion entre les nœuds $$i$$ et $$j$$,
- $$x_j$$ est la centralité de vecteur propre du nœud $$j$$.

Cette formule dépend de la somme des centralités de ses voisins, pondérée par les connexions directes dans le graphe. En d’autres termes, un nœud est d’autant plus central que ses voisins sont eux-mêmes centraux.

##### Analogie 
La **centralité de vecteur propre** d’un utilisateur $$i$$ ne mesure pas uniquement le nombre de ses abonnés, mais aussi l'**importance** de ses abonnés.

- Un utilisateur ayant une centralité de vecteur propre élevée est suivi par des utilisateurs eux-mêmes influents. En d'autres termes, si un utilisateur est suivi par de nombreux comptes populaires (ceux qui sont eux-mêmes bien connectés), il aura une centralité de vecteur propre élevée.
- Cela signifie que cet utilisateur est **influant non seulement par son nombre d'abonnés**, mais aussi parce que ses abonnés sont bien connectés, lui donnant accès à un réseau d'audience plus large et plus engagé.

La centralité de vecteur propre permet d’identifier des **influenceurs de haut niveau** qui non seulement ont de nombreux abonnés, mais bénéficient également d'une portée accrue grâce aux réseaux de leurs abonnés.

### Distance moyenne et diamètre du réseau
- **Distance moyenne** \( D \) : moyenne des distances (chemins les plus courts) entre toutes les paires de nœuds. Dans les réseaux sociaux, une faible distance moyenne suggère que les informations peuvent se propager rapidement, car les utilisateurs sont connectés de manière dense.
Dans un réseau de transport, une faible distance moyenne signifie que les trajets sont globalement plus courts, améliorant l’efficacité des déplacements.
- **Diamètre** : distance maximale ou le plus long des chemins les plus courts entre toutes les paires de nœuds. Le diamètre d’un réseau donne une indication de sa taille effective et de ses limites d'accessibilité. Un faible diamètre signifie qu'il est possible d’atteindre tous les nœuds avec un nombre limité d’étapes, ce qui est souhaitable pour des réseaux où la transmission rapide est essentielle.

### Densité du réseau
La **densité** est une mesure qui indique à quel point les nœuds du réseau sont connectés entre eux. Elle compare le nombre d’arêtes actuelles à l’ensemble des arêtes possibles dans le réseau.

$$
\text{Densité} = \frac{2 \times |E|}{|V| \times (|V| - 1)}
$$

### Utilité de la densité
- Réseaux sociaux : dans un réseau social, une forte densité indique que la plupart des membres sont connectés entre eux. Cela peut être typique d'un petit groupe ou d’une communauté très liée.
- Réseaux d'infrastructure : dans un réseau de transport ou de communication, une forte densité peut indiquer une meilleure robustesse et fiabilité, car de nombreux chemins alternatifs existent entre les nœuds.
- Propagation de l’information : un réseau dense favorise la propagation rapide de l’information, car de nombreux chemins existent pour transmettre des messages.

## Détection de communautés

### Qu'est-ce qu'une communauté ?
Une communauté est un sous-ensemble de nœuds dans lequel les connexions sont plus denses qu’avec le reste du réseau.

### Méthodes de détection
- **Algorithme de Louvain** : méthode d'optimisation de modularité pour identifier les communautés
- **Modularité** : mesure de la densité de liens à l'intérieur des communautés :

$$
Q = \frac{1}{2m} \sum_{ij} \left[ A_{ij} - \frac{k_i k_j}{2m} \right] \delta(c_i, c_j)
$$

où \( A \) est la matrice d'adjacence, \( k \) est le degré des nœuds, \( m \) le nombre total d’arêtes, et \delta  est une fonction qui vaut 1 si $$c_i = c_j$$ (nœuds dans la même communauté) et 0 sinon.

---

# Conclusion

L'étude des graphes est un domaine complexe et vaste, au cœur de l'analyse de réseaux. Bien qu'il s'agisse d'une spécialisation qui demande un approfondissement, cette introduction permet de saisir les éléments essentiels pour des analyses pratiques de données. Comprendre les concepts de nœuds, d'arêtes, de centralité et de communauté offre une base solide pour interpréter les réseaux dans différents contextes, qu'il s'agisse des réseaux sociaux ou d'autres types de connexions. En maîtrisant ces notions, vous pouvez exploiter efficacement l'analyse de réseaux dans vos projets. 

Dans un passé récent, j'étais profondément investi dans la théorie des graphes et les grammaires de graphes avant de me tourner vers la sécurité comportementale de l'information et la santé maternelle ;). Un de nos projets phares reposait sur une approche algébrique pour la manipulation de structures de graphes, utilisant le framework Eclipse Modeling (EMF). Cet environnement permet de manipuler des modèles et de générer automatiquement des outils de modélisation, avec notamment l'utilisation de productions finies sous forme de triplets (M, D, E), où M et D représentent des structures de graphes et E un ensemble de règles de transformation (voir mon github pour les codes (2015/2016)).

## Références et ressources supplémentaires
  - "Networks: An Introduction" de Mark Newman
  - "Exploratory Social Network Analysis with Pajek" de Wouter de Nooy et al.
  - "Graph Theory" de Reinhard Diestel
  - Bhagat, Smriti, Moira Burke, Carlos Diuk, Ismail Onur Filiz, and Sergey Edunov. 2016. “Three and a Half Degrees of Separation.” facebook research blog https://research.fb.com/three-and-a-half-degrees-of-separation/.
  - Milgram, Stanley. 1967. “The Small World Problem.” Psychology Today 1 (60): –.
  - Yook, Soon-Hyung, Hawoong Jeong, and Albert-Laszlo Barabasi. 2001. “Modeling the Internet’s Large-Scale Topology.”
