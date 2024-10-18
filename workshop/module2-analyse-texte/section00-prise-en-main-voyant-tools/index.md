---
layout: default
title: "Overview Voyant-Tools"
parent: "Outils"
grand_parent: "Analyse textuelle"
nav_order: 2
---

# Overview de voyant tools

**Voyant Tools** est une application web open-source dédiée à l'analyse et à la visualisation de textes, accessible en ligne sans installation à l’adresse [voyant-tools.org](https://voyant-tools.org/?lang=fr){:target="_blank"}. Cet outil intuitif est particulièrement apprécié dans le domaine des sciences sociales pour l'analyse exploratoire de corpus de textes.

## Fonctionnalités principales
- **Visualisation des fréquences de mots** : l'outils génère automatiquement des nuages de mots et des graphiques, facilitant l’identification des mots les plus courants dans un corpus.
- **Distribution des termes** : analyse la répartition de termes spécifiques dans l'ensemble du corpus, permettant de visualiser où et comment certains mots apparaissent.
- **Contextualisation des termes** : la fonction de concordance aide à étudier le contexte d'apparition des mots dans le corpus, ce qui peut enrichir l'interprétation du texte.

## Points forts
- **Interface graphique intuitive** : simple d'utilisation, c'est accessible aux utilisateurs sans connaissances préalables en programmation.
- **Multilingue** : prend en charge plusieurs langues, y compris le français, ce qui le rend idéal pour les utilisateurs francophones.
- **Utilisation Flexible** : il peut être utilisé pour l'analyse de textes divers, allant des articles de recherche aux textes littéraires et corpus de médias sociaux.

Voyant Tools constitue un excellent complément à **Orange Data Mining** pour ceux qui souhaitent explorer des données textuelles sans programmation, tout en accédant à des visualisations avancées pour enrichir leur analyse.

# Utilisation du serveur local de voyant tools

Voyant Tools offre une option pour exécuter une instance autonome sur votre machine locale, appelée **Voyant Server**. Cela permet aux utilisateurs de bénéficier de Voyant Tools avec des avantages spécifiques par rapport à la version hébergée en ligne.

## Avantages du serveur local
Lancer l'outils en local offre plusieurs avantages :
- **Performance** : accélère l’analyse en réduisant la latence, car les traitements s'effectuent directement sur votre machine.
- **Sécurité et confidentialité** : les données analysées ne quittent pas votre ordinateur, ce qui est essentiel pour des documents sensibles ou confidentiels.
- **Fiabilité** : évite les interruptions de service liées à l’hébergement en ligne, garantissant une continuité d’utilisation même sans connexion Internet.

## Installation et démarrage du serveur local
Ce n'est pas trop technique l'installation donc tentons ensemble. Suivez ces étapes :

### Java
Le serveur nécessite l'installation d'une version spécifique de Java: **11**. Si vous avez plusieurs versions de Java installées, vous devez vous assurer que la version 11 est activée. Java 11 peut être téléchargé à partir des emplacements suivants (selon votre systeme d'exploitation Windows, MacOS, Linux...):
- [Adoptium](https://adoptium.net/fr/temurin/releases/?version=11){:target="_blank"}

![VT](/assets/images/workshop/voyant-tool/vt3.png) 

![VT](/assets/images/workshop/voyant-tool/vt4.png) 

- [Oracle](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html){:target="_blank"}

### Télécharger voyant server
Récupérez le Zip (qui contient le fichier JAR) depuis le dépôt GitHub de Voyant Tools : 

[VoyantServer GitHub](https://github.com/voyanttools/VoyantServer/releases/latest){:target="_blank"}.

![VT](/assets/images/workshop/voyant-tool/vt2.png) 

Décompressez le fichier (assurez-vous d'extraire réellement le contenu dans un vrai répertoire) et double-cliquez sur le fichier VoyantServer.jar (sur Mac, vous devrez peut-être appuyer sur Ctrl tout en cliquant sur VoyantServer.jar, sélectionner Ouvrir et confirmer l'ouverture - ceci est dû aux précautions de sécurité dans OS X). 

![VT](/assets/images/workshop/voyant-tool/vt8.png)

### Lancement
Une fois que vous avez ouvert VoyantServer.jar, une application de contrôleur apparaît (qui vous permet d'arrêter le serveur, de voir les messages d'erreur, de modifier les paramètres, etc.) et un nouveau onglet (dans votre navigateur) apparaît également avec Voyant Tools. **C'est tout!**

![VT](/assets/images/workshop/voyant-tool/vt6.png) 

![VT](/assets/images/workshop/voyant-tool/vt7.png) 

## Troubleshooting

### Version de Java
Voyant Server nécessite **Java 11** et peut ne pas fonctionner avec d'autres versions.

### Mac OS
Si vous rencontrez un message d’erreur sur Mac OS :

> The Java JAR file “VoyantServer.jar” could not be launched. Check the Console for possible error messages.

Vous pouvez ouvrir VoyantServer via le terminal comme solution de contournement en utilisant :
```bash
java -jar VoyantServer.jar
```

![VT](/assets/images/workshop/voyant-tool/vt5.png) 

Remarque : vous devez exécuter la commande ci-dessus à partir du répertoire dans lequel vous avez extrait le fichier JAR.