# Journal DevOps – semaine 1

pwd : affiche le dossier où je suis\n

ls -l : liste les fichiers avec leurs droits

cd /srv/mboamarket : entre dans le dossier de l'application

cat /etc/passwd : affiche la liste des comptes

sudo groupadd equipe : crée le groupe equipe

sudo useradd -m -s /bin/bash -G equipe amina : crée le compte amina

sudo usermod -aG equipe koffi : ajoute koffi au groupe sans retirer les autres

sudo chown root:equipe /srv/mboamarket/partage : donne le dossier au groupe

sudo chmod 2770 /srv/mboamarket/partage : droits du groupe + setgid

tail -n 20 /var/log/mboamarket/app.log : les 20 dernières lignes du journal

grep -c ERROR /var/log/mboamarket/app.log : compte les erreurs



# Journal DevOps - tp01
# OPS-103


samba@Samba:~$ su - amina
Password:
amina@Samba:~$ touch text.txt
amina@Samba:~$ echo "texte" > text.txt
amina@Samba:~$ ls
bonjours  text.txt
amina@Samba:~$


julle@Samba:~$ touch /srv/mboamarket/partage
touch: setting times of '/srv/mboamarket/partage': Permission denied
julle@Samba:~$


# Journal DevOps - tp01
# OPS-104


samba@Samba:/srv/mboamarket/config$ sudo chgrp mboa .env
samba@Samba:/srv/mboamarket/config$ cd .env

samba@Samba:/srv/mboamarket/config$ sudo chmod 640 .env
samba@Samba:/srv/mboamarket/config$ cd .env
-bash: cd: .env: Permission denied
samba@Samba:/srv/mboamarket/config$
