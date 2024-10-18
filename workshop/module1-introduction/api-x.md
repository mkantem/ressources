---
layout: default
title: "API Twitter V2"
parent: "Collecte de données via API"
grand_parent: "Introduction et scraping de données"
nav_order: 1
---

# Collecte de données avec l'API Twitter V2

Dans cette section, nous allons explorer comment utiliser l'API Twitter V2 pour collecter des données depuis la plateforme Twitter. Cela inclut le processus complet, depuis la création d'un compte développeur Twitter jusqu'à la configuration d'un environnement de travail dans Google Colab pour exécuter des requêtes vers l'API et récupérer des données en temps réel.

## Étape 1 : création d'un compte développeur Twitter

Pour utiliser l'API Twitter, vous devez d'abord posséder un compte développeur Twitter :
1. **Inscription** : allez sur [Twitter Developer](https://developer.twitter.com/){:target="_blank"} et connectez-vous avec votre compte Twitter.
2. **Demande d'accès développeur** : cliquez sur *Apply for a Developer Account* et suivez les instructions pour soumettre une demande. Cela inclut la description de votre projet et les raisons pour lesquelles vous souhaitez accéder à l'API.
3. **Confirmation et accès** : une fois la demande approuvée, vous recevrez un accès au portail développeur de Twitter.

### Tarification de l'API V2

Depuis les récents changements sous Elon Musk, l’accès à l’API Twitter est désormais payant, avec trois niveaux principaux :

1. **Forfait gratuit** : ne permet que la publication de tweets, jusqu’à 1 500 par mois. Il n’autorise pas l’extraction de tweets d’utilisateurs.
2. **Forfait basique** : au tarif de 100 $ par mois, permet d'extraire jusqu'à 10 000 tweets par mois, avec des limites d’interaction plus étendues.
3. **Forfait entreprise** : offre un accès de grande envergure avec un tarif personnalisé.

Ces options visent à monétiser l’API et restreignent l'accès aux données.

[Plus de détails](https://developer.twitter.com){:target="_blank"}.

## Étape 2 : création d'un projet et d'une application

Après l'approbation de votre compte :
1. **Créer un projet** : dans le tableau de bord développeur, créez un nouveau projet en cliquant sur *Create Project*. Donnez-lui un nom et une description correspondant à vos objectifs.
2. **Générer les Clés d'API** : lors de la création de l'application associée, Twitter vous fournira des clés d'API et des jetons de sécurité. **Notez-les soigneusement** : ils seront nécessaires pour toutes vos requêtes API.

## Étape 3 : configurer un environnement dans Google Colab

Pour exécuter vos requêtes API en Python, Google Colab offre un environnement pratique :

### Installer les bibliothèques requises
Dans Google Colab, exécutez la commande suivante pour installer `tweepy`, une bibliothèque Python permettant d'interagir avec l'API Twitter.
   ```python
   !pip install tweepy
   ```
### Configurer les Clés d'API : ajoutez vos clés d'API et jetons de sécurité dans votre code Colab 
```python
import tweepy
# Ajouter vos clés
api_key = 'VOTRE_API_KEY'
api_key_secret = 'VOTRE_API_SECRET'
access_token = 'VOTRE_ACCESS_TOKEN'
access_token_secret = 'VOTRE_ACCESS_TOKEN_SECRET'
# Authentification
auth = tweepy.OAuthHandler(api_key, api_key_secret)
auth.set_access_token(access_token, access_token_secret)
api = tweepy.API(auth)
```
### Récupération de données avec l'API
Exemple de recherche de tweets

```python
for tweet in tweepy.Cursor(api.search_tweets, q="votre mot-clé", lang="fr").items(100):
    print(tweet.text)
```
Ce code extrait les tweets contenant un mot-clé donné et les affiche dans la console.

### Analyse des résultats
Les données extraites peuvent ensuite être analysées pour effectuer des opérations de text mining, telles que l'analyse de sentiment ou la modélisation de sujets.
