---
layout: default
title: "Modelisation de sujet"
parent: "Analyse textuelle"
grand_parent: "Traitements du langage et Social media"
nav_order: 3
---

# Modélisation de sujets

La **modélisation de sujets** est une technique d'apprentissage automatique non supervisé qui permet d'identifier automatiquement les thèmes ou sujets présents dans un corpus de documents textuels. Elle est particulièrement utile pour explorer de grands ensembles de données textuelles et extraire des informations pertinentes sans avoir à lire chaque document individuellement.

## Objectifs de cette section

- Comprendre le concept de modélisation de sujets.
- Se familiariser avec l'algorithme **Allocation de Dirichlet Latente (LDA)**.
- Apprendre à utiliser Orange Data Mining pour effectuer une modélisation de sujets.
- Interpréter et visualiser les résultats obtenus.

## 1. Qu'est-ce que la modélisation de sujets ?

### 1.1 Définition

La modélisation de sujets vise à découvrir automatiquement les sujets cachés dans un corpus de documents en analysant les cooccurrences de mots. Chaque document est considéré comme un mélange de plusieurs sujets, et chaque sujet est représenté par un ensemble de mots clés.

### 1.2 Applications

- **Analyse de médias sociaux** : identifier les thèmes dominants dans des tweets, des posts Facebook, etc.
- **Recherche documentaire** : faciliter la navigation dans de grandes bases de données de documents.
- **Marketing** : comprendre les préoccupations des clients à partir des avis et commentaires.
- **Journalisme** : détecter les tendances émergentes dans les actualités.

## 2. L'Allocation de Dirichlet Latente (LDA)

### 2.1 Présentation de LDA

L'**Allocation de Dirichlet Latente (LDA)** est l'un des algorithmes les plus populaires pour la modélisation de sujets. Il s'agit d'un modèle génératif probabiliste qui suppose que :

- Chaque document est une combinaison aléatoire de sujets.
- Chaque sujet est une distribution sur les mots du vocabulaire.

### 2.2 Comment fonctionne LDA ?

- **Hypothèses de base** :
  - Les documents sont générés en sélectionnant des sujets selon une distribution spécifique, puis en choisissant des mots à partir de ces sujets.
- **Processus** :
  1. **Choix des sujets** : pour chaque document, LDA détermine une distribution de probabilités sur les sujets.
  2. **Assignation des mots** : chaque mot du document est assigné à un sujet en fonction de cette distribution.
  3. **Optimisation** : l'algorithme ajuste les distributions pour maximiser la probabilité des données observées.

### 2.3 Paramètres clés de LDA

- **Nombre de sujets (K)** : le nombre de sujets à découvrir dans le corpus. C'est un paramètre que l'utilisateur doit définir.
- **Hyperparamètres alpha et beta** :
  - **Alpha (α)** : contrôle la distribution des sujets dans les documents. Une faible valeur favorise les documents avec peu de sujets, tandis qu'une valeur élevée favorise les documents avec une répartition plus uniforme des sujets.
  - **Beta (β)** : contrôle la distribution des mots dans les sujets. Une faible valeur favorise les sujets avec quelques mots dominants, tandis qu'une valeur élevée favorise une répartition uniforme des mots.

## 3. Utilisation de Orange Data Mining pour la modélisation de sujets

### 3.1 Préparation des données

Avant de procéder à la modélisation de sujets, il est essentiel de prétraiter les données textuelles :

- **Nettoyage** : suppression des caractères spéciaux, des URLs, etc.
- **Tokenisation** : découpage du texte en mots individuels.
- **Lemmatisation** : réduction des mots à leur forme canonique.
- **Suppression des mots vides** : élimination des mots fréquents qui n'apportent pas de sens significatif (par exemple, "le", "de", "et").

### 3.2 Flux de travail dans Orange

Voici les étapes pour effectuer une modélisation de sujets avec Orange :

#### Étape 1 : Chargement du Corpus

- **Widget utilisé** : **Corpus**
- **Action** :
  - Importer le fichier contenant les données textuelles (par exemple, un fichier CSV avec une colonne de textes).

#### Étape 2 : Prétraitement du Texte

- **Widget utilisé** : **Preprocess**
- **Paramètres à configurer** :
  - **Convertir en minuscules**
  - **Supprimer la ponctuation**
  - **Tokeniser par mots**
  - **Lemmatiser** (choisir la langue appropriée)
  - **Supprimer les mots vides** (sélectionner la liste de stop words en français)

