---
layout: default
title: "Enrichissement des mots"
parent: "Analyse textuelle"
grand_parent: "Traitements du langage et Social media"
nav_order: 8
---

# Enrichissement de mots

L'**Enrichissement de mots** est une technique utilisée pour identifier les mots qui sont statistiquement significatifs dans un sous-ensemble de documents par rapport à l'ensemble complet du corpus. Cela permet de découvrir quels mots sont particulièrement associés à une sélection spécifique de documents, offrant ainsi des insights sur les thèmes ou sujets qui distinguent ce sous-ensemble.

## Objectifs de cette section

- Comprendre le concept d'enrichissement de mots.
- Apprendre à utiliser le widget **Enrichissement de Mots** dans Orange Data Mining.
- Interpréter les résultats obtenus, notamment la signification des p-values et du FDR (False Discovery Rate).

## 1. Qu'est-ce que l'enrichissement de mots ?

### 1.1 Principe

L'enrichissement de mots consiste à comparer la fréquence des mots dans un sous-ensemble de documents sélectionnés avec leur fréquence dans l'ensemble du corpus. Les mots qui apparaissent significativement plus souvent dans le sous-ensemble sont considérés comme enrichis.

### 1.2 Importance

- **Identification des thèmes spécifiques** : permet de déterminer quels mots caractérisent le mieux un groupe de documents.
- **Analyse Comparative** : utile pour comparer différents groupes ou catégories de documents.

## 2. Comment fonctionne l'Enrichissement de Mots dans Orange

Le widget **Word Enrichment** dans Orange calcule la significativité statistique des mots dans les documents sélectionnés par rapport au corpus complet.

### 2.1 Entrées du Widget

- **Corpus** : L'ensemble des documents textuels.
- **Données sélectionnées** : Un sous-ensemble de documents sélectionnés à partir du corpus.

### 2.2 Sorties du widget

- **Aucune sortie directe** : Les résultats sont affichés dans le widget lui-même.

### 2.3 Interprétation des résultats

- **p-value** : indique la probabilité que l'observation d'un mot soit due au hasard. Une p-value plus faible signifie que le mot est plus significativement associé au sous-ensemble sélectionné.
- **FDR (False Discovery Rate)** : représente le taux de fausses découvertes attendu dans la liste des mots significatifs, prenant en compte les tests multiples.

## 3. Utilisation Pratique avec des tweets sur la Politique

### Contexte

Supposons que vous ayez collecté un ensemble de tweets sur des sujets politiques, et que vous souhaitiez identifier les mots spécifiques qui caractérisent un sous-ensemble de tweets, par exemple, ceux qui mentionnent un parti politique particulier ou une politique spécifique.

### Étape 1 : préparation du corpus

- **Collecte des données** :
  - Utilisez un outil comme **Lobster** ou le widget Orange Data Mining pour extraire des tweets contenant des mots-clés ou hashtags politiques (par exemple, `#élections2024`, `#écologie`, `#économie`).
- **Prétraitement** :
  - Nettoyez les tweets en supprimant les URLs, mentions, emojis, etc.
  - Appliquez une tokenisation et supprimez les mots vides.

### Étape 2 : Importer les données dans orange

- **Widget utilisé** : **Corpus**
- **Action** :
  - Importez le fichier contenant les tweets prétraités.

### Étape 3 : sélectionner un sous-ensemble de tweets

- **Objectif** :
  - Sélectionner les tweets qui mentionnent un sujet spécifique, par exemple, l'écologie.
- **Méthode** :
  - Utilisez le widget **Select Rows** ou un widget de visualisation pour filtrer les tweets contenant le mot "écologie".

### Étape 4 : Connecter le Widget Word Enrichment

- **Action** :
  - Reliez le corpus complet et le sous-ensemble sélectionné au widget **Word Enrichment**.

### Étape 5 : Analyser les résultats

- Le widget affichera une liste de mots avec leurs p-values et FDR, indiquant quels mots sont significativement plus fréquents dans les tweets sur l'écologie.

### Exemple de Résultats

- **Mots Enrichis** :
  - "environnement", "durable", "climat", "énergies", "renouvelables", "pollution".
- **Interprétation** :
  - Ces mots sont particulièrement associés aux tweets sur l'écologie et peuvent indiquer les thèmes spécifiques abordés par les utilisateurs.

## 4. Interprétation des résultats

### 4.1 Signification des p-values et FDR

- **p-value Basse** :
  - Un mot avec une p-value faible est fortement associé au sous-ensemble sélectionné.
- **FDR** :
  - Permet de contrôler le taux de fausses découvertes, important lorsque de nombreux tests sont effectués.

### 4.2 Utilisation des Résultats

- **Compréhension des thèmes** :
  - Identifiez les préoccupations majeures des utilisateurs sur le sujet sélectionné.
- **Orientation des analyses futures** :
  - Les mots enrichis peuvent guider vers des analyses plus approfondies, comme la modélisation de sujets ou l'analyse de sentiments.

## 5. Considérations statistiques

- **Taille du sous-ensemble** :
  - Assurez-vous que le sous-ensemble est suffisamment grand pour obtenir des résultats statistiquement significatifs.
- **Biais Potentiels** :
  - Soyez conscient des biais possibles dans les données, comme une surreprésentation de certains points de vue.

## 6. Limites

- **Variabilité du Langage sur les réseaux sociaux** :
  - L'utilisation de slang, abréviations ou fautes d'orthographe peut affecter les résultats.
- **Contextualisation** :
  - Certains mots peuvent avoir des significations différentes selon le contexte, nécessitant une interprétation prudente.

## Conclusion

L'enrichissement de mots est un outil puissant pour extraire des insights spécifiques d'un corpus de textes, en identifiant les termes qui caractérisent le mieux un sous-ensemble de documents. Dans le contexte de tweets sur la politique, cette technique permet de comprendre les sujets spécifiques qui mobilisent les utilisateurs sur les réseaux sociaux.
