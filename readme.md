Clever Garden Starter Kit
================================================================================

Ce dépôt GIT sert de kit de démarrage pour les projets d'intégration statique.

Ils contient toutes nos bonnes pratiques et tous les outils nécessaires pour
nos projets d'intégration statique chez Clever Age. Parmi tous les outils
présents dans ce kit vous trouverez ceux qui doivent être utilisés
obligatoirement aussi bien que ceux qui sont simplement recommandés.

Chaque outil utilisé dispose d'une documentation dédiée sur la façon de
l'utiliser dans notre contexte. Cette documentation est rédigée au format
Markdown et est disponible dans le répertoire `docs` de ce dépôt.


Créer un nouveau projet
--------------------------------------------------------------------------------
Pour créer un nouveau projet, suivez simplement les instructions ci-après.

## Vérifiez votre environnement
Tous nos projet pré-supposent que votre environnement dispose des outils suivant
installés au niveau global sur votre machine :

* [Git](http://git-scm.com/)
* [NodeJS](http://nodejs.org/)
* [Ruby](https://www.ruby-lang.org/fr/)
* [Rubygems](http://rubygems.org/)
* [Bundler](http://bundler.io/)
* [Grunt CLI](http://gruntjs.com/getting-started)

Dans la mesure ou vous êtes sous Mac, vous devez obligatoirement installer XCode
et les outils en ligne de commande qui l'accompagne (ce qui installera
automatiquement Ruby et Rubygems).

Il est également recommandé d'installer et d'utiliser [Homebrew](http://brew.sh/)
pour installer tous les outils en ligne de commande dont vous pourriez avoir
besoin.

## Démarrez votre projet
Vous avez deux options pour démarrer votre projet:

1. Télécharger le contenu de ce dépôt et l'utiliser comme base de démarrage
2. Cloner ce dépôt avec GIT (voir ci-après)

> *NOTE :* _Il est prévus à termes de disposer d'un script de démarrage qui
  automatisera la mise en œuvre d'un projet_

Une fois que vous aurez récupéré le contenu de ce dépôt, vous avez la possibilité d'ajouter les outils recommandés ci-après (voir section : Outils recommandés).

### Cloner le kit de démarrage avec GIT
Si vous le souhaitez, vous pouvez directement cloner ce dépôt avec GIT.
Si vous choisissez cette option, cela vous permet de garder le lien avec ce
dépôt. Ça peut être utile si vous voulez pouvoir récupérer des mises à jour de
ce starter kit après coup. *ATTENTION:* _En l'état c'est assez risqué et il est
recommandé de supprimer la branche distante liée à ce dépôt une fois que vous
avez l'avez cloné._

Le plus simple:

```bash
$ cd ~/monProjet
$ git clone git@git.clever-age.net:clever-age-expertise/clever-garden-starter-kit.git
$ git remote remove origin
```

Il ne vous reste plus qu'a ajouter une nouvelle `origin` vers le dépôt définitif
des sources du projet final et à envoyer vos source vers le dépôt définitif.
Le paramètre `-u` permet d'associer la branche locale (ici le master) avec celle distante de façon pérenne.

```bash
$ git remote add git@git.clever-age.net:client-name/project-name.git
$ git push -u origin master
```

Lorsque le dépôt est rapatrié en local, exécutez les commandes
suivantes :

```bash
$ bundle install
$ npm install
```

## Organisation des fichiers
Pour harmoniser notre travail, tous les projets utiliserons la structure de
fichiers suivante.

Les sources sur lesquelles nous travaillons sont toutes dans le répertoire `src`.
Normalement, seuls les fichiers présents dans ce répertoire devraient être
modifiés après le début du projet.

* `/src`
* `/src/sass` : L'ensemble des fichiers Sass du projet
* `/src/js`   : L'ensemble des sources JavasSript du projet
* `/src/img`  : L'ensemble des images d'interface du projet
* `/src/img/sprites` : L'ensemble des images d'interface qui seront regroupées en sprites
* `/src/font` : L'ensemble des fonts utilisées par le projet
* `/src/html` : L'ensemble des gabarits HTML du projet
* `/src/docs` : L'ensemble de la documentation statique du projet au format Markdown

A chaque fois que le projet est "construit", le résultat est disponible dans
les répertoires suivant:

* `/build`
* `/build/docs` : Toute la documentation du projet au format HTML
* `/build/dev` : Le projet construit sans optimisation pour le développement
* `/build/prod` : Le projet statique optimisé pour la livraison final


Outils obligatoires
--------------------------------------------------------------------------------
Les outils listés ici doivent êtres utilisés obligatoirement lorsqu'on démarre
un nouveau projet d'intégration. _Le seul cas ou on ne les utilisera pas sera
lorsqu'on aura une demande explicite du client pour utiliser autre chose._

* [Grunt](docs/grunt.md)
* [Sass/compass](docs/sass.md)
* [Linter](docs/linter.md)


Outils recommandés
--------------------------------------------------------------------------------
Les outils listés ci-après sont des recommandations. Il peuvent apporter des
fonctionnalités originales ou en cours d’expérimentation. Vous êtes libre de
les utiliser, ou non, selon vos envies ou votre contexte projet.

* Bower
