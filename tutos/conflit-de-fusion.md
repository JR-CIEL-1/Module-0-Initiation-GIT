## Résoudre un conflit de fusion

Un conflit de fusion intervient lorsque l'on tente de fusionner deux branches qui modifient la même partie d'un même fichier. Dans ce cas, `git` va intégrer les deux versions dans le même fichier puis laisser le développeur décider du contenu final de cette partie.

L'objectif de ce tuto est d'apprendre à résoudre un conflit de fusion. (*merge conflict*)

Pour cela, nous allons devoir commencer par en causer un !

### Procédure pour causer un conflit de fusion

Étapes à suivre, une par une:

1. Créer un nouveau dépôt sur Github
2. Cloner ce dépôt localement avec `git clone`
3. Dans le répertoire du dépôt local, créer un fichier `README.md` contenant les paroles d'une chanson de votre choix
4. Créer un commit initial sur la banche main et l'envoyer sur Github avec `git add`, `git commit` puis `git push`
5. Créer une branche `branche1` à partir de `main`, avec la commande `git checkout -b branche1`
6. Verifier que vous êtes bien dans la branche branche1 avec la commande `$ git branch`
7. Dans le `README.md` de cette branche, modifier à votre guise la première phrase des paroles, créer un commit, créer une branche nommée `branche1` sur gitHub et envoyer les modifications avec la commenade  `git push --set-upstream origin branche1 `
8. Revenir à la branche `main` avec `git checkout main`
9. Créer une branche `branche2` à partir de `main` (comme dans l'étape 5)
10. Dans le `README.md` de cette branche, modifier également la première phrase des paroles avec un texte différent de celui saisi à l'étape 7, créer un commit, créer une branche sur gitHub nommée `branche2` et envoyer les modifications avec la commande  `git push --set-upstream origin branche2 `
11. Revenir à la branche `main`
12. Fusionner `branche1` dans `main`, avec `git merge branche1`
13. Fusionner `branche2` dans `main` , avec `git merge branche2`

Si vous avez bien suivi cette procédure, vous devriez obtenir un conflit de fusion:

```
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
```

Voici ce que devrait répondre `git status`:

```
On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)

        both modified:   README.md
```

### Procédure pour résoudre un conflit de fusion

Pour résoudre ce conflit, il va falloir:

[ressource classroom pour la résolution de conflit lors d'un merge](https://openclassrooms.com/fr/courses/7688581-devenez-un-expert-de-git-et-github/7851552-resolvez-les-conflits-avec-git)

Après la résolution du conflit de fusion, `git status` devrait répondre ceci:

```
On branch master
nothing to commit, working tree clean
```

### Bonus

- supprimer les branches `branche1` et `branche2`, non seulement dans votre dépôt local, mais aussi dans le dépôt distant associé (sur GitHub).

  
