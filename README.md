@@ -0,0 +1,103 @@
Ecoride app
=============


[TOC]


I. About
--------

This app is made by [Artevelde University College Ghent][ahs] as part of a project-based scientific research project.

### Project Team

 - Jeroen Knockaert   (Student/Web-Designer)
 - Neeltje Chanterie  (Student/Web-Designer)
 - Valérie Verplanken (Student/Web-Designer)



II. Installation
----------------

### Local Development Environment

 - Use [Artevelde Laravel Homestead][artestead].

#### Configuration 

	$ artestead edit
 
```
sites:

…

# Ecoride
# ---------

    - map: www.ecoride.arteveldehogeschool.local
      to: /home/vagrant/Code/ecoride.arteveldehogeschool.local/www/public
      hhvm: false
```

Start with the `provision` option to enable the new configuration option

	$ artestead up --provision

#### Install Dependencies

	$ cd ~/Code/
	$ git clone https://bitbucket.org/JeroenKnockaert/ecoride.arteveldehogeschool.local/
	$ cd ~/Code/ecoride.arteveldehogeschool.local/www/
	$ composer self-update
	$ composer install
	$ composer update
	$ npm install
	$ bower install

	$ artestead up
	$ artestead ssh
	vagrant@homestead$ cd ~/Code/ecoride.arteveldehogeschool.local/www/
	vagrant@homestead$ cp .env.example .env
	
> Windows:
>
>      vagrant@homestead$ dos2unix **/.settings **/*.sh artisan
	
	vagrant@homestead$ database/init.sh
	vagrant@homestead$ ./artisan migrate --seed

### Pages

 - **API**
    - http://www.ecoride.arteveldehogeschool.local/api/v1
 - **Backoffice**
    - http://www.ecoride.arteveldehogeschool.local/backoffice
 - **Frontoffice**
    - http://www.ecoride.arteveldehogeschool.local
    - http://www.ecoride.arteveldehogeschool.local/Rides
    - http://www.ecoride.arteveldehogeschool.local/Parking
    - http://www.ecoride.arteveldehogeschool.local/Login
    - http://www.ecoride.arteveldehogeschool.local/Settings
 - **Login**
    - http://www.ecoride.arteveldehogeschool.local/Login
 - **Register**
    - http://www.ecoride.arteveldehogeschool.local/Register
 - **Ride**
    - http://www.ecoride.arteveldehogeschool.local/Ride
    - http://www.ecoride.arteveldehogeschool.local/Rides
    - http://www.ecoride.arteveldehogeschool.local/Ridedetail
 - **Style Guide**
    - http://www.ecoride.arteveldehogeschool.local/styleguide

### Docs
 - **Productiedossier**
  - **Functionaliteiten.md**
 
 
[ahs]:			http://www.arteveldehogeschool.be/en
[artestead]:	https://bitbucket.org/JeroenKnockaert/ecoride_v2


