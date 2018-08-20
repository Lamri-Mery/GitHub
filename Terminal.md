#Savoir ce qu'il y a dans le dossier
ls

#Savoir ce qu'il y a dans le dossier avec détail
ls -l

#Savoir ce qu'il y a dans le dossier avec fichier invisible
ls -A

#Savoir où on est
pwd

#Créer un nouveau dossier
mkdir

Créer un nouveau fichier
touch

#Supprimer un dossier
rm -rf

#Supprimer un fichier
rw

#Voir ce qu'il y a dans un fichier directement via le terminal
less

#Copier/coller un fichier
cp (cp premier second -> premier est le nom du fichier qu'on souhaite copier, second le nom qu'on souhaite lui donner)

#Copier un dossier avec tout son contenu
cp -r

#Couper/coller & renommer
nv

#Trouver un fichier dans l'arborescence
find

#Afficher toute les commandes disponible après avoir écrit le début d'un mot
[tab][tab]

#Compresser et décompresser un ficher
tar

sudo apt update                      ### permet de mettre à jour la liste des paquets disponibles, commande à taper en premier
                                         avant toute installation pour être sûr d'avoir les mises à jour.

sudo apt upgrade                     ### permet de mettre à jour les paquets déjà installés, à taper pour faire les mises à 
                                         jour de sécurité.

sudo apt install soft                ### Installe le logiciel "soft" en gérant les dépendances, donc "apt" vous 
                                         demande peut être d'installer d'autres paquets en complément.

sudo apt remove soft                 ### désinstalle le paquet "soft".

sudo apt autoremove soft             ### désinstalle "proprement" le paquet "soft" ainsi que ses dépendances

apt search supersoft                 ### recherche le texte "supersoft" dans les descriptions des paquets

