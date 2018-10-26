## Créer un dépôt `git` sur le serveur `gitlab` de l'EEMI

> Note: le signe dollar (`$`) permet d'indiquer que la commande qui suit sera à saisir dans le terminal. Pour que la commande fonctionne, il ne faut pas copier le `$` dans le terminal, seulement la commande qui suit.

> Note: "dépôt" se traduit "repository", en Anglais.

> Note: après chaque commande tapée dans le terminal, pensez à lire et comprendre la réponse fournie avant de passer à l'étape suivante. Dans certains cas, cette réponse vous informera d'une erreur et vous invitera donc à essayer à nouveau.

1. Vérifier dans le terminal que `git` est bien installé: `$ git version`, sinon le télécharger et l'installer depuis https://git-scm.com/downloads puis redémarrer votre terminal
1. Vérifier dans le terminal que vous êtes identifié: `$ git config user.email` doit afficher votre adresse email EEMI, sinon suivez les instructions de la section "Votre identité" de [Paramétrage à la première utilisation de Git](https://git-scm.com/book/fr/v2/D%C3%A9marrage-rapide-Param%C3%A9trage-%C3%A0-la-premi%C3%A8re-utilisation-de-Git)
1. Ouvrir l'interface web GitLab de l'EEMI: [gitlab.eemi.tech](https://gitlab.eemi.tech/)
1. Si vous ne l'avez pas encore fait, ajoutez un mot de passe à votre compte GitLab
1. Toujours depuis de l'interface de GitLab, cliquer sur "Nouveau projet"
1. Le nom du projet sera aussi le nom du dépôt correspondant => donner un nom de projet concis, en minuscules, et séparé par des tirets
1. Ne pas utiliser "privé" pour les travaux à rendre !
1. Copier l'adresse HTTPS (au lieu de SSH) fournie dans la page du dépôt
1. Dans le terminal: `$ git clone adresse_https_du_dépôt` puis `$ cd nom_du_dépôt`
1. Premier commit:
    - `$ echo "Bonjour" >README.md` pour créer `README.md` (documentation du projet)
    - `$ git status` (optionnel) pour constater qu'un fichier a été créé mais pas encore ajouté dans le dépôt
    - `$ git add README.md ` pour ajouter le fichier `README.md` dans l'espace de staging
    - `$ git status` (optionnel) pour afficher le contenu actuel de l'espace de staging
    - `$ git commit -m "first commit: documentation"` pour créer un commit à partir de l'espace de staging. Notez que le texte fourni entre guillemets est libre. Similairement à l'objet d'un email, ce message permet d'expliquer de manière concise quelles modifications sont apportées au dépôt par votre commit.
    - `$ git status` (optionnel) pour constater que l'espace de staging a été réinitialisé et qu'aucun fichier n'a été modifié depuis notre commit
    - `$ git push` pour uploader notre commit sur le serveur git de l'EEMI.
1. Le fichier `README.md` devrait maintenant être visible depuis la page web du dépôt.
