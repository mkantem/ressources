---
layout: default
title: "Scrapy-GUI"
parent: "Outils sans codage"
grand_parent: "Introduction et scraping de données"
ancestor: "Traitements du langage et Social media"
nav_order: 4
---

# Scrapy-GUI

**Scrapy-GUI** est une interface graphique pour le célèbre framework Scrapy, permettant de créer des spiders et de scraper des données sans écrire de code. Il rend l'utilisation de Scrapy accessible aux utilisateurs non techniques via une interface visuelle.

## Installation de Scrapy-GUI

### Étapes d'installation :

1. Assurez-vous d'avoir [**Python**](https://etudestech.com/decryptage/comment-installer-python/){:target="_blank"} installé sur votre machine.
2. Installez **Scrapy-GUI** via pip en exécutant la commande suivante :
```bash
    pip install scrapy-GUI
```

3. Une fois installé, lancez l'application avec la commande suivante :
```bash
    scrapy-gui 
    ou 
    scrapy_gui.open_browser()
```
Cela ouvrira l'interface graphique de Scrapy où vous pourrez configurer vos projets de scraping.

## Utilisation de Scrapy-GUI

### Étape 1 : Créer un nouveau spider

- Après avoir ouvert l'interface, cliquez sur **"New Project"** pour créer un nouveau projet de scraping.
- Entrez l'URL du site web que vous souhaitez scraper et donnez un nom à votre projet.

### Étape 2 : Définir les éléments à scraper

- Sélectionnez les éléments que vous souhaitez extraire (titres, images, etc.) en les pointant dans l'interface.
- Vous pouvez également configurer des règles pour suivre des liens et scraper plusieurs pages.

### Étape 3 : Exécuter le spider

- Une fois les éléments définis, cliquez sur **"Start Spider"** pour démarrer le scraping.
- Les données collectées seront affichées dans la console et peuvent être exportées en différents formats (CSV, JSON, etc.).

## Exercice Pratique avec Scrapy-GUI

### Objectif

Utiliser **Scrapy-GUI** pour extraire les titres et les dates de publication des articles d'un site d'actualités.

### Étapes

1. **Installer Scrapy-GUI** si ce n'est pas déjà fait en suivant les instructions d'installation ci-dessus.
2. **Créer un nouveau projet** en entrant l'URL d'un site d'actualités (par exemple, [https://www.exemple-actualites.com](https://www.exemple-actualites.com)).
3. **Sélectionner les éléments** : Identifiez les titres et les dates des articles en utilisant l'interface visuelle.
4. **Configurer la pagination** pour extraire des données de plusieurs pages si nécessaire.
5. **Exécuter le spider** et collecter les données.
6. **Exporter les données** au format CSV pour les analyser dans un tableur comme **Excel** ou **Google Sheets**.


## Conclusion
Scrapy-GUI est une solution puissante pour les utilisateurs qui souhaitent utiliser Scrapy sans compétences en programmation. Il permet d'accéder à toutes les fonctionnalités avancées de Scrapy via une interface conviviale, rendant le scraping de sites complexes accessible à tous. C'est un excellent outil pour automatiser le scraping de données sans écrire de code ou presque peu, tout en conservant la flexibilité et la puissance de Scrapy.