###### Instalation

* Mac et Windows
Telecharger [ici](https://git-scm.com/downloads) et suivre l'instalation

* Linux ```sudo apt-get install git```

* Création du compte [Github](https://github.com/)

* *- faclultatif* pour ceux qui veulent ce connecter par la suite en SSH voici le [lien](https://help.github.com/articles/connecting-to-github-with-ssh/)

----


###### Création d'un repo si aucun existant

* Initialisation d'un repository dans le dossier souhaité

```git init```

* si SSH ajout du lien vers le repo souhaité
```git remote add origin git@github.com:[User]/[Nom_repo].git```

* si https ajout du lien vers le repo souhaité
```git remote add origin https://github.com/[User]/[Nom_repo].git```

-----


###### Iteration a chaque modification

* Ajout des fichiers souhaités dans le repository

```git add [le_nom_du_fichier]```

* une fois l'ensemble des fichiers souhaité ajouter création du commit

```git commit -m "[le message décrivant le commit]"```

* pousser vers le repository souhaité

```git push```

----



###### Pull Request

- [x] ![Fork dans l'interface graphique de github](https://github.com/Tonow/GL-Test-CI/blob/master/Capture%20d'%C3%A9cran%20de%202018-01-07%2020-49-43.png)

- [x] ```git clone 	git@github.com:Tonow/GL-Test-CI.git```

- [x] ```git remote add [votre-nom-github] 	git@github.com:[votre-nom-github]/GL-Test-CI.git".git```

> exemple git remote -vv
* [votre-nom-github]	git@github.com:[votre-nom-github]/GL-Test-CI.git".git (fetch)
* [votre-nom-github] git@github.com:[votre-nom-github]/GL-Test-CI.git".git (push)
* origin	git@github.com:Tonow/GL-Test-CI.git".git (fetch)
* origin	git@github.com:Tonow/GL-Test-CI.git".git (push)

- [x] ```git fetch --all```

- [x] ```git pull```

- [x] ```git checkout -b [nomDeLaBarnche]```

----


###### fusionner les commit
[lien ohshitgit](http://ohshitgit.com/)

- si deja commit:
 * ```git log -5```
 * ```git rebase -i [hash d'un commit sain] ```
 * - squash [les commit a fusionner]
 * - choix du message du commit
 - ```git push -f```


- pas encore commit:

```git commit --amend```

----



###### Run docker-compose

* Toute une Release

    ```docker-compose run --rm -e MARABUNTA_FORCE_VERSION=10.0.20 -p 8069:8069 odoo odoo --workers=0```

* Juste un module

    ```docker-compose run --rm -p 8069:8069 odoo odoo --workers=0 -u enfinfidu_payroll```

* drop la DB

    ```docker-compose run --rm odoo dropdb odoodb```

-----
