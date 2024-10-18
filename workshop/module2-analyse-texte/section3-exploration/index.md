---
layout: default
title: "Exploration des sujets"
parent: "Analyse textuelle"
grand_parent: "Traitements du langage et Social media"
nav_order: 4
---

# Exploration des sujets

Ici, nous allons approfondir la **visualisation de la modélisation de sujet** à l'aide de techniques avancées telles que **t-SNE** et **MDS**.

## Ce que nous allons couvrir :
- **Visualisation bidimensionnelle des documents** : avec t-SNE, nous réduirons la dimensionnalité du corpus pour placer les documents similaires les uns près des autres sur une carte. Cela permet d'explorer la distribution des themes.
  
- **Analyse de la similitude des sujets avec MDS** : le MDS (Multi-Dimensional Scaling) sera utilisé pour visualiser la similitude entre les différents sujets dans un espace à deux dimensions. Plus les points représentant les sujets sont proches, plus leurs thèmes sont similaires. Nous analyserons également la fréquence de chaque sujet dans le corpus.

### Explication de t-SNE et MDS :
- **t-SNE (t-Distributed Stochastic Neighbor Embedding)** : technique de réduction de la dimensionnalité qui place les documents similaires à proximité. C'est particulièrement utile pour les données complexes telles que les textes, car il préserve les relations locales.
  
- **MDS (Multi-Dimensional Scaling)** : méthode de visualisation des similarités entre les sujets. Elle permet de représenter les relations entre les sujets sur une carte où les distances entre les points reflètent les dissimilarités des thèmes.

Ces outils sont cruciaux pour mieux comprendre comment les sujets sont répartis et interagissent dans un corpus de texte.

**NB:** dans le contexte de l'analyse de texte, le terme "document" fait référence à une unité d'analyse textuelle dans un corpus, qui peut être un ensemble de textes ou un seul texte divisé en segments. Un corpus peut contenir plusieurs documents, comme des articles, tweets, ou discours. 