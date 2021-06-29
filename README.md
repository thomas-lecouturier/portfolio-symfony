# Portfolio en Symfony

## BACK OFFICE

* Création de la BDD et du .env.local

* Création des Entitées Skills / Formations / Réferences / Medias
* Création des Repository Skills / Formations / Réferences

* Création de EntityListener / MediaListener pour téléchargé les fichiers images

* Création du HomeController / SkillController / FormationController / ReferencesController

* Création de home.html.twig / manage.html.twig + create.html.twig + update.html.twig des controlleurs skills/formation/references

* Création du formulaire d'ajout d'un Skills / Formations / Réferences / Medias
* Création de la vue des formulaires

* Ajout d'une image dans le formulaire de création d'une référence avec possibilitée de téléchargé une image depuis ses fichiers locaux

## FRONT OFFICE

* composer require symfony/webpack-encore-bundle
* ajout theme bootstrap dans twig.yaml
* npm install
* npm i --save-dev bootstrap @fortawesome/fontawesome-free jquery popper.js node-sass sass-loader
* npm run watch pour compiler webpack
* configuration webpack.config.js
* configuration assets/app.js + app.scss

* app.js : Ajout d'une image dans le formulaire de création d'une référence avec possibilitée de téléchargé une image depuis ses fichiers locaux

* Création d'un dossier uploads pour accueillir les images téléchargées, dans public avec un fichier .gitignore * 

* Ajouter le chemin public uploads dans services.yaml parameters puis les binder dans services
  * ajouter App\EntityListener\:
    * resource: '../src/EntityListener'
      * tags: ['doctrine.orm.entity_listener']

* composer require uid

* Création d'une API pour récupérer les skills / formations / references sur la page d'accueil (sérializer les groups : GET)
* Dans app.js boucler sur les formations / skills / references pour faire appel à l'API et récupérer les données
npm i --save-dev moment

* Sécurisé l'acces aux donnees 
* Creer un utilisateur admin qui sera le seul autorisé à axceder aux routes pour creer ajouter ou supprimer un skill/reference/formation/media
* Créer une authentification pour se connecter avec admin
