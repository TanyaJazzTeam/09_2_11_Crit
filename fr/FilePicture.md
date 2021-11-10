Premier en-tête | Deuxième en-tête
--- | ---
Cellule de contenu | Cellule de contenu
Cellule de contenu | Cellule de contenu

Premier en-tête | Deuxième en-tête
--- | ---
Cellule de contenu | Cellule de contenu
Cellule de contenu | Cellule de contenu

![Citadelle](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

Aligné à gauche | Aligné au centre | Aligné à droite
:-- | :-: | --:
la colonne 3 est | un texte verbeux | **1600 $**
la colonne 2 est | centré | 12 $
rayures zébrées | sont soignés | ~~$1~~

Dillinger est un éditeur HTML5 Markdown basé sur AngularJS, compatible avec les appareils mobiles, de stockage hors ligne.

- Tapez du Markdown sur la gauche
- Voir HTML à droite
- la magie

# vrai

- Importez un fichier HTML et regardez-le se convertir comme par magie en Markdown
- Glissez-déposez des images (nécessite que votre compte Dropbox soit lié)

# LIIIII
# ndpr of m worfc

Vous pouvez également:

- Importez et enregistrez des fichiers depuis GitHub, Dropbox, Google Drive et One Drive
- Faites glisser et déposez les fichiers Markdown et HTML dans Dillinger
- Exporter des documents au format Markdown, HTML et PDF

Markdown est un langage de balisage léger basé sur les conventions de formatage que les gens utilisent naturellement dans les e-mails. Comme l'écrit [John Gruber] sur le [site Markdown][df1]

> L'objectif primordial de la conception de la syntaxe de mise en forme de Markdown est de la rendre aussi lisible que possible. L'idée est qu'un document au format Markdown doit être publiable tel quel, en texte brut, sans avoir l'air d'avoir été balisé avec des balises ou des instructions de formatage.

Ce texte que vous voyez ici est en *fait* écrit en Markdown ! Pour avoir une idée de la syntaxe de Markdown, tapez du texte dans la fenêtre de gauche et regardez les résultats dans la droite.

### faux

Dillinger utilise un certain nombre de projets open source pour fonctionner correctement :

- [AngularJS] - HTML amélioré pour les applications Web !
- [Ace Editor] - éditeur de texte Web génial
- [markdown-it] - L'analyseur Markdown est bien fait. Rapide et facile à étendre.
- [Twitter Bootstrap] - excellent modèle d'interface utilisateur pour les applications Web modernes
- [node.js] - E/S événementielles pour le backend
- [Express] - framework d'application réseau node.js rapide [@tjholowaychuk]
- [Gulp] - le système de compilation en streaming
- [Breakdance](https://breakdance.github.io/breakdance/) - Convertisseur HTML en Markdown
- [jQuery] - duh

Et bien sûr, Dillinger lui-même est open source avec un [référentiel public][dill] sur GitHub.

# kfjbhdfkcjhb

### Installation

![Ilos](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

Dillinger nécessite l' [exécution de Node.js](https://nodejs.org/) v4+.

Installez les dépendances et devDependencies et démarrez le serveur.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

Pour les environnements de production...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

Dillinger est actuellement étendu avec les plugins suivants. Les instructions sur la façon de les utiliser dans votre propre application sont liées ci-dessous.

Brancher | LISEZ-MOI
--- | ---
Boîte de dépôt | [plugins/dropbox/README.md][PlDb]
GitHub | [plugins/github/README.md][PlGh]
Google Drive | [plugins/googledrive/README.md][PlGd]
OneDrive | [plugins/onedrive/README.md][PlOd]
Moyen | [plugins/support/README.md][PlMe]
Google Analytics | [plugins/googleanalytics/README.md][PlGa]

### Développement

Vous voulez contribuer ? Super!

Dillinger utilise Gulp + Webpack pour un développement rapide. Apportez une modification à votre fichier et visualisez instantanément vos mises à jour !

Ouvrez votre terminal préféré et exécutez ces commandes.

00000000000000000

Premier onglet :

```sh
$ node app
```

Deuxième onglet :

```sh
$ gulp watch
```

(facultatif) Troisième :

```sh
$ karma test
```

#### Bâtiment pour la source

Pour la sortie de production :

```sh
$ gulp build --prod
```

Génération d'archives zip pré-construites pour la distribution :

```sh
$ gulp build dist --prod
```

### Docker

Dillinger est très facile à installer et à déployer dans un conteneur Docker.

Par défaut, le Docker exposera le port 8080, modifiez-le donc dans le Dockerfile si nécessaire. Lorsque vous êtes prêt, utilisez simplement le Dockerfile pour créer l'image.

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

Cela créera l'image dillinger et tirera les dépendances nécessaires. Assurez-vous d'échanger `${package.json.version}` avec la version actuelle de Dillinger.

Une fois cela fait, exécutez l'image Docker et mappez le port sur celui que vous souhaitez sur votre hôte. Dans cet exemple, nous mappons simplement le port 8000 de l'hôte sur le port 8080 du Docker (ou tout autre port exposé dans le Dockerfile) :

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

Vérifiez le déploiement en accédant à l'adresse de votre serveur dans votre navigateur préféré.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

Voir [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)

### À faire
