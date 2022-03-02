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