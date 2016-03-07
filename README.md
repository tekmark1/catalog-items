# Cataloging Linux Server Configuration
## IP Address
52.34.35.40
## SSH Port Number
2200
## URL to Hosted Web Application
http://ec2-52-34-35-40.us-west-2.compute.amazonaws.com/
## Password for 'grader'
'grader263@'
## Installed Software and Configuration Changes
1. Upgraded all packages
2. Reconfigured local timezone to UTC
  - Completed using dpkg-reconfigure tzdata
3. Installed git in order to clone project
  - sudo apt-get install git
4. Enabled firewall to allow the following:
  - ssh
  - www
  - ntp
5. Changed the ssh port from 22 to 2200
  - sudo nano /etc/ssh/sshd_config
6. Installed Apache2 to host website
  - sudo apt-get install apache2
7. Installed Apache2-mod-wsgi to allow mod_wsgi file to link python with Apache
  - sudo apt-get install libapache2-mod-wsgi
8. Installed postgresql database
  - sudo apt-get install postgresql
9. Installed psycopg2 in tandem with postgresql
  - sudo apt-get install python-psycopg2
10. Installed python oauth2client for authentication purposes
  - sudo apt-get install python-oauth2client
11. Installed Flask
  - sudo apt-get install Flask
12. Installed sqlalchemy
  - sudo apt-get install python-sqlalchemy
13. Logged into postgresql database as postgress and created a new user named catalog (with password catalog), as well as a new database named catalog.
14. Disabled root login abilities
  - sudo /etc/ssh/sshd_config

## Third Party Sources
1. https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04
  - Used this website to figure out how to create a new user and database (as well as to set permissions) in postgresql
2. http://packages.ubuntu.com/
  - Used to find packages needed to install for configuration
3. http://docs.sqlalchemy.org/en/latest/core/engines.html
  - Engine configuration for postgresql within the __init__.py file and database_setup.py file to connect to database
4. https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
  - Used for multiple reasons, including:
    - Creating an __init__.py file to hold logic that runs the app
    - Insalling Flask
    - Configuring the virtual host
    - creating the .wsgi file
5. The Udacit Forums were also a great help!!
