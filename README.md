#Práctica Symfony

El projecte de la práctica es symfony_Concerts. Es necessari crear la db, les entitats i els esquemes.

#symfony commands:

##Borrar i crear database:

	php bin/console doctrine:database:drop --force
	php bin/console doctrine:database:create


##Actualitzar entitats:

	php bin/console  doctrine:generate:entities AppBundle

##Actualitzar esquemes i taules:

	php bin/console doctrine:schema:update --force

##Pasos a seguir pel correcte funcionament:

Introduirem al terminal les següents comandes posicionantnos a l'arrel del nostre projecte symfony.

	php bin/console doctrine:database:drop --force
	php bin/console doctrine:database:create
	php bin/console  doctrine:generate:entities AppBundle
	sudo php bin/console doctrine:schema:update --force

Haurem de esborrar la carpeta vendor si està si es que dona problemes amb el comandament per a engegar el servidor symfony.

        sudo composer install

Seguidament engegarem el servidor

        sudo bin/console server:start ip_corresponent

Per crear usuaris nem a /register.

Segurament serà necessari reconfigurar l'arxiu parameters.yml per a que funcioni amb la nostra base de dades.

        database_name: dbTrivial
        username_root: root
        password: ausias

Un cop creat l'usuari o usuaris d'exemple anirem a l'arxiu db.sql i amb el terminal dintre de la consola mysql mitjançant el següent comandament entrarem a la consola mysql.

        mysql -u root -p

Aquí entrarem a la db utilitzant:

        use nomDatabase

Aquí afegirem els games i relacions Cheese de usuaris (primers apartats de db.sql a l'arrel del projecte).

Qualsevol problema de permisos per a editar introduir aquestes comandes

        sudo chown -R user:user *
        sudo chmod -R 775 *