#### Étape 3 : Création du sac de mots

- **Widget utilisé** : **Bag of Words**
- **Action** :
  - Convertir le texte prétraité en une matrice de termes (documents vs mots avec leurs fréquences).

#### Étape 4 : phase de modélisation

- **Widget utilisé** : **Topic Modeling**
- **Paramètres à configurer** :
  - **Nombre de sujets (K)** : définir le nombre de sujets que vous souhaitez découvrir (par exemple, K = 5).
  - **Algorithme** : choisir LDA.
- **Action** :
  - Lancer l'algorithme pour générer les sujets.

#### Étape 5 : visualisation des sujets

- **Widget utilisé** : **Word Cloud** ou **Heat Map**
- **Action** :
  - Visualiser les mots clés associés à chaque sujet.
  - Explorer la répartition des sujets dans les documents.

#### Étape 6 : Interprétation des résultats

- Examiner les mots clés de chaque sujet pour identifier les thèmes.
- Analyser la proportion de chaque sujet dans les documents pour comprendre la distribution thématique.

### 3.3 Conseils pratiques

- **Choix du nombre de sujets** : il peut être utile de tester plusieurs valeurs de K pour trouver le nombre optimal de sujets qui offrent une interprétation significative.
- **Validation** : impliquer des experts du domaine pour valider les sujets identifiés.
- **Itération** : réajuster les paramètres de prétraitement ou de l'algorithme en fonction des résultats obtenus.

## 4. Interprétation des résultats

### 4.1 Analyse des sujets

- **Mots clés dominants** : les mots avec les poids les plus élevés dans un sujet sont les plus représentatifs.
- **Thématique Générale** : en se basant sur les mots clés, assigner un intitulé au sujet (par exemple, "Politique", "Technologie", "Sport").

### 4.2 Analyse des documents

- **Distribution des sujets** : voir quels sujets sont les plus présents dans chaque document.
- **Classification** : les documents peuvent être classés ou groupés en fonction de leur sujet dominant.

## 5. Limites et considérations

### 5.1 Limites de LDA

- **Interprétabilité** : les sujets générés peuvent parfois être difficiles à interpréter.
- **Sensibilité aux Paramètres** : les résultats dépendent fortement du nombre de sujets et des hyperparamètres choisis.
- **Hypothèse du Sac de Mots** : LDA ignore l'ordre des mots, ce qui peut limiter la capture de certaines nuances sémantiques.

### 5.2 Bonnes pratiques

- **Nettoyage approfondi** : assurer un prétraitement de qualité pour améliorer les résultats.
- **Analyse exploratoire** : utiliser des visualisations pour explorer les données avant et après la modélisation.

## 6. Étude de Cas : Analyse des Sujets dans des Tweets 

### 6.1 Contexte

- **Objectif** : identifier les thèmes principaux discutés sur Twitter à propos d'un événement spécifique (par exemple, une élection, un événement sportif, une crise sanitaire).

### 6.2 Étapes

1. **Collecte des données** :
   - Utiliser **Lobster** ou le **widget ODM** pour extraire des tweets contenant des hashtags ou mots-clés liés à l'événement.
2. **Prétraitement** :
   - Appliquer les techniques de nettoyage et de prétraitement vues précédemment.
3. **Modélisation de Sujets** :
   - Utiliser Orange pour effectuer la modélisation de sujets avec LDA.
4. **Interprétation** :
   - Examiner les sujets identifiés et comprendre les préoccupations et discussions dominantes sur Twitter concernant l'événement.
5. **Visualisation** :
   - Créer des nuages de mots et des graphiques pour présenter les résultats de manière claire.

## 7. Ressources Supplémentaires

- **Outils Avancés** :
  - **Gensim** : bibliothèque Python pour la modélisation de sujets (nécessite du codage).
  - **Mallet** : outil Java pour la modélisation de sujets offrant des performances optimisées.

## Conclusion

La modélisation de sujets est un outil puissant pour extraire des thèmes cachés dans de grandes quantités de données textuelles. Grâce à des outils comme Orange Data Mining, il est possible d'appliquer ces techniques sans coder, rendant l'analyse accessible à un large public. En comprenant les principes derrière des algorithmes comme LDA et en suivant une méthodologie rigoureuse, vous pouvez obtenir des insights précieux à partir de vos données textuelles.

---
