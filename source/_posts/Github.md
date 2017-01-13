---
title: Github
date: 2016-12-12 02:38:39
tags: [github]
categories: [technologies]
---
# GitHub


![](/images/illustrating.png)
<p>Les tendances de codage on beaucoup changer au cours du temps. Au debut de l’ere du codage, la roue avait besoin d’etre reinventee, lorsqu’une application etait developpee, la plus part des librairies et du code pour y parvenir avait besoin d’etre ecris. Pourtant a l’heure actuelle ou je suis entrain d’ecrire, beaucoup de choses on deja etees creer par d’autre codeurs autour du monde. Le challenge aujourd’hui dans beaucoup de cas (pas tous), n’est alors que d’apprendre a comprendre et a utiliser ce que d’autre personnes ont deja coder et ont mis a la disposition d’autres codeur sous la forme d’open source. Github est la plus grande plateforme aujourd’hui hebergant de l’ open source code.</p>

<p>
Github est une plateforme gratuite qui octroie a toute personne tierse enregistree sur sa plateforme d’uploaded du code, et de le tenir a jour au fil du temps en permettant des actualisations, des uploads a chaque fois qu’une modification vous semble importante.
</p>

<p><i>Par exemple, imaginez qu’avec des amis a travers le monde, vous vous mettez en tete de creer un site web. Du fait de vos distantes locations, il est difficile pour chacun de travailler ensemble. Vous pouvez utiliser un serveur git pour cela (ou github si la publication du code source de votre site web ne vous derange pas). Cela vous permettra a chacun d’avoir une version toujours a jour du code et cela meme si vous amis font des changements pele et mele, vous pourrez toujours avoir une version tres a jour du code pour vous aidez a evoluer tous ensemble. Et en plus de tout cela, vous pourrez meme retourner dans l’historique des mises a jour pour recuperer une version anterieure de votre code (c’est tres important lors de la cherche de certains bugs quelque fois).</i></p>

 
#### L’objet de cet article est d’enseigner les bases de l’utilisation de github en ce qui concerne :
* L’installation de l’outils Git
* La creation d’un depot de code (repository) github 
* Comment uploader du code sur github.



## Prerequis
 
* #### git:
	 Vous pouvez le telecharger sur le site ci dessous, mais au moment de l’installation, nous devons faire attention a installer Git aussi bien en console qu’en graphique: 
    * Selectionner les options Git Bash Here & Git GUI Here pour que ces options puissent etres ajoutees au menu explorer.
    
    ![](/images/installbash.png)

    * Selectionner l’option du milieu pour que la commande git puisse etre ajouter au a la variable d’environement PATH de sorte que nous puissions utiliser git depuis le terminal (console).
    
    ![](/images/installbash2.png)

<p>Sans plus tarder, je vais vous apprendre a creer un projet sur github, a l’uploader sur le serveur et a permettre a plusieurs partenaires de pouvoir le modifier en meme temps que vous. Accrochez vous bien ! 8).</p>

## Entrer dans le monde de github

Pour se rendre sur github il suffit de se rendre a cette adresse ci http://github.com . Pour pour pouvoir acceder a la majorite des outils que cette platforme nous procure gratuitement , Nous avons besoin de creer un compte github. [Cliquez ici pour creer votre compte github](https://github.com/join?source=header-home) et entrez toutes les informations requises.
 

## Creer un depot github

*A cet endroit, une explication s’ingere. *

**Pourquoi creer un projet github ?**
Parce qu’en fait github, agis jusqu’ici comme une hebergeur de code source. C’est a dire que github peut nous permettre d’enregistrer le code source d’une certaine application, logiciel ou meme un vulguaire texte que nous sommes en train d’ecrire et de le sauveguarder en ligne. <br/> <br/> 
*NB : comme je l’avais dit plutot github, est une plateforme qui fait uniquement dans le code source et a cose de cela a tous les droits d’effacer les fichiers musicaux ou videos, bref medias anormalement sauveguarder sur sa plateforme.*

