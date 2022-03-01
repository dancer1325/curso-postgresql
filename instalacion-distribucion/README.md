# How to run postgreSQL under Vagrant?
* These steps must be done after executing the 2 first points in the installation (root REAMDE.md)
  * [MAC M1] Follow the steps indicated, creating the 'scr' folder and doing the git clone
* Go to the path in which your Vagrantfile is
  * [MAC M1] Take the one placed in MACM1 subfolder
  * [Others] Take this one, placed here
* `vagrant up`
  * Start Vagrant based on the Vagrantfile
* `vagrant ssh`
  * Access to the new launched machine
* `yum search postgresql`
  * Either centos (VM's OS used for others) or fedora (Docker container's OS used for MAC M1), use yum commands
  * Look for postgreSQL coincidences in the fedora repository
* `yum info NameOfThePackage`
  * Get information about the package NameOfThePackage
  * Here you can check that the versions delivered by the own OS's distribution is older than latest releases of the software
* `sudo yum install postgresql-server.aarch64`
  * Install
    * postgreSQL server
    * postgresql.aarch64, which it's postgreSQL client
* `sudo postgresql-setup initdb`
  * Initialize the database
* `sudo systemctl start postgresql.service`
  * Initialize the postgresql service
* `sudo systemctl status postgresql.service`
  * Initialize the postgresql service
* `sudo systemctl status postgresql.service`
  * Check service's status
* `exit`
  * Exit from the VM / container console
* `vagrant suspend`
  * Suspend the container using vagrant, but it's still up the container
* [MACM1] Go in the browser to 'http://localhost:8080' to login in the NGINX page