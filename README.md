# linux-server-configuration
Take a baseline installation of a Linux server and prepare it to host web applications. Secure the server from a number of attack vectors, install and configure a database server, and deploy an existing web applications onto it.

## Udacity Reviewer Instructions

* __IP Address:__ 35.167.96.98; __SSH Port:__ 2200
* __Web Application URL:__ http://35,167.96.98

## Software Installed

* Apache2
  * Including WSGI module
* PostgreSQL
* Git

## Summary of Configurations

### Linux server
* Updated installed packages
* Created user 'grader' with password 'grader'
* Generated ssh key and granted SSH and SUDO permission to 'grader' 

### Uncomplicated Firewall
* Allow connections to ports 80, 123, and 2200 only
* Changed SSH port from 22 to 2200
* Enabled firewall

### Apache
* Created directories 'catalog/catalog'
* Cloned project repo and renamed 'catalog.py' to '__init__.py'
* Created 'catalog.wsgi' and configured to call '__init__.py'
* Start Apache

### PostgreSQL
* Created user 'catalog' with password 'catalog' and granted permission to CreateDB
* Created DB 'catalog' with 'catalog as owner and locked DB permissions to only 'catalog' user
* Setup tables in the 'catalog' database using database_setup.py
* Updated __init__.py to use 'catalog' DB

## Summary of Resources

### Udacity Courses
* Intro to Linux
* Linux Security
* Web Application Servers

### Udacity Forums
* @Swooding
* @trish_836018
* @abha_356405465602580

### Digital Ocean
* 'How To Deploy a Flask Application on an Ubuntu VPS' 
  https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
* 'How To Secure PostgreSQL on an Ubuntu VPS'
  https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
