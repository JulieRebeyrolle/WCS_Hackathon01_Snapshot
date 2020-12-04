# Projet réalisé dans le cadre d'un hackathon à la Wild Code School du 19 au 20 novembre 2020

## Thème du hackathon 
"Back to the future" : Développer une application qui aurait pu être d'une grande utilité aux contemporains d'une époque historique avec une contrainte technique : consommer au moins une API

## Notre projet : 
https://hattersgonnahat.fr/snapshot/index

Snapshot, un générateur de shooter qui remplace les alcools interdits pendant la dure période de la Prohibition par des alcools de contrebande ou des ingrédients alternatifs. 

Afin de ne pas se faire prendre par la police qui veille au grain, la recette ne sera visible que pendant 20 secondes, vous serez ensuite redirigés vers le site du fameux chapelier 'Hatters Gonna Hat", car à cette époque, c'est bien connu, les gens qui portent des chapeaux sont des gens biens, cela permettra donc de lever tout soupçon sur votre personne. Cliquer sur n'importe quel lien vous ramènera bien sur vers Snapshot.

Nous avons également prévu un bouton d'urgence qui vous redirigera instantanément si d'aventure un représentant de l'autorité faisait soudainement irruption derrière vous. 

Vous pourrez également contacter l'administrateur du site afin d'être mis en relation avec un contrebandier de votre secteur. 

Petit bonus, pour vous soutenir moralement en ces temps difficiles, nous avons fait le choix d'ajouter une phrase inspirante à chaque recette.

Coté technique, pour générer les recettes, nous avons utilisé l'API "TheCocktailDB" en remplacant 5 alcools communs par des alias de contrebande, puis les autres alcools par des ingrédients aléatoires. Les phrases inspirantes quant à elles viennent de l'API "Forismatic".






# Simple MVC

## Description

This repository is a simple PHP MVC structure from scratch.

It uses some cool vendors/libraries such as Twig and Grumphp.
For this one, just a simple example where users can choose one of their databases and see tables in it.

### Prerequisites

Use this template repository to a new Github repository in WildCodeSchool organization following this exemple :
`<campus>-<langage>-<YYMM>-<type>-<name>` as **bordeaux-php-1903-project2-servyy**

### Check on Travis

1. Go on [https://travis-ci.com](https://travis-ci.com).
2. Sign up if you don't have account,
3. Look for your project in search bar on the left,
4. As soon as your repository have a `.travis.yml` in root folder, Travis should detect it and run test.
5. Configure Travis as described in the screenshot below, this is needed to avoid performance issues.

> You can watch this screenshot to see minimum mandatory configuration : ![basic config](http://images.innoveduc.fr/symfony4/travis-config.png)



### Configure you repository - Settings options

1. Add your students team as contributor .
2. Disallow both on 'dev' and 'master' branches your students writing credentials. 
3. Disallow merge available while one approbation is not submitted on PR.

> You can watch this very tiny short video : (Loom : verrouillage branches GitHub)[https://www.loom.com/share/ad0c641d0b9447be9e40fa38a499953b]


## Steps

1. Clone the repo from Github.
2. Run `composer install`.
3. Create *config/db.php* from *config/db.php.dist* file and add your DB parameters. Don't delete the *.dist* file, it must be kept.
```php
define('APP_DB_HOST', 'your_db_host');
define('APP_DB_NAME', 'your_db_name');
define('APP_DB_USER', 'your_db_user_wich_is_not_root');
define('APP_DB_PWD', 'your_db_password');
```
4. Import `simple-mvc.sql` in your SQL server,
5. Run the internal PHP webserver with `php -S localhost:8000 -t public/`. The option `-t` with `public` as parameter means your localhost will target the `/public` folder.
6. Go to `localhost:8000` with your favorite browser.
7. From this starter kit, create your own web application.

### Windows Users

If you develop on Windows, you should edit you git configuration to change your end of line rules with this command :

`git config --global core.autocrlf true`

## URLs availables

* Home page at [localhost:8000/](localhost:8000/)
* Items list at [localhost:8000/item/index](localhost:8000/item/index)
* Item details [localhost:8000/item/index/show/:id](localhost:8000/item/show/2)
* Item edit [localhost:8000/item/index/edit/:id](localhost:8000/item/edit/2)
* Item add [localhost:8000/item/index/add](localhost:8000/item/add)
* Item deletion [localhost:8000/item/index/delete/:id](localhost:8000/item/delete/2)

## How does URL routing work ?

![Simple MVC.png](https://raw.githubusercontent.com/WildCodeSchool/simple-mvc/master/Simple%20-%20MVC.png)
