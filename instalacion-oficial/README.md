# How to run postgreSQL under Vagrant?
* These steps must be done after executing the 2 first points in the installation (root REAMDE.md)
* Go to the path in which your Vagrantfile is
  * [MAC M1] Take the one placed in MACM1 subfolder
  * [Others] Take this one, placed here
* `vagrant up`
  * Start Vagrant based on the Vagrantfile
* `vagrant ssh`
  * Access to the new launched machine
* Go to https://www.postgresql.org/download/, and check your OS, and follow the steps indicated
  * [MAC M1 with Fedora] TODO: Solution not found to install it, following these steps https://www.postgresql.org/download/linux/redhat/