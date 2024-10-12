---
layout: default
title: "Outils Gephi"
parent: "Analyse des réseaux"
grand_parent: "Traitements du langage et Social media"
nav_order: 2
has_children: true
---

## Introduction à Gephi

Gephi est un logiciel open-source d’analyse de réseaux et de visualisation. Il est particulièrement utile pour explorer les réseaux de manière interactive.

### Fonctionnalités principales
- **Importation/Exportation** : formats supportés (CSV, GEXF)
- **Visualisation dynamique** : layouts variés (Fruchterman-Reingold, force atlas, layout circulaire, ...)
- **Calcul des mesures** : centralité, clustering, détection de communautés
- **Personnalisation** : couleurs, tailles, étiquettes pour une meilleure visualisation

### Installation
Téléchargez Gephi depuis le site officiel : [Gephi.org](https://gephi.org/){:target="_blank"}.

---

## Analyse de réseaux avec Gephi

### Importation des données
Préparez vos données en fichiers CSV avec :
- **Nœuds** : identifiants et attributs des nœuds
- **Arêtes** : sources, cibles, poids des liens

### Visualisation du réseau
1. **Paramètres de base** : choisissez le type de graphe (dirigé/non dirigé)
2. **Utilisation des layouts** :
   - **Fruchterman-Reingold** : équilibrage des forces
   - **Force Atlas** : regroupe les clusters naturels

### Calcul des mesures
1. Ouvrez l’onglet **Statistiques**
2. Sélectionnez et appliquez les mesures de centralité et de clustering

### Détection et visualisation des communautés
1. Utilisez l'algorithme de **Louvain**
2. Colorez les communautés pour visualiser les sous-groupes

---

## Étude de cas : analyse de tweets avec Gephi

### Collecte des données Twitter
1. Utilisez un outil comme **Lobster** ou le plugin pour collecter les tweets
2. Organisez les données en nœuds (utilisateurs) et en arêtes (relations de mention, retweet, etc.)

### Préparation et importation des données
1. Créez des fichiers CSV pour les nœuds et arêtes
2. Importez dans Gephi, en assignant des attributs aux nœuds (nombre de followers, localisation)

### Analyse et interprétation
- **Identification des influenceurs** : utilisez la centralité de degré
- **Visualisation des communautés** : appliquez l'algorithme de Louvain et interprétez les sous-groupes

---

- **Documentation officielle** : [Gephi Documentation](https://gephi.org/users/)
- **Tutoriels en ligne** : cherchez "Tutoriel Gephi en français" sur YouTube pour des vidéos détaillées