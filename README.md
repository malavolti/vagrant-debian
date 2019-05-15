# HOWTO Instance a new Debian Virtual Machine

## Requirements to install before the next instructions
* Vagrant: https://www.vagrantup.com/downloads.html
* Virtualbox: https://www.virtualbox.org/wiki/Downloads

## Istructions for Linux
1. Retrieve GIT Repository:
   * `sudo su -`
   * `apt install git`
   * `cd /opt/ ; git clone https://github.com/malavolti/vagrant-debian.git` 
   or
   * Download from `https://github.com/malavolti/vagrant-debian/archive/master.zip` into `/opt` directory
2. Move on the "`vagrant-debian`" directory extracted.
   * `cd /opt/vagrant-debian`
3. Install the Virtualbox Guest Additions with "`vagrant plugin install vagrant-vbguest`"
4. Install the Vagrant plugin to resize hard disk: "`vagrant plugin install vagrant-disksize`"
5. Run "`vagrant up`" command to instance the Development Environment.
6. Run "`vagrant rsync-auto > rsync-auto.log 2>&1 &`" to maintain synced the `vagrant-debian` directory inside VM and monitor changes with the log file. Put your files into `share-data` dir to transfer them into `/vagrant/share-data` dir inside the VM.
7. Run "`vagrant ssh`" to access the VM created.

## Istructions for MacOSX
1. Retrieve GIT Repository:
   * `cd Desktop ; git clone https://github.com/malavolti/vagrant-debian.git` 
   or
   * Download from `https://github.com/malavolti/vagrant-debian/archive/master.zip`
2. Move on the "`vagrant-debian`" directory extracted.
3. Install the VirtualBox Guest Additions with "`vagrant plugin install vagrant-vbguest`"
4. Install the Vagrant plugin to resize hard disk: "`vagrant plugin install vagrant-disksize`"
5. Run "`vagrant up`" command to instance the Development Environment.
6. Run "`vagrant rsync-auto > rsync-auto.log 2>&1 &`" to maintain synced the Vagrant directory inside VM and monitor changes with the log file. Put your files into `share-data` dir to transfer them into `/vagrant/share-data` dir inside the VM.
7. Run "`vagrant ssh`" to access the VM created.
   
## Istructions for Windows
1. Download the Repository from: https://github.com/malavolti/vagrant-debian/archive/master.zip
2. Extract the ZIP file on your computer as "`vagrant-debian`".
3. Run "`cmd`" command (Windows) as Administrator and move on the "`vagrant-debian`" directory extracted.
4. Install the VirtualBox Guest Additions with "`vagrant plugin install vagrant-vbguest`"
5. Install the Vagrant plugin to resize hard disk: "`vagrant plugin install vagrant-disksize`"
6. Run "`vagrant up`" command to instance the Development Environment.
7. Run "`vagrant rsync-auto > rsync-auto.log 2>&1 &`" to maintain synced the Vagrant directory inside VM and monitor changes with the log file. Put your files into `share-data` dir to transfer them into `/vagrant/share-data` dir inside the VM.
8. Run "`vagrant ssh`" to access the VM created.

## Useful Commands (to use inside 'vagrant-debian' dir)
1. To shutdown the Development Environment use "`vagrant halt`" within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

2. To reload the Development Environment use "`vagrant reload`" within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

3. To destroy the Development Environment use "`vagrant destroy`" within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

4. To use the Development Environment use "`vagrant ssh`" (to connect into the VM) and "`sudo su`" (to obtain ROOT access) within the "`cmd`" prompt (Windows) or terminal (Linux/OSX)

5. To manage Snapshot in Vagrant
   1. Move in the vagrant VM directory and create a snapshot called "NAME_SNAPSHOT":

      `vagrant snapshot save NAME_SNAPSHOT`

   2. Recover your "`NAME_SNAPSHOT`":

      `vagrant snapshot restore NAME_SNAPSHOT`

   3. (OPTIONAL) List Snapshot:

      `vagrant snapshot list`

   4. (OPTIONAL) Remove Snapshot:

      `vagrant snapshot delete NAME_SNAPSHOT`

## Authors

#### Original Author and Development Lead

* Marco Malavolti (marco.malavolti@gmail.com)
