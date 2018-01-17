# Cour Génie Logiciel : Test/Integration continue
## Utilisation de service de Versionning Git + Github

![Git](https://github.com/gl-tests-ci/Git_Github/blob/master/images/git-s.png)       ![Github](https://github.com/gl-tests-ci/Git_Github/blob/master/images/github-s.png)

### Installation

* [Mac](https://git-scm.com/download/mac) et [Windows](http://gitforwindows.org/)
Cliquer pour télécharger ou [de façon générale](https://git-scm.com/downloads) et suivre l'installation

* Linux ```sudo apt-get install git```

* Création du compte [Github](https://github.com/)

* *- facultatif* pour ceux qui veulent se connecter par la suite en SSH voici le [lien](https://help.github.com/articles/connecting-to-github-with-ssh/)

----
----

### Création d'un repo si aucun existant

* Initialisation d'un repository dans le dossier souhaité

```git init```

* si SSH ajout du lien vers le repo souhaité
```git remote add origin git@github.com:[User]/[Nom_repo].git```

* si https ajout du lien vers le repo souhaité
```git remote add origin https://github.com/[User]/[Nom_repo].git```

-----


### Iteration à chaque modification

* Ajout des fichiers souhaités dans le repository

```git add [le_nom_du_fichier]```

* une fois l'ensemble des fichiers ajouté, création du commit

```git commit -m "[le message décrivant le commit]"```

* pousser vers le repository

```git push [MonNom] [NomBranche]```

----


### Pull Request Workflow

#### Initialisation du repository

- [x] Fork dans l'interface graphique de github

![Fork dans l'interface graphique de github](https://github.com/gl-tests-ci/Git_Github/blob/master/images/Fork1.png)

- [x] Cloner le repository original

```git clone https://github.com/gl-tests-ci/GL-Test-CI-Calculatrice.git```

- [x] Se placer dans le bon dossier

```cd GL-Test-CI-Calculatrice```

- [x] Ajouter le chemin vers le Fork du repository qui est sur votre compte

```git remote add [votre-nom-github] 	https://github.com:[votre-nom-github]/GL-Test-CI.git".git```

> exemple après  ```git remote -vv```
* [votre-nom-github]	git@github.com:[votre-nom-github]/GL-Test-CI.git".git (fetch)
* [votre-nom-github] git@github.com:[votre-nom-github]/GL-Test-CI.git".git (push)
* origin	git@github.com:Tonow/GL-Test-CI.git".git (fetch)
* origin	git@github.com:Tonow/GL-Test-CI.git".git (push)

----

#### Mettre à jour son repository local

- [x] récupérer toutes les données de ce projet que vous ne possédez pas déjà

```git fetch --all```

- [x]  récupère généralement les données depuis le serveur qui a été initialement cloné et essaie de les fusionner dans votre branche de travail actuelle

```git pull```

- [x] Créer une branche de travail et basculer dessus

```git checkout -b [nom-de-la-branche-a-cree]```

----

#### Proposition de la pull request

- [x] une fois les modifications terminées [commiter et pousser](https://github.com/gl-tests-ci/Git_Github#iteration-a-chaque-modification) dans l'interface web de github, créer une "New pull resquest"

![New pull resquest](https://github.com/gl-tests-ci/Git_Github/blob/master/images/PR1.png)

- [x] choisir avec quelle branche on veux comparer la branche actuelle

![choix branche a comparer](https://github.com/gl-tests-ci/Git_Github/blob/master/images/PR2.png)

- [x] Entrer les informations pertinantes puis cliquer sur _Create pull request_


> - [x] 1. choisir la personne qui ont le droit de contrôler le code, proposer "Reviewers"

> - [x] si il y a des choses à changer, continuer les cycles de [commit push](https://github.com/gl-tests-ci/Git_Github#iteration-a-chaque-modification)

> - [x] 2. si il n'y a pas de conflit et que les autres personnes approuvent le changement, alors il y a possibilité de "Merger" les deux branches (fusionner celle que l'on viens de faire avec l'autre)

> ![Merger + Review PR](https://github.com/gl-tests-ci/Git_Github/blob/master/images/PR3.png)


![Recap](https://github.com/gl-tests-ci/Git_Github/blob/master/images/pull-request.png)

![Workflow](https://github.com/gl-tests-ci/Git_Github/blob/master/images/branching.png)


----


#### Fusionner les commit
[lien ohshitgit](http://ohshitgit.com/)

- si déjà commit:
 * ```git log -5```
 * ```git rebase -i [hash d'un commit sain] ```
>  - squash [les commit a fusionner]
>  - choix du message du commit
 - ```git push -f```


- pas encore commit:

```git commit --amend```

----


### Documentation officielle:

[Branche](https://git-scm.com/book/fr/v1/Les-bases-de-Git-Travailler-avec-des-d%C3%A9p%C3%B4ts-distants)
