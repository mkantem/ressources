---
layout: default
title: "Réseau d'utilisateurs"
parent: "Twitter"
grand_parent: "Analyse des réseaux"
nav_order: 1
has_children: true
---


# Réseau d'utilisateurs

Nous allons construire et analyser un réseau d'utilisateurs Twitter basé sur les interactions de réponse.

## Réseau de Tweets utilisateurs

### Concept
Le réseau d'utilisateurs Twitter se concentre sur les relations entre utilisateurs à travers leurs réponses. Chaque interaction est représentée par un lien qui aide à visualiser la structure de la conversation et les influences au sein de la communauté.

- **Noeuds (Nodes)** : représentent les utilisateurs.
- **Liens (Edges)** : chaque lien indique qu’un utilisateur (source) a répondu à un autre utilisateur (cible).

### Objectifs de l'analyse
- Identifier des **communautés** d'utilisateurs engagés dans des sujets spécifiques.
- Détecter des **nœuds centraux** influents (comptes recevant de nombreuses réponses).
- Observer la **propagation d'informations** ou d'idées à travers les réponses et mentions.

### Exemple de cas Pratique
Dans ce tutoriel, nous allons utiliser l'API Twitter (vous devez disposez d'au moins la version payante basic pour suivre (100$)) pour extraire des tweets contenant des réponses et créer un fichier CSV des interactions. Ensuite, nous importerons ces données dans gephi pour visualiser le réseau et détecter les communautés.

### Étapes Pratiques
1. **Extraction des Données** : utilisation de l'API Twitter pour obtenir des tweets répondant à un sujet particulier.
2. **Création du fichier CSV** : structurez les données sous forme de source et cible.

![VT](/assets/images/workshop/gephi/x/gephi2.png)

3. **Visualisation avec Gephi** : importez les données dans Gephi pour observer les interactions, détecter les communautés et analyser les influenceurs.

![VT](/assets/images/workshop/gephi/x/gephi1.png) 

### Conclusion
L'analyse des réseaux sur Twitter offre un aperçu puissant des dynamiques de communication et des relations d'influence, facilitant une meilleure compréhension des échanges et des tendances sur la plateforme.

