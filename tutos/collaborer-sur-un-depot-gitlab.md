## Collaborer sur un dépôt `gitHub`

Par défaut seul le créateur d'un dépôt peut y ajouter des commits.

Si un autre développeur souhaite contribuer au dépôt, il existe deux manières de procéder:
- *forker* le dépôt puis proposer une contribution à l'aide d'un *pull request*;
- ou obtenir la permission d'ajouter des commits directement dans le dépôt.

Nous découvrirons les *pull requests* dans le TP suivant.

### Objectif et programme

L'objectif de ce tuto est d'ajouter un fichier dans le dépôt d'un autre étudiant.

Dans ce tuto, nous allons chacun:

- donner les droits à un autre étudiant d'ajouter des commits dans un dépôt personnel;
- et ajouter des commits dans le dépôt personnel d'un autre étudiant, après qu'il nous ait donné les droits nécessaires.

### Notes importantes

À lire avant de commencer:

- Contrairement au TD précédent, les commandes `git` ne seront pas fournies de manière complète. À vous de les compléter en vous inspirant de ce que vous aviez fait au TD précédent.
- Avant de faire un `git clone`, pensez à sortir de votre dossier en cours, à l'aide de la commande `$ cd ..`

### Procédure pour ajouter un développeur dans une équipe GitHub:

1. Depuis la barre latérale de la page du dépôt, cliquer sur "Paramètres"
1. Cliquer sur "Membres"
1. Taper le ou les noms d'utilisateurs (ou adresse email) du/des développeurs à ajouter
1. Vérifier que le(s) développeur(s) est/sont bien capables d'ajouter et pusher un commit dans la branche de travail du dépôt (ex: `master`)

### Procédure pour ajouter un commit dans le dépôt d'un autre développeur

1. Utiliser `git clone` pour importer le dépôt de l'autre étudiant
1. S'assurer qu'on a bien les dernières mises à jour (`git pull`)
1. Créer un nouveau fichier dans le dépôt local, puis l'ajouter à l'index (`git add`)
1. Créer un commit contenant ce fichier (`git commit`) puis l'envoyer sur le dépôt de l'autre étudiant (`git push`)
1. Dans l'interface web de GitHub, aller sur le projet de votre camarade, puis cliquez sur "commits" pour vérifier que votre commit apparaît bien dans la liste.
