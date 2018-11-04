# Cours `git`

## Cours 1 (2h)

- Cours: Introduction à git:
  - pourquoi / problème
    - éditer des fichiers à plusieurs, de manière concurrente, en évitant les pertes de données
    - garder un historique des modifications et des versions
    - isoler les améliorations en cours de la version qui fonctionne
    - (illustration: linux-code.png)
  - quoi / solutions
    - passé: CVS (1990), MS SourceSafe (1994), Subversion (2000), Git / Mercurial (2005)
    - git créé par Linus Torvalds, pour intégrer les contributions sur son projet Linux
    - critères: vitesse, décentralisation, intégrité des données
    - aujourd'hui: incontournable. plateformes: github, gitlab, bitbucket...
  - comment ?
    - branches et commits:
      - (illustration: master-and-branches.png)
    - terminologie:
      - `Repository` (dépôt): espace de stockage du code source: local / remote
      - `Staging` (index): une mise à jour en cours d'assemblage
      - `Commit`: une mise à jour du code source: lignes de code de fichier(s)
      - `Branch`: une suite de commits liés entre eux
      - `Merge` (fusion): intégrer les mises à jour d'une branche dans une autre
    - flot
      - (illustration: git-local-remotes.png)
    - commandes:
      - `git clone` (ou `git init`): importer ou créer un dépôt localement
      - `git status`: afficher l'état de l'index
      - `git pull`: récupérer mises à jour depuis dépôt distant
      - `git add`: ajouter les mises à jour de fichier(s) dans l'index
      - `git commit`: empaqueter les mises à jour de l'index
      - `git push`: envoyer les commits dans le dépôt distant

- TP: [Créer un dépôt `git` sur le serveur `gitlab` de l'EEMI](tutos/creer-depot-gitlab-eemi.md)

- TP: [Collaborer sur un dépôt `gitlab`](tutos/collaborer-sur-un-depot-gitlab.md)

- Pro tips:
  - Harmoniser l'encodage des fin de lignes (`autocrlf` / `safecrlf`) avec git config, cf [Preparation](https://githowto.com/setup) ou [Dealing with line endings](https://help.github.com/articles/dealing-with-line-endings/)
  - Visualisation de l'historique dans le terminal: [`git git lola`](http://blog.kfish.org/2010/04/git-lola.html)
  - Éviter d'avoir à taper son mot de passe Gitlab à chaque fois: [Stockage des identifiants](https://git-scm.com/book/fr/v2/Utilitaires-Git-Stockage-des-identifiants), ou [Configure SSK key](https://docs.gitlab.com/ee/university/training/topics/env_setup.html#configure-ssh-key), ou encore [GitLab and SSH keys](https://docs.gitlab.com/ee/ssh/) (plus détaillé)

## Cours 2 (2h)

- Cours: Branches et résolution de conflits de fusion (*merge conflict*)
  - Branches `git`
    - `git log`
    - `git branch`
    - `git checkout`
    - `git diff`
    - `git merge`
  - fast-forward vs 3-way: https://dev.to/neshaz/how-to-use-git-merge-the-correctway-25pd
  - (cf https://blog.github.com/2018-08-22-merge-conflicts-in-the-classroom/)

- TP: [Résoudre un conflit de fusion](tutos/conflit-de-fusion.md)

- Cours: Contribuer à un projet open-source sur GitHub
  - Exemples de projets Open-Source
  - Workflow: GitHub Flow
    - *issues*, *pull request*, *review*
  - Dérivation (fork)
  - Licences & étiquette
  - GitHub pages / GitLab pages

- TP: Contribuer à un projet open-source sur GitHub
  - https://www.firsttimersonly.com/
  - https://opensource.guide/fr/how-to-contribute/

- Évaluation: ajouter sa photo et bio sur https://adrienjoly.com/trombi-eemi-2018-1a/

- Pro tips:
  - `git rebase`
  - `git stash`
  - semver + conventionalcommits.org = changelog
  - alternative au GitHub flow: git flow
    - http://danielkummer.github.io/git-flow-cheatsheet/index.fr_FR.html
    - video: https://www.grafikart.fr/formations/git/git-flow
  - ssl: https://help.github.com/articles/set-up-git/#next-steps-authenticating-with-github-from-git
