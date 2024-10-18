---
layout: default
title: "Considérations éthiques et légales"
nav_order: 5
parent: "Traitements du langage et Social media"
has_children: true
---

# Considérations éthiques et légales

L'analyse de données, notamment à partir de sources en ligne et de réseaux sociaux, soulève des questions éthiques et légales essentielles qui doivent être prises en compte pour garantir le respect des droits des utilisateurs et des normes en matière de confidentialité et de sécurité.

## Respect de la vie privée et confidentialité des données
Lors de la collecte et de l’analyse de données, il est primordial de respecter la vie privée des utilisateurs. Cela signifie :
- **Minimiser la collecte** de données personnelles, en s’assurant que seules les informations strictement nécessaires à l’analyse sont collectées.
- **Anonymisation des données** : lorsque les données personnelles sont inévitables, elles doivent être anonymisées ou pseudonymisées pour garantir la confidentialité des individus.
- **Consentement implicite ou explicite** : s'assurer, dans la mesure du possible, que les informations publiquement accessibles ne sont pas utilisées en dehors de leur contexte d'origine.

## Conformité aux réglementations sur la protection des données
Les réglementations en matière de protection des données, comme le RGPD en Europe, imposent des restrictions sur la manière dont les données personnelles peuvent être collectées, stockées et traitées. Il est essentiel de :
- **Identifier les obligations légales** applicables au projet, en fonction du pays et du type de données collectées.
- **Obtenir des autorisations** ou licences d'utilisation, lorsque nécessaire, notamment lors de l’utilisation d’API de plateformes pour la collecte de données.

