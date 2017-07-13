# Postgresql
![gras](logo.png)

## Install - Ubuntu

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

## Create utilisateur


