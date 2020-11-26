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


