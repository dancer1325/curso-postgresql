# How to run postgreSQL under Vagrant?
* These steps must be done after executing the 2 first points in the installation (root REAMDE.md)
  * [MAC M1] Follow the steps indicated, creating the 'scr' folder and doing the git clone
    * TODO: Clean, removing the unnecessary stuff in the Dockerfile contained into the subfolder
* Go to the path in which your Vagrantfile is
  * [MAC M1] Take the one placed in MACM1 subfolder
  * [Others] Take this one, placed here
* `vagrant up`
  * Start Vagrant based on the Vagrantfile
* `vagrant ssh`
  * Access to the new launched machine
* Go to https://www.postgresql.org/ftp/source/, check the desired version, copy the URL and download it
  * [MAC M1 with Fedora] 
    * `sudo dnf install wget`
      * Install wget package
    * `sudo dnf install https://ftp.postgresql.org/pub/source/DesiredVersion.tar.bz2`
  * [Others] 
    * Install some wget package in case that you need it
    * `sudo wget https://ftp.postgresql.org/pub/source/DesiredVersion.tar.bz2`
* Decompress the binary file
  * Install some decompress package
    * [Fedora] `sudo dnf install bzip2`
  * Run a command to decompress it 
    * `tar -xvjf NameOfTheBinary.bz2`
  * You can check that a folder has been created with the code decompressed
* Install the necessary requirements to run it
  * `cat INSTALL`
    * Open the INSTALL file which exists into the postgreeSQL folder recently decompressed
  * Required dependencies
    * [Fedora]
      * `sudo dnf install -y readline-devel zlib-devel make gcc`
* Check that all the required dependencies are installed
  * `./configure` 
    * If no error is indicated --> All have been installed correctly
* Compile the code
  * `make`
* Install 
  * `sudo make install`
* Create a directory to store the installation data
  * `sudo mkdir -p /usr/local/pgsql/data`
    * '-p' required to create the parent directories
* Create system user and gives credentials to be the owner of the folder
  * `sudo useradd -r -U -M -d /usr/local/pgsql/data postgres`
    * '-r' indicates that it's a system user
    * '-U' TODO: Check what it does
    * '-M' TODO: Check what it does
    * '-d' TODO: Check what it does
  * `sudo chown postgres:postgres /usr/local/pgsql/data`
    * UserName:GroupName
* Switch to the user created
  * `sudo su - postgres`
* Initialize the databases in that folder created
  * `/src/bin/initdb -D /usr/local/pgsql/data`
    * Problems:
      * Problem1: `-bash: /src/bin/initdb: No such file or directory` got it
        * Solution: TODO: Find a solution for it