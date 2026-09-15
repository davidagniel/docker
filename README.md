# docker
hello every body , this repo is to remember me to create a docker with apache , mariadb (with phpmyadmin) and php 

to use the yml file , before you may install docker and docker-compose

the link to use docker , use this link to install docker :

https://aymeric-cucherousset.fr/installer-docker-debian-11/

------------------------

Pour débuter l’installation de docker sur Debian, on va commencer par une mise à jour de la machine :

apt update && apt full-upgrade -y
Puis l’installation des dépendances :

apt-get install -y apt-transport-https ca-certificates curl gnupg lsb-release
Ensuite, on ajout de la clé GPG officielle de Docker :

curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
Ajout du repository Docker dans les sources :

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
Puis on met à jour la liste des sources :

apt update 
Ensuite, on télécharge le paquet Docker depuis les sources :

apt install -y docker-ce docker-ce-cli containerd.io docker-compose
Puis on ajoute le groupe « docker » et on l’attribue à notre utilisateur :

# Création du groupe "docker" :
groupadd docker 
# Attribution du groupe à notre utilisateur :
usermod -aG docker $USER
Enfin on vérifie l’installation de Docker sur la machine :

docker run hello-world

------




create a directory : testdocker
create 2 directories in testdocker's direcotry : www and backups


and use  docker-compose.yml , put in the testdocker's directory 

use docker-compose up -d 

to enter in container : docker container exec -ti (use the name of container_name) /bin/bash  

enjoy ;)