### Lois et réglementations importantes :
   - **GDPR (Règlement Général sur la Protection des Données)** : applicable dans l'UE, le GDPR régit la collecte et le traitement des données personnelles, en mettant l'accent sur le consentement et la transparence des utilisateurs. Texte complet : [GDPR](https://eur-lex.europa.eu/eli/reg/2016/679/oj?eliuri=eli%3Areg%3A2016%3A679%3Aoj&locale=fr){:target="_blank"}
   - **CCPA (California Consumer Privacy Act)** : applicable en Californie, USA, le CCPA encadre les droits des consommateurs en matière d'accès, de suppression et de partage des données. Détails : [CCPA](https://oag.ca.gov/privacy/ccpa){:target="_blank"}
   - **LGPD (Lei Geral de Proteção de Dados)** : L'équivalent brésilien du GDPR, régissant la collecte et le traitement des données des citoyens brésiliens. Texte officiel : [LGPD](https://www.in.gov.br/web/dou/-/lei-n-13.709-de-14-de-agosto-de-2018-172198735){:target="_blank"}
   - **Au Mali** : 

        - Loi [N°2017-070 du 18 DEC 2017](https://www.apdp.ml/en/loi-ndeg2017-070-du-18-dec-2017-portant-modificatiion-de-la-loi-ndeg-2013-015-du-21-mai-2013){:target="_blank"} portant modificatiion de la loi n° 2013-015 du 21 mai 2013 portant protection des Données à Caractère Personnel en République du Mali 
        - [Autorité de Protection des Données à Caractère Personnel](https://www.apdp.ml/){:target="_blank"} 

### Considérations pour un cadre juridique inclusif
Les réglementations en vigueur, souvent issues des pays de l'UE, des États-Unis et d'autres pays développés, reflètent des perspectives occidentales sur la confidentialité et la sécurité des données. Cependant, ces normes peuvent parfois ne pas tenir compte des dynamiques culturelles et des contextes uniques d'autres régions, notamment en Afrique et en Asie. Ce déséquilibre soulève des questions quant à la manière dont les utilisateurs de cultures différentes perçoivent et interagissent avec ces réglementations.

Dans le cadre du projet **Décoloniser la sécurité comportementale de l’information** ([en savoir plus](https://mkante.ml/en_US/decolonising-bis/){:target="_blank"}), nous explorons comment les normes sociales influencent les attitudes envers la confidentialité en ligne dans trois contextes culturels distincts : la Tanzanie, le Mali et la Suède. Avec l'accélération de la transformation numérique, comprendre comment les contextes culturels façonnent les comportements et les attitudes des individus envers la confidentialité est essentiel pour le développement de pratiques de sécurité de l'information plus efficaces et inclusives.

L’objectif de cette recherche est de mettre en évidence les façons dont les normes sociales influencent les perceptions et les actions liées à la confidentialité en ligne dans ces différents environnements. En comparant les expériences et attitudes en Tanzanie, au Mali, et en Suède, le projet vise à identifier les facteurs universels et spécifiques à chaque région qui influencent la confidentialité en ligne. Cette approche pourrait apporter des contributions significatives aux lois et politiques internationales, afin qu'elles prennent davantage en compte les perspectives africaines et d'autres régions sous-représentées. 

En bref, ce n’est pas le sujet principal ici, mais je tenais à faire cette parenthèse pour illustrer comment ces dynamiques se rejoignent et surtout montrer la convergence entre **recherche technique (systèmes d’information) et sciences sociales...**

## Respect des conditions d’utilisation des plateformes
De nombreuses plateformes (Twitter, Facebook, etc.) imposent des restrictions dans leurs conditions d’utilisation quant à la collecte automatisée de données via des outils de scraping ou des API. Afin de respecter ces règles :
- **Vérifier les conditions d’utilisation** de chaque plateforme pour s’assurer que les pratiques de collecte de données sont conformes.
- **Limiter la fréquence des requêtes** et ne pas contourner les restrictions en matière d’accès pour éviter de surcharger les serveurs ou de violer les termes de service.

### Règles spécifiques des plateformes sociales :
   - **Twitter** : [politique et accord de développement Twitter](https://developer.twitter.com/en/developer-terms/agreement-and-policy){:target="_blank"}
   - **Facebook** : [politique de la plateforme Facebook](https://developers.facebook.com/policy){:target="_blank"}
   - **Instagram** : utilise les termes de la plateforme Facebook, [API Instagram Graph](https://developers.facebook.com/docs/instagram-api){:target="_blank"}
   - **LinkedIn** : politique stricte contre le scraping. [Conditions d'utilisation de LinkedIn](https://www.linkedin.com/legal/user-agreement){:target="_blank"}
   - **Reddit** : [conditions d'utilisation de l'API de Reddit](https://www.redditinc.com/policies/data-api-terms){:target="_blank"}

## Utilisation responsable des données collectées
Les données doivent être analysées et interprétées de manière à éviter les biais, les manipulations ou les conclusions incorrectes. Cela inclut :
- **Éviter la manipulation des données** qui pourrait induire en erreur ou créer des conclusions fausses ou partiales.
- **Préserver la neutralité et l'objectivité** dans l’analyse, en étant transparent quant aux limites et aux biais potentiels de l’étude.

## Transparence et communication des résultats
Dans une optique de transparence, il est conseillé de :
- **Documenter les processus de collecte et d’analyse** pour rendre compte des méthodologies utilisées.
- **Communiquer ouvertement les résultats** de l’étude, en précisant les biais ou limitations identifiés, afin que les utilisateurs et parties prenantes puissent interpréter les résultats de manière éclairée.

---

### Ressources académiques et directives éthiques
   - **CFAA (Computer Fraud and Abuse Act)** – USA : régit l'accès non autorisé aux systèmes informatiques. Informations : [CFAA](https://www.law.cornell.edu/uscode/text/18/1030){:target="_blank"}
   - **The Menlo report** : guide éthique pour la recherche numérique en sciences sociales, couvrant la confidentialité, le consentement éclairé et l’atténuation des risques. [The Menlo report](https://www.caida.org/publications/papers/2012/menlo_report_actual_formatted/){:target="_blank"}

Ces considérations éthiques et légales doivent guider chaque étape de la collecte, de l'analyse, et de l'interprétation des données pour garantir le respect des individus et des réglementations en vigueur.
