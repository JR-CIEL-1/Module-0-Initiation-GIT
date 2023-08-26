## Créer un dépôt `git` sur le serveur GitLab de la section CIEL

Dans ce tuto, nous allons:

- installer et/ou configurer `git`
- créer un dépôt sur GitLab
- cloner ce dépôt sur votre disque dur (`git clone`)
- y ajouter un fichier (`git add`, `git commit`), puis mettre à jour le dépôt distant (`git push`)

Le but est de retrouver ce fichier dans la page du dépôt sur GitLab, ainsi que le commit correspondant.

### Notes importantes

À lire avant de commencer:

- À savoir: "dépôt" se traduit "repository", en Anglais.
- Ce tuto nécessite l'utilisation d'un terminal (aussi appelé "shell", "console" ou "invite de commandes").
  - Si vous êtes sous macOS ou linux: il suffit d'utiliser le terminal fourni. Si macOS vous propose d'installer "XCode Command Line Tools", acceptez. Vous aurez peut-être besoin de redémarrer ensuite votre terminal.
  - Si vous êtes sous Windows, utilisez l'outil bash de git ( tapper git bash dans la barre de recherche de windows ) .
- Le signe dollar (`$`) permet d'indiquer que la commande qui suit sera à saisir dans le terminal. Pour que la commande fonctionne, il ne faut pas copier le `$` dans le terminal, seulement la commande qui suit.
- Après chaque commande tapée dans le terminal, pensez à lire et comprendre la réponse fournie avant de passer à l'étape suivante. Dans certains cas, cette réponse vous informera d'une erreur et vous invitera donc à essayer à nouveau.
- Certaines commandes ne répondent rien. Vous pouvez toujours vérifier que l'objectif de l'étape en cours est atteint en ré-exécutant la commande fournie. (par exemple: `git version` affichera le numéro de version après que vous ayez installé `git` et redémarré votre terminal)
- Bref, lisez attentivement chaque étape du début à la fin, et faites l'effort de comprendre ce que vous faites.

Autres infos qui pourraient vous aider si vous êtes bloqué(e):

- Si jamais vous ne reconnaissez plus l'invite de commandes de votre terminal et/ou que vous n'arrivez plus à exécuter des commandes, pressez les touches `Ctrl-C` pour revenir à l'invite de commandes.
- Si jamais vous êtes bloqué(e) dans l'editeur de texte `vi`, tapez la séquence de touches suivante pour quitter et revenir à l'invite de commandes.

### Étapes

À suivre une par une:

1. Vérifier dans le terminal que `git` est bien installé: `$ git version`. Si ce n'est pas le cas, installez-le en suivant les recommandations de votre système d'exploitation où en le téléchargeant depuis [git-scm.com/downloads](https://git-scm.com/downloads), puis redémarrez votre terminal.
1. Vérifier dans le terminal que vous êtes identifié(e): `$ git config user.email` doit afficher votre adresse email Jean Rostand. Si ce n'est pas le cas, suivez les instructions de la section "Votre identité" de [Paramétrage à la première utilisation de Git](https://git-scm.com/book/fr/v2/D%C3%A9marrage-rapide-Param%C3%A9trage-%C3%A0-la-premi%C3%A8re-utilisation-de-Git).
1. Ouvrir l'interface web GitHub
1. Toujours depuis de l'interface de Github, créez un dépôt:
   - Cliquer sur "Nouveau projet"
   - Le nom du projet sera aussi le nom du dépôt correspondant => donner un nom de projet concis, en minuscules, et séparé par des tirets
   - Choisissez "public", afin que le dépôt soit accessible en lecture aux autres étudiants
   - Copier l'adresse HTTPS fournie dans la page du dépôt
1. Dans le terminal:
   - Téléchargez le dépôt sur votre disque-dur: `$ git clone <url>` (remplacer `<url>` par l'adresse HTTPS de votre dépôt, celle qui finit par `.git`)
   - puis entrez dans le dossier de ce dépôt: `$ cd nom_du_dépôt`
1. Créer un commit:
    - `$ echo "Bonjour" >README.md` pour créer un fichier `README.md` contenant le texte "Bonjour"
    - `$ git status` (optionnel) pour constater qu'un fichier a été créé mais pas encore ajouté dans le dépôt
    - `$ git add README.md` pour ajouter le fichier `README.md` dans l'espace de staging (index)
    - `$ git status` (optionnel) pour afficher le contenu actuel de l'espace de staging (index)
    - `$ git commit -m "ajout du fichier README.md"` pour créer un commit à partir de l'espace de staging. Notez que le texte fourni entre guillemets est libre. Similairement à l'objet d'un email, ce message permet d'expliquer de manière concise quelles modifications sont apportées au dépôt par votre commit.
    - `$ git status` (optionnel) pour constater que l'espace de staging a été réinitialisé et qu'aucun fichier n'a été modifié depuis votre commit
    - `$ git push` pour uploader votre commit sur votre dépôt distant : vous devrez créer un token pour cela suivez la video suivante : https://www.youtube.com/watch?v=FugonDV6RdE
1. Le fichier `README.md` devrait maintenant être visible depuis la page web du dépôt, sur GitLab.
