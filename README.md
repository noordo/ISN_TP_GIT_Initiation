# ISN_TP_GIT_Initiation
=======================

## TP d'initiation à la pratique de GIT


### Fork et clonage du projet

* Vous vous êtes mis par groupe de deux et vous avez chacun créé un compte sur GitHub (nous désignerons par noordoXXX et noordoYYY vos identifiants respectifs dans ce qui suit).
* Dupliquez (*fork*) le projet ISN_TP_GIT_Initiation dans votre espace public.
* Récupérez sur votre disque dur les sources du projet.

        git clone https://github.com/noordoXXX/ISN_TP_GIT_Initiation.git

### Ajout d'une référence pour désigner le dépôt officiel du projet

* Vérifier qu'une référence (origin) existe  pour désigner le dépôt à partir duquel vous avez cloné le projet :

        git remote -v
        
* Définissez une nouvelle référence (depot-officiel) pour désigner le dépôt officiel :

        cd ISN_TP_GIT_Initiation
        git remote add depot-officiel https://github.com/noordo/ISN_TP_GIT_Initiation.git

* Vérifiez l'ajout de la nouvelle référence à la liste des références de dépôts distants :

        git remote -v

### Création d'une révision du fichier README.md dans une nouvelle branche

En informatique, une révision représente l'instance d'un fichier à un moment donné.
        
* Dans le dossier ISN_TP_GIT_Initiation de votre disque dur où a été cloné ce fichier, ajoutez à la fin les initiales et l'identifiant GitHub de **l'un** des 2 membres du groupe (par exemple noordoXXX). La ligne doit commencer par une étoile. Corrigez la liste pour que la dernière ligne se termine par un point et les autres par des virgules.

* Pour faire une révision du projet dans une nouvelle branche de développement du projet :

  * déplacez le pointeur HEAD (indiquant la branche courante) sur une nouvelle branche de développement (devNoordoXXX) avec la commande :
  
          git checkout -b devNoordoXXX

  * ajoutez le fichier README.me à la liste des fichiers qui seront dans le prochain "commit" :
        
          git add README.md

  * effectuez un "commit" avec le commentaire suivant "Ajout du pseudo de noordoXXX" :
        
          git commit -m "Ajout du pseudo de noordoXXX"

* Publiez la révision dans votre espace public :

        git push origin devNoordoXXX

### Création d'une seconde révision du fichier README.md dans une autre branche
        
* Placez le pointeur HEAD (indiquant la branche courante) sur la branche master :

        git checkout master

* Constatez dans le fichier README.md du dossier ISN_TP_GIT_Initiation de votre disque dur que vous retrouvez l'état initial.

* Pour faire une seconde révision du projet relative au binôme noordoYYY, ajoutez ses initiales et son identifiant GitHub comme vous l'avez fait pour noordoXXX :

* ... puis procédez de manière analogue à ce qui a été fait la première fois :

        git checkout -b devNoordoYYY
        git add README.md
        git commit -m "Ajout du pseudo de noordoYYY"

* Vérifiez l'état des branches avec la commande :

        git show-branch
        
* Visualisez ce qui a été fait jusqu'à présent avec la commande :

        gitk

### Intégration des branches individuelles de développement dans une branche de développement du groupe
        
* On souhaite fusionner les branches devNoordoXXX et devNoordoYYY dans une nouvelle branche (devGROUPE) d'intégration des développements des 2 membres du groupe. Pour cela :

  * commencez par intégrer devNoordoXXX à devGROUPE :

          git checkout master
          git checkout -b devGROUPE
          git merge devNoordoXXX
        
  * puis, essayez d'intégrer la seconde branche à devGROUPE :

          git merge devNoordoYYY

  * Réglez le conflit constaté en éditant le fichier README.md. Modifiez la mise en page de la liste conformément à vos attentes. 
  
  * Puis déclarez que le conflit est réglé, via les commandes :

          git add README.md
          git commit

* Publiez l'ensemble des révisions dans votre espace public :

          git push origin devGROUPE

* Allez constatez les changements sur GitHub.

### Soumission des modifications du fork à l'administrateur du dépôt officiel
        
* Dans GitHub faites, une demande d'intégration (*pull request*) et patientez.

### Et pour finir...

* Supposons maintenant que la maintenance de la branche officielle ne soit plus assurée et que vous décidiez de prendre la relève. Récupérez la dernière version officielle :
 
        git pull depot-officiel master

* Récupérez la demande d'intégration d'un de vos collègues (noordoZZZ) :

        git pull https://github.com/noordoZZZ/ISN_TP_GIT_Initiation.git nomdesabranche

* Réglez le conflit. Mettez à jour votre branche maître. Publiez.

## Des liens intéressants
-------------------------

* [La documentation officielle de Git (en anglais)](https://git-scm.com/book/en/v2) et [sa version traduite en français](https://git-scm.com/book/fr/v2).
* [Un simulateur pour comprendre les commandes principales de Git](https://onlywei.github.io/explain-git-with-d3/).
* [Un résumé interactif des commandes.](http://ndpsoftware.com/git-cheatsheet.html#loc=workspace)
* [Tutoriel sur Git de w3ii.com](http://www.w3ii.com/en-US/git/git_quick_guide.html) et [sa traduction](http://www.w3ii.com/fr/git/git_quick_guide.html).
* [Tutoriel sur Git sous Dokuwiki.](http://anne.pacalet.fr/Notes/doku.php?id=notes:0106_git)
* [L'aide de GitHub.](https://help.github.com/)

## Liste des élèves de TS ayant réussi ce TP
--------------------------------------------

* GM alias noordo.
