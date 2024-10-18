---
layout: default
title: "Analyse de sentiment"
parent: "Analyse textuelle"
grand_parent: "Traitements du langage et Social media"
nav_order: 2
---

# Analyse de sentiment

L'**analyse de sentiment** est une technique de traitement du langage naturel qui vise à déterminer l'opinion ou l'émotion exprimée dans un texte. Elle permet de classifier des documents textuels en catégories telles que positive, négative ou neutre. Cette technique est largement utilisée pour analyser les avis clients, les commentaires sur les réseaux sociaux, les critiques de produits, et bien plus encore.

## Objectifs de cette section

- Comprendre le concept d'analyse de sentiment.
- Découvrir les méthodes courantes utilisées pour l'analyse de sentiment.
- Apprendre à utiliser Orange Data Mining pour effectuer une analyse de sentiment.
- Interpréter et visualiser les résultats obtenus.

## 1. Qu'est-ce que l'Analyse de Sentiment ?

### 1.1 Définition

L'analyse de sentiment, également appelée **opinion mining**, est le processus qui consiste à identifier et extraire les informations subjectives dans les sources de texte. Elle permet de déterminer l'attitude de l'auteur du texte à l'égard d'un sujet spécifique ou d'une entité en particulier.

### 1.2 Importance

- **Compréhension des opinions** : aide les entreprises/chercheurs à comprendre ce que les clients pensent de leurs produits ou services / d'un sujet ou d'une thematique.
- **Surveillance de la réputation** : permet de surveiller l'image de marque sur les médias sociaux et autres plateformes en ligne.
- **Prise de décision** : les gouvernements et organisations peuvent utiliser l'analyse de sentiment pour prendre des décisions basées sur l'opinion publique.

## 2. Méthodes d'snalyse de sentiment

### 2.1 Approches basées sur les règles

- **Lexiques de sentiment** : utilisation de dictionnaires qui associent des mots à des scores de sentiment (positif ou négatif).
- **Avantage** : simples à mettre en œuvre.
- **Limite** : ne capturent pas le contexte ou les nuances du langage.

### 2.2 Approches Basées sur l'apprentissage automatique

- **Modèles Supervisés** : entraînement de modèles sur des données annotées en sentiments (positif, négatif, neutre).
  - **Algorithmes Courants** : régression logistique, SVM, Naïve Bayes.
- **Avantage** : meilleure précision en capturant les nuances du langage.
- **Limite** : nécessite un jeu de données annoté pour l'entraînement.

### 2.3 Approches basées sur l'apprentissage profond

- **Réseaux de Neurones** : utilisation de LSTM, CNN, ou Transformers pour capturer les dépendances complexes dans le texte.
- **Avantage** : performance élevée sur des tâches complexes.
- **Limite** : nécessite des ressources computationnelles importantes et des compétences avancées.

## 3. Analyse de sentiment avec Orange Data Mining

Orange Data Mining propose des widgets pour réaliser une analyse de sentiment sans avoir à coder. Il utilise des modèles pré-entraînés et des lexiques pour estimer le sentiment des textes.

### 3.1 Préparation des données

Avant d'effectuer l'analyse de sentiment, il est important de prétraiter les données :

- **Nettoyage du Texte** : suppression des caractères spéciaux, des URLs, etc.
- **Tokenisation** : découpage du texte en mots (tweet) individuels .
- **Lemmatisation** : réduction des mots à leur forme canonique.
- **Suppression des Mots Vides** : élimination des mots courants qui n'apportent pas de valeur sentimentale.

### 3.2 Flux de travail dans Orange

#### Étape 1 : chargement du corpus

- **Widget utilisé** : **Corpus**
- **Action** :
  - Importer les données textuelles (par exemple, des tweets).

#### Étape 2 : prétraitement du texte

- **Widget utilisé** : **Préprocess text**
- **Paramètres à configurer** :
  - **Convertir en minuscules**
  - **Supprimer la ponctuation**
  - **Tokeniser par mots**
  - **Lemmatiser** (choisir la langue appropriée)
  - **Supprimer les mots vides**

#### Étape 3 : Analyse de sentiment

- **Widget utilisé** : **Sentiment Analysis**
- **Paramètres** :
  - **Langue** : sélectionner la langue du texte (par exemple, Français).
  - **Méthode** : choisir la méthode d'analyse (par exemple, Basée sur le lexique).
- **Action** :
  - Le widget ajoute une nouvelle variable à chaque document avec le score de sentiment.

#### Étape 4 : visualisation des résultats

- **Widget utilisé** : **Distributions** ou **Box Plot**
- **Action** :
  - Visualiser la distribution des scores de sentiment.
  - Identifier les documents les plus positifs ou les plus négatifs.

  ***(Le terme document désigne tout type de texte non structuré : article de blog, article d’actualité, tweet, mise à jour de statut, document commercial, …)***

#### Étape 5 : Exploration plus approfondie

- **Widget utilisé** : **Word Cloud**, **Data Table**
- **Action** :
  - Examiner les mots les plus fréquents dans les textes positifs ou négatifs.
  - Analyser des exemples spécifiques de documents pour comprendre les résultats.

## 4. Interprétation des résultats

### 4.1 Comprendre les scores de sentiment

- **Scores numériques** : le score peut être une valeur continue (par exemple, de -1 à 1) ou catégorielle (Positif, Négatif, Neutre).
- **Polarité** :
  - **Positif** : indique une opinion favorable.
  - **Négatif** : indique une opinion défavorable.
  - **Neutre** : pas d'opinion claire ou sentiments mitigés.

### 4.2 Identifier les tendances

- **Tendance générale** : déterminer si l'opinion publique est globalement positive ou négative.
- **Analyse des Cas Extrêmes** : étudier les textes avec les scores les plus élevés ou les plus bas pour comprendre les raisons.

## 5. Limitations et considérations

### 5.1 Ironie et sarcasme

- **Défi** : les approches basées sur les mots ont du mal à détecter l'ironie ou le sarcasme, ce qui peut fausser les résultats.

### 5.2 Langage informel

- **Défi** : les abréviations, le langage familier, les fautes d'orthographe peuvent affecter la précision de l'analyse.

### 5.3 Domaines spécifiques

- **Défi** : les lexiques généraux peuvent ne pas être adaptés aux domaines spécifiques (par exemple, sociologique, géographique, médical, juridique).

## 6. Améliorations possibles

- **Personnalisation du lexique** : ajouter des mots spécifiques au domaine d'étude avec des scores de sentiment appropriés.
- **Annotation Manuelle** : créer un petit jeu de données annoté manuellement pour entraîner un modèle supervisé plus précis.
- **Combinaison avec d'autres méthodes** : utiliser des techniques avancées comme les Word Embeddings pour capturer le contexte.

## 7. Ressources Supplémentaires

- **Documentation Orange** :
  - [Orange3 Text Documentation](https://orange.biolab.si/widget-catalog/text-mining/)
- **Lexiques de Sentiment** :
  - **VADER** : un lexique adapté pour les médias sociaux (nécessite adaptation pour le français).
  - **SentiWordNet** : Un lexique général pour l'anglais (nécessite adaptation pour le français).

## Conclusion

L'analyse de sentiment est un outil précieux pour comprendre les opinions exprimées dans de grandes quantités de données textuelles. En utilisant Orange Data Mining, vous pouvez réaliser cette analyse sans avoir à **coder**, ce qui rend cette technique accessible à un large public. En étant conscient des limitations et en prenant des mesures pour les atténuer, vous pouvez obtenir des insights significatifs pour informer la prise de décision.
