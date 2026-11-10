# Journal DevOps – semaine 1

pwd : affiche le dossier où je suis
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
