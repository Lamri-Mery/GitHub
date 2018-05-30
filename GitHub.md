# GitHub
       https://github.com/becodeorg/Johnson2/blob/master/01-La-prairie/git/exercice-git-configuration.md
       https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/
       Première utilisation de GitHub
    1. Installer GitHub
       Ouvre un terminal. Copie & colle les lignes dans le terminal et press Enter.
       sudo apt-get update
       sudo apt-get upgrade
       sudo apt-get install git
    2. Se loguer sur GitHub Sous linux
    a) Ouvre ton Terminal. 
    b) Copie/colle le texte ci-dessous, en changeant l'email par l' email de ton compte GitHub
       ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
       Cela crée une clef ssh, avec l'email comme identifiant.
    c) Generating public/private rsa key pair. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
    d) Enter a file in which to save the key (/home/user/my-key-name): [Press enter]
    e) Enter passphrase (empty for no passphrase): [Laisse vide]
    f) Enter same passphrase again: [Laisse vide]
    g) cat ~/my-key-name/my-key-name.pub
    h) copier la clé ssh ( commence par ssh-rsa ......)
    i) Suivre ce tuto à partir du point 2 : Aller sur le 2e lien proposer sur l’en tête du document et sélectionner l’onglet mac avant de suivre les instructions
    3. Se loguer sur GitHub Sous mac
    a) Generating a new SSH key 
    b) Ouvre ton Terminal
    c) Copie/colle le texte ci-dessous, en changeant l'email par l' email de ton compte GitHub. 
	ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
	Cela crée une clef ssh, avec l'email comme identifiant.
    a) Faire le premier point Generating a new SSH key 
    b) cat ~/.ssh/id_rsa.pub 
    c) copier la clé ssh ( commence par ssh-rsa…)
    d) Suivre ce tuto à partir du point 2 : Aller sur le 2e lien proposer sur l’en tête du document et sélectionner l’onglet linux avant de suivre les instructions
    4. Se loguer sur GitHub Sous windows
    a) Generating a new SSH key 
    b) Ouvre Terminal/cmdr. 
    c) Copie/colle le texte ci-dessous, en changeant l'email par l' email de ton compte GitHub 
    d) ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    e) Cela crée une clef ssh, avec l'email comme identifiant.
    f) Generating public/private rsa key pair. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
    g) Enter a file in which to save the key (/Users/UserName/.ssh/id_rsa): [Press enter]
    h) Enter passphrase (empty for no passphrase): [Type a passphrase]
    i) Enter same passphrase again: [Type passphrase again]
    j) cat ~/.ssh/id_rsa.pub
    k) copier la clé ssh ( commence par ssh-rsa ......)
    l) Suivre ce tuto à partir du point 2 : Aller sur le 2e lien proposer sur l’en tête du document et sélectionner l’onglet windows avant de suivre les instructions
    1. Connecter votre mail et nom d’utilisateur en global pour être lier
       git config --global user.email "MON E-MAIL"
       git config --global user.name "MON NOM"
    2. Verifier si on a git et sa version
       git –version
    3. Verifier où il est installé
       which git
       
       Commende Git
    1. initialiser
       Pour dire à git de commencer à versionner mon code, lui indiquer que je dois initialiser mon projet et donc travailler avec git sur ce projet.
       git init
       
    2. status
       Après avoir initialisé mon projet, je peux à tout moment l’utiliser. Cette commende me dit ce qui ce passe sur mon projet.
       git status
       
    3. add
       Cette commende ajouter les fichiers ou dossiers ou des modifications que je souhaite enregistrer dans mon projet.
       git add nom_de_mon_fichier_ou_dossier
       
       Pour ajouter tous les éléments de mon dossier dans mon projet je peux utiliser l’astérixis.
       git add *

	Pour ajouter tous les éléments du dossier dans lequel je suis actuellement j’utilise le points.
	git add .
	
    4. commit
       Lorsque vous modifiez votre repository (depot), vous devez demander à Git d'enregistrer vos modifications en faisant un git commit.
       git commit
       
       À chaque commit on doit absolument indiqué en commentaire pour quel raison ce commit à été créé. Pour ça on a le choix entre git commit --message "commentaire"ou git commit --m "commentaire" entre les guillemets il nous faut donc indiquer que c’est ma première sauvegarde ou qu’est ce qui a été changé depuis ma précédente sauvegarde.
       git commit --m ‘commentaire’
       
       Rééditer les commentaires de mes commit, si l’on s’est trompé avec un commit --amend -m.
       git commit --amend -m ‘commentaire_modifié’

    5. diff
       pour nous indiquer les différences qu’il y a eu sur notre travail depuis le dernier commit.
       git diff
       
       On peut spécifier le fichier que l’on souhaite comparer. (HTML, CSS, JS, ...)
       git diff NOM_DE_MON_FICHIER
       
       Ou comparer deux branches entre elles en les séparant par deux point.
       git diff NOM_DE_MA_BRANCH..NOM_DE_MON_AUTRE_BRANCH
       
       Voir comparer le master le master et une branche.
       git diff master..NOM_DE_MA_BRANCH
       
    6. log
       Visualiser tous les commit depuis le début du projet
       git log
       
    7. branch
       Lorsque l’on ne souhaite pas travailler sur le master de notre travail, on crée un branche parallèle afin de retourner en arrière si besoin. 
       git branch nom_de_ma_nouvelle_branche
       
       Pour vérifier quel sont les branche présentes et sur quels branche je suis.
       git branch
       
       On peut aussi git br en raccourci à git branches.
       git br

    8. branch -a
       Lister toutes les branches afin de ce déplacer dans la branche d’un collègue. (utile avec un fetch)
       git branch -a
       
    9. branch -d
       Utilisé pour supprimer une branche qui a été merge.
       git branch -d nom_de_ma_branche
       
    10. branch -D
       Forcer à supprimer une branche qui n’est pas merge, si celle ci ne nous plaît pas et qu’on souhaite jeter son travail.
       git branch -d nom_de_ma_branche
       
    11. branch -f
       bouge (de force) la branche master à trois parents derrière HEAD et réassigner les branches à un commit.
       git branch -f master HEAD~3 
       ne maitrise pas encore ce chapitre (branch -f) j’arrête là pour le moment les explications de ce point là.
	
    12. checkout
       Permet de sélectionner la branche (ou si on veut le master) où l’on souhaite faire un commit.
       git checkout nom_de_ma_sélection
       
    13. checkout -b
       Permet en une fois de créer une nouvelle branche et de sélectionner la branche nouvellement créé. 
       git  checkout -b nom_de_ma_sélection
       
    14. merge
       permet de fusionner ma branche à mon master on se met sur la branche qu’on souhaite fusionner. Il faut être sur le master via un checkout puis merge la branche souhaité. En cas de conflit je dois éditer le texte moi même, manuellement (en faisant un commit).
       git merge nom_de_ma_branche_que_je_souhaite_fusionner_avec_ma_master
       
    15. Rebase 
       Il prend un ensemble de commits, les "recopie", et les ajoute en bout de chaîne à un autre endroit (le master par exemple). Sur ta branche, tu copies tout ton travail dans un autre depos à l’aide git rebase master, puis tu déplaces ton master sur ce depo à l’aide git rebase nom_de_ma_branche.
       git rebase master
       git rebase nom_de_ma_branche_que_je_souhaite_fusionner_avec_ma_master
       
    16. remote add origin
       c’est l’ajout d’un serveur dans lequel je vais pouvoir pousser mon projet. C’est un projet vide.
       https://github.com/MON_NOM/MONPROJET.git
       
    17. clone
       Récupérer un projet déjà entamer sur le serveur afin de pouvoir continuer à travailler dessus.
       git clone https://github.com/MON_NOM/MONPROJET
       
    18. remote -v
       Vérifie que j’ai bien une remote disponible.
       Git remote -v
       
    19. push
       Poussier mon travail sur le remote, git push indique où est ce que je souhaite l’envoyé sur origin (nom sur serveur GitHub) et sur quel branche donc sur master
       git push origin master
       
       Si on veut push sur une branches
       git push origin nom_de_ma_branche
       
       Si l’on veut heberger son travail  sur GitHub, en ajoutant un fichier CNAME dans un seul projet héberger je peux pointer mon travail sur mon nom de domaine (dans le CNAME ex : lamri-mery.be ou lamri-mery.me ou …). Ne pas oublier de configurer son nom de dns pour qu’il pointe correctement son site. (ne fonctionne que pour des sites static.
       git push origin gh-pages
       
    20. pull
       tirer (récupérer) le travail de quelqu’un d’autre sur mon pc. (Il fait un fetch puis un merge en récupérant le travail).
       git pull origin master
       
       Si on veut pull une branche
       git pull origin  nom_de_ma_branche
       
    21. fetch
       Rapatrier sans faire les avance de commit (utiliser pour travailler sur la branche de quelqu’un d’autre en parallèle). Il tire sans faire les merges.
       git fetch
       
    22. rm -r --cached
       Supprimer fichier ou dossier dans GitHub. Après avoir remove le dossier/fichier, il faudra add le fichier modifié. Une fois fait, il ne faudra pas oublier de commit le tout en informant qu'on a supprimé tel dossier/fichier, avant de push le tout.
       git rm -r --cached nom_de_element_a_supprimer
       
    23. à suivre 

HEAD est le nom du commit sur lequel nous nous situons/travaillons actuellement.
Hash est le nom des commit
^ on l’utilise pour revenir à une commit en arrière
~<num> on l’utilise pour revenir à plusieurs niveaux en arrière <num> est remplacer par le nombre de retours en arrière on souhaite atteindre.
       
Les commendes unix

https://fr.wikipedia.org/wiki/Commandes_Unix

mkdir
pwd
ls
stt
s
ls -l
open .