** Pour creer un nouveau projet **, rendez vous sur la page d’acceuil de votre compte et :
	1. Appuyer sur le bouton nouveau projet.<br/>
    ![](/images/createrepo.png)
	2. Entrer les informations du projet que vous voulez creer sur la page qui s’affichera a vous. Les informations comprennent :
 + Owner : Celui a qui appartient de le projet
 + Repository name :  Le nom du projet
 + Description : Une courte description de votre projet
 + Ensuite vous devez choisir si vous voulez votre projet publique (acces ouvert a tout le monde), ou votre projet prive, c’est a dire que seulement vous et les personnes que vous aurez autoriser auront acces a voir ce projet.
    <br/>
    ![](/images/creating repo.png)
    
 + Le derniere point demande si vous aimeriez demarrer le projet actuel en creant un fichier README.md . Ce fichier permettra de procurer une page d’accueil de projet a quiconque voudra consulter votre projet sur github.** Add .gitignore ** contient la liste de fichier que vous n’aimeriez inclure dans vos commit/push. **Add a license** demande quelle license paraine vous aimeriez rattacher a votre projet. Il existe plusieur types de license qui regissent les projets, les plus utilises sont apache 2.0, mit etc... Ce license definissent les conditions d’utilisation de votre code source a d’autre essient.


## Uploader sur GitHub

Pour importer du contenu sur github, vous devez deja le posseder en local (sur votre ordinateur). 
1. Rendez vous dans le repertoire du contenu que vous compter importer
2. Faites un click droit dans le dossier et selectionner l’option * Git Bash Here *. Cela ouvrira pour vous un terminal git dans le dossier ou vous vous trouvez actuellement.
Une fois terminal ouvert, vous entrez la commande *dir* et validez. Vous verez s'afficher la liste des fichiers dans votre dossier de travail.
 *** La toute premiere fois ou vous uploadez de votre dossier vers github, nous avons besoin d'effectuer certaines taches basiques: ***
    * initialiser le dossier actuel si ceci n'est pas encore fait en entrant la commande ci dessous: 
```
$> git init
```
    * faire le lien entre le dossier local et le depot github en ligne:
 ```
$> git remote add origin https://github.com/blackgerman/ubiquitous-disco.git
```   

![](/images/firstcreatedrepo.png)
  ** Ce que nous devons savoir ici c'est que le derniere parametre, le lien pointe vers notre depot en ligne.**

3. Voici les trois pas que vous devrez poser a chaque fois que voudrez importer votre code vers votre espace github:
    * Ajouter les fichiers que vous voulez ajouter a votre git. Par exemple pour un fichier mail.doc dans votre dossier, vous ferez : 
```
$> git add mail.doc
```
Pour la plupart du temps, vous avez besoin de rajouter tous les dossiers au git ce qui se fait la commande qui stipule que tout le dossier sera pris en compte :
```
$> git add .
```

4. Faire une sauveguarde de l’etat actuel de votre projet, ce qui s’appelle faire un commit:
```
$> git commit –m "Message explicatif de la sauveguarde"
```
Le message explicatif de la sauveguarde nous permettra dans l’historique de sauveguarde de savoir quand et pourquoi est ce que des sauveguardes on etees faites. La grande force du versionnage de code est qu’ a un niveau plus avancer, Nous pourrons meme revenir a des etats de sauvegarde anterieur de l’application a notre guise.
5. Pour uploader le code source vers la plateforme, nous devons utiliser la commande
```
$> git push -u origin master
```
    + push : stipule que vous voulez effectuer un upload vers la plateforme en ligne
    + -u origin : stipule le depot de code vers lequel l’upload est effectuer
    + master :  stipule la branche vers laquelle vous faites votre upload

*Si tout se passe bien apres cette commande il vous sera demander d’entrer les informations de votre compte (nom d’utilisateur et mot de passe github).*



### A partir de votre deuxieme mise a jour du code source en ligne, vous pourrez donc vous contenter d'utiliser ces commandes pour uploader des donnees vers votre depot github.
```
$> git add .
$> git commit –m "Message explicatif de la sauveguarde"
$> git push 
```
    Cela vous permettra d'uploader la branche actuelle sur laquelle vous vous trouvez vers github.
    
<span style="color:red;font-size:16px;"> NB : Cet article discute uniquement de l’utilisation de github si vous etes le seul a travailler sur github, et si vous ne travailler que vous n’uploadez que d’une seule machine.  </span>

#### Un autre article discutera de concepts plus complexes par rapport a l’utilisation de l’outils git en general.

