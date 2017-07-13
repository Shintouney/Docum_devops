# Postgresql
![gras](logo.png)

### Ubuntu
## Installation {#install}

Step 1 - Ajout de la source postgresql

    sudo sh -c "echo 'deb http://apt.postgresql.org/pub/repos/apt/ xenial-pgdg
    main' > /etc/apt/sources.list.d/pgdg.list"sudo sh -c "echo 'deb
    http://apt.postgresql.org/pub/repos/apt/ xenial-pgdg main' >
    /etc/apt/sources.list.d/pgdg.list""

Step 2 - Ajout de la clef public

    wget --quiet -O - http://apt.postgresql.org/pub/repos/apt/ACCC4CF8.asc |
    sudo apt-key add -

Step 3 - Mise à jours des package et installations du programme

    sudo apt-get update
    sudo apt-get install postgresql-common
    sudo apt-get install postgresql-9.5 libpq-dev

## Création d'un utilisateur {#create-user}

Création de l'utilisateur ** shinta **

    sudo -u postgres createuser shinta -s

## Connection {#connect}

Pour se connecter à l'invite de postgresql

    sudo -u postgres psql

## Modification du mot de passe {#change-password}

Connectez vous à psql, le prompt ** postgres=# ** devrais s'afficher, entrer la commande suivante pour
effectuer la modification

    # If you would like to set a password for the user, you can do the following
    postgres=# \password shinta

## Création d'une base de donnée {#create-bdd}

Création de la base ** mybdd ** avec comme proprietaire ** shinta **

    CREATE DATABASE mybdd WITH OWNER shinta ENCODING 'UTF8';
