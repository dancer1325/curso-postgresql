# Curso de PostgreSQL

# ¿Qué es esto?

Una serie de ejercicios para el curso de PostgreSQL de [OpenWebinars](https://openwebinars.net)

# Requisitos

- Una versión reciente de Vagrant (>= 2.0) (https://www.vagrantup.com/downloads.html)
  * [MAC] `brew install vagrant`
- Una versión reciente de VirtualBox (https://www.virtualbox.org/wiki/Downloads)
  * [MAC M1] It isn't available VirtualBox, so Docker will be used. So next steps will be necessaries following https://betterprogramming.pub/managing-virtual-machines-under-vagrant-on-a-mac-m1-aebc650bc12c
    * `mkdir src`
    * `cd src`
    * `git clone https://github.com/gdraheim/docker-systemctl-replacement.git`
    * `cd ..`
    * Create the Dockerfile added into the subdirectory 'instalacion-dsitribucion/MACM1', and run 
      * `docker build --rm -t mynewvm .`
- Un cliente git (https://git-scm.com/downloads)
- PgAdmin III instalado (https://www.pgadmin.org/download/) o un cliente PostgreSQL (bajo responsabilidad del usuario)
- Un cliente SSH (para Windows recomiendo seguir la siguiente guía: http://donwebayuda.com/como-me-conecto-por-acceso-remoto-via-ssh-desde-mi-pc-windows/
- En principio cualquier SO que soporte Vagrant, VirtualBox, git, PgAdminIII y SSH está soportado, pero recomiendo usar una distribución GNU/Linux o MacOS X.
- 40GB de espacio libre en disco (para las máquinas virtuales)
- 1GB de RAM libre (para las máquinas virtuales)

