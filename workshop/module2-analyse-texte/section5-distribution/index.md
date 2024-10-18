---
layout: default
title: "Distribution des mots"
parent: "Analyse textuelle"
grand_parent: "Traitements du langage et Social media"
nav_order: 6
---

# Distribution 

Le widget **Distribution** dans Orange Data Mining est un outil puissant pour visualiser la distribution des variables dans vos données, y compris les mots dans un corpus textuel. Il permet d'explorer la fréquence des mots ou des thèmes et de comparer leur occurrence dans différents sous-ensembles de données.

## Objectifs de cette section

- Comprendre le fonctionnement du widget **Distribution**.
- Apprendre à l'utiliser pour analyser la distribution des mots dans un corpus textuel.
- Interpréter les visualisations pour extraire des insights significatifs.

## 1. Présentation du widget distribution

### 1.1 Fonctionnalités principales

- **Visualisation de la Distribution** : affiche la distribution des valeurs pour une variable sélectionnée sous forme d'histogramme ou de diagramme en barres.
- **Comparaison de Groupes** : permet de comparer la distribution entre différents groupes ou classes dans les données.
- **Sélection Interactive** : offre la possibilité de sélectionner des sous-ensembles de données directement depuis le graphique pour une analyse plus approfondie.

### 1.2 Pourquoi l'utiliser pour la Distribution de mots ?

- **Fréquence des Mots** : visualiser les mots les plus fréquents dans le corpus.
- **Analyse comparative** : comparer la fréquence des mots entre différents groupes de documents (par exemple, sentiments positifs vs négatifs).
- **Identification de tendances** : détecter les mots ou thèmes dominants dans les données textuelles.

## 2. Utilisation du widget distribution pour les mots

### 2.1 Préparation des données

Avant d'utiliser le widget **Distribution**, il est nécessaire de transformer les données textuelles en une forme appropriée :

- **Prétraitement du texte** : nettoyage, tokenisation, lemmatisation, suppression des mots vides.
- **Création du sac de mots** : utilisez le widget **Bag of Words** pour convertir le texte en une représentation numérique basée sur la fréquence des mots.

### 2.2 Flux de travail dans Orange

#### Étape 1 : chargement du corpus

- **Widget utilisé** : **Corpus**
- **Action** :
  - Importer vos données textuelles dans Orange.

#### Étape 2 : prétraitement du texte

- **Widget utilisé** : **Prétraitement du Texte**
- **Action** :
  - Nettoyer et préparer le texte pour l'analyse.

#### Étape 3 : création du sac de Mots

- **Widget utilisé** : **Bag of Words**
- **Action** :
  - Convertir le corpus prétraité en une matrice de termes.

#### Étape 4 : sélection de la variable de mot

- **Widget utilisé** : **Select columns**
- **Action** :
  - Sélectionner le ou les mots spécifiques que vous souhaitez analyser, ou choisir la variable représentant les mots.

#### Étape 5 : visualisation avec le Widget Distribution

- **Widget utilisé** : **Distribution**
- **Action** :
  - Connecter le widget **Distribution** au flux de travail.
  - Sélectionner la variable correspondant aux mots ou aux fréquences de mots.
  - Visualiser la distribution des mots dans le corpus.

### 2.3 Options du Widget Distribution

- **Variable à visualiser** : choisissez la variable représentant les mots ou les fréquences.
- **Groupes** : si vous avez une variable de classe (par exemple, sentiment positif/négatif), vous pouvez comparer la distribution entre les groupes.
- **Type de graphique** : Histogramme, diagramme en barres, etc.

## 3. Interprétation des résultats

### 3.1 Fréquence des mots

- **Mots les plus fréquents** : les mots avec les barres les plus hautes sont les plus fréquents dans le corpus.
- **Longue Traîne** : observez si une petite proportion de mots est très fréquente tandis que de nombreux mots sont rares.

### 3.2 Comparaison entre groupes

- **Différences de fréquence** : identifiez les mots qui sont plus fréquents dans un groupe par rapport à un autre.
- **Insights sur les thèmes** : comprendre quels mots ou thèmes sont associés à différents sous-ensembles de données.

### 3.3 Sélection interactive

- **Analyse approfondie** : sélectionnez des barres spécifiques pour filtrer les données et effectuer des analyses supplémentaires avec d'autres widgets.

## 4. Exemple pratique

Supposons que vous analysiez des avis des participants a votre etude avec des étiquettes de sentiment (positif ou négatif).

#### Étapes :

1. **Charger les Données** : importez les avis enquetés avec leur texte et leur étiquette de sentiment.
2. **Prétraiter le Texte** : nettoyez les avis et créez le sac de mots.
3. **Visualiser la Distribution** :
   - Utilisez le widget **Distribution** pour visualiser la fréquence des mots.
   - Sélectionnez la variable de sentiment comme variable de groupe.
4. **Interpréter** :
   - Comparez les mots les plus fréquents dans les avis positifs et négatifs.
   - Identifiez les mots spécifiques qui caractérisent chaque groupe.

## 5. Conseils pratiques

- **Filtrage des mots Rares/Frequents** : vous pouvez utiliser le widget **Filter** pour exclure les mots trop rares ou trop fréquents qui pourraient ne pas être informatifs.
- **Combinaison avec d'autres widgets** : utilisez le widget **Word Cloud** pour compléter l'analyse visuelle.
- **Attention aux Mots Vides Restants** : assurez-vous que le prétraitement a correctement éliminé les mots vides pour éviter qu'ils ne dominent la distribution.

## Conclusion

Le widget **Distribution** est un outil essentiel pour explorer la fréquence et la répartition des mots dans un corpus textuel. Il offre une visualisation claire qui facilite l'identification des mots clés et la compréhension des tendances dans les données. En l'utilisant conjointement avec d'autres widgets dans Orange, vous pouvez mener une analyse textuelle approfondie sans avoir besoin de coder.

---

**Remarque :**

La visualisation de la distribution des mots est particulièrement utile lors de l'exploration initiale des données pour orienter les analyses futures et identifier les points d'intérêt potentiels.
