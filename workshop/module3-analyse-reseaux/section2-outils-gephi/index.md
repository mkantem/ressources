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
- Gephi a besoin de Java pour fonctionner correctement [Installation JDK JAva](/workshop/module2-analyse-texte/section00-prise-en-main-voyant-tools/index.html/#java)

- Téléchargez Gephi depuis le site officiel : [Gephi.org](https://gephi.org/){:target="_blank"}.

![VT](/assets/images/workshop/gephi/gephi1.png) 
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

- **Documentation officielle** : [Gephi Documentation](https://gephi.org/users/)
