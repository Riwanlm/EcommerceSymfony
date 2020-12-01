# Installation d'un projet symfony

## Création d'un nouveau projet : 
symfony new my_project_name --full

## Intégration de Bootstrap :
Ajout du dossier CSS & JS de bootstrap dans le dossier public/assets + copie du tamplate du code dans base.html.twig 

## Création d'un controller avec le terminal :
symfony console make:controller

## Création de l'entité Utilisateur avec : 
symfony console make:user

## Création de la base de donnée : 
Modifier dans le .env la DATABASE_URL 
& 
créer la BDD via doctrine :
symfony console doctrine:database:create
&
Générer le fichier SQL migration :
symfony console make:migration
&
Exécuter la migration vers la BDD :
symfony console doctrine:migration:migrate

## Formulaire d'inscription : 
Création du Controller RegisterController 
&
Création du formulaire avec : symfony console make:form
+ Ajout des différents champs dans Entity User (make:entity) puis dans RegisterType.

## Sauvegarde des données en BDD pour la création d'un new User :
- Création de la public function __construct() & validation des données dans RegisterController (New object User, vérification & validation, persistance des données et flush en BDD).

## Hachage des MDP en BDD avec :
- UserPasswordEncoderInterface & utilisation de la variable $password.

## Ajout de contrainte de validation : 
- Dans RegisterType avec 'constraints'

## Passer les messages d'erreurs en anglais par défaut en fr :
Aller dans : config > packages > translation.yaml & changer le "default_locale" en fr.

## Création de la page de connexion : 
Utiliser la commande : symfony console make:auth -> permet de générer le fomulaire de connexion ainsi que de générer les routes 'login' et 'logout'.

#### Pour voir toutes les routes de l'application : 
symfony console debug:router

## Création de l'espace membre utilisateur (/compte) : 
symfony console make:controller --> AccountController