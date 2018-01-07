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

- [x] Fork (dans l'interface graphique de github)

- [x] ```git clone git@github.com:camptocamp//"[nomDuClient]".git [nomDuDossier]```

- [x] ```git remote add Tonow-c2c git@github.com:Tonow-c2c/"[nomDuClient]".git```

> exemple git remote -vv
* Tonow-c2c	git@github.com:Tonow-c2c/"[nomDuClient]".git (fetch)
* Tonow-c2c	git@github.com:Tonow-c2c/"[nomDuClient]".git (push)
* origin	git@github.com:camptocamp/"[nomDuClient]".git (fetch)
* origin	git@github.com:camptocamp/"[nomDuClient]".git (push)

- [x] ```git fetch --all```

- [x] ```git pull```

- [x] ```git checkout -b [nomDeLaBarnche]```

- [x] ```git submodule sync; init; update```

- [x] ```docker-compose pull```

- [x] ```docker-compose build```

- [x] ```docker-compose run --rm -p 8069:8069 odoo odoo --workers=0```

----



###### Recuperation projet

> Fork

- [x] ```git clone ...```

- [x]
 - ```git remote Tonow-c2c git@git...Tonow-c2c..```
 -  ```origin    git@git...origin..```


- [x] ```git submodule sync```

- [x] ```git submodule init```

- [x] ```git submodule update```

- [x] ```docker-compose pull```

- [x] ```docker-compose build```

- [x] ```docker-compose run --rm -p 8069:8069 odoo odoo --workers=0```

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
