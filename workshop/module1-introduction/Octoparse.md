---
layout: default
title: "Octoparse"
parent: "Outils sans codage"
grand_parent: "Introduction et scraping de données"
ancestor: "Traitements du langage et Social media"
nav_order: 3
---

# Octoparse 

**Octoparse** est une solution puissante et sans code pour le scraping de données. Il permet de configurer des projets de scraping de manière visuelle, sans avoir à coder. Octoparse est disponible en plusieurs langues, dont le français, et offre des fonctionnalités avancées telles que le scraping de sites dynamiques, la gestion de la pagination, et l'exportation de données au format CSV ou JSON.

## Installation et inscription

### Étapes d'installation :

1. **Inscription** :
   - Rendez-vous sur le site [Octoparse](https://www.octoparse.fr){:target="_blank"} et créez un compte gratuit.
   - L'interface est disponible en français, facilitant la prise en main.

![Octoparse](../../assets/images/workshop/octoparse1.png) 

2. **Télécharger Octoparse** :
   - Octoparse propose une application de bureau pour Windows et macOS. [Téléchargez](https://www.octoparse.fr/download){:target="_blank"} et installez l'application sur votre ordinateur.

   ![Octoparse](../../assets/images/workshop/octoparse2.png) 

   ![Octoparse](../../assets/images/workshop/octoparse3.png)
---

Octoparse, en plus d'offrir une version gratuite avec des fonctionnalités "acceptables" propose des réductions pour les étudiants, chercheurs, et organisations à but non lucratif. Ils accordent notamment une remise de 15 % sur le plan mensuel, 20 % sur le plan trimestriel, et 30 % sur le plan annuel pour les utilisateurs du secteur éducatif.

De plus, vous pouvez bénéficier d'une réduction allant jusqu'à 50 % si vous acceptez de mentionner le logiciel Octoparse dans votre article.

[Lire ici pour en savoir plus sur les reductions](https://helpcenter.octoparse.com/fr/articles/6471124-demandez-une-reduction-pour-l-education-l-exposition-ou-les-organisations-a-but-non-lucratif){:target="_blank"}

## Utilisation 

Octoparse propose une large gamme de tutoriels ainsi qu'un guide complet pour débutants, disponibles gratuitement en consultation 


### [Bienvenue sur Octoparse!](https://helpcenter.octoparse.com/fr/articles/6470918-bienvenue-sur-octoparse){:target="_blank"}

### [Découvrir Octoparse](https://helpcenter.octoparse.com/fr/articles/6470919-lecon-0-decouvrir-octoparse){:target="_blank"}

### [Démarrer par l'auto-détection](https://helpcenter.octoparse.com/fr/articles/6470921-lecon-1-demarrer-par-l-auto-detection){:target="_blank"}

### [Optimiser votre tâche](https://helpcenter.octoparse.com/fr/articles/6470922-lecon-2-optimiser-votre-tache){:target="_blank"}

### [Affiner les données](https://helpcenter.octoparse.com/fr/articles/6470923-lecon-3-affiner-les-donnees){:target="_blank"}

### [Tester votre tâche](https://helpcenter.octoparse.com/fr/articles/6470924-lecon-4-tester-votre-tache){:target="_blank"}

### [Récupérer les données](https://helpcenter.octoparse.com/fr/articles/6470925-lecon-5-recuperer-les-donnees){:target="_blank"}

### [Planifier des exécution régulières](https://helpcenter.octoparse.com/fr/articles/6470926-lecon-6-planifier-des-execution-regulieres){:target="_blank"}

### [Allez-y! Créez votre première tâche!](https://helpcenter.octoparse.com/fr/articles/6470927-lecon-7-allez-y-creez-votre-premiere-tache){:target="_blank"}

---

 ![Octoparse](../../assets/images/workshop/octoparse4.png)

## Exercice pratique

### Objectif

Utiliser Octoparse pour extraire des titres et des dates d'un site d'actualités.

### Étapes

1. **Installer Octoparse** et créer un compte gratuit.
2. **entrer l'URL du site à scraper** : https://burkina24.com/category/actualite/politique/#google_vignette 

 ![Octoparse](../../assets/images/workshop/octoparse5.png)

3. **Sélection des éléments** : veuillez patienter pendant le chargement et permettre à Octoparse d'effectuer l'auto-détection 

 ![Octoparse](../../assets/images/workshop/octoparse6.png)

 Créez le flux de travail en cliquant sur le bouton. En attendant, pour fermer les fenêtres publicitaires ou autres pop-ups, activez temporairement la navigation
4. **Configurer la pagination** pour extraire plusieurs pages.

Une fois les tests effectués (pagination, liens, etc.), vous avez la possibilité de modifier les noms des champs. Pour cet exercice, nous limiterons le nombre de répétitions de la boucle à 10.

![Octoparse](../../assets/images/workshop/octoparse7.png)

5. **Lancer le scraping** et collecter les données.

![Octoparse](../../assets/images/workshop/octoparse8.png)

![Octoparse](../../assets/images/workshop/octoparse9.png)

![Octoparse](../../assets/images/workshop/octoparse10.png)

6. **Exporter les données** au format CSV

![Octoparse](../../assets/images/workshop/octoparse11.png)

7. **Vérifier les données** dans un tableur.

![Octoparse](../../assets/images/workshop/octoparse12.png)

---

## Conclusion
Maintenant que vous maîtrisez les bases, explorez les différents modèles prêts à l'emploi et testez-les en fonction de vos besoins. 
Octoparse est une alternative puissante et facile à utiliser. Il dispose de modèles préconfigurés capables d'extraire des données de presque tous les sites web (généralement dans les versions payantes), allant de Twitter à YouTube, Amazon, et même TikTok, entre autres. Cependant, gardez à l'esprit que l'accès à certains d'entre eux est réservé aux utilisateurs premium, car les API des plateformes, où les données doivent être récupérées, ne sont pas gratuites. Par exemple, avant l'ère Elon Musk, Twitter offrait un accès public relativement large, mais ce n'est plus le cas et l'accès à l'API est désormais très coûteux. Avec son interface graphique intuitive et sa prise en charge du scraping de sites dynamiques, il s'agit d'une excellente option pour les utilisateurs sans expérience en programmation.

---