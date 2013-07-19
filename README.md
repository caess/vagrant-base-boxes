These are the definitions for my Vagrant base boxes using VirtualBox.  Right now, I only have definitions for CentOS 6 base boxes.

# How do I build these myself?
First, install the [veewee gem](https://github.com/jedi4ever/veewee).

For each base box you want to build:

1. Build the base box: `veewee vbox build *DEFINITION*`<br>
  For example: `veewee vbox build CentOS-6.4-i386`
2. Export the base box: `vagrant package --base *DEFINITION* --output *BOX FILE*`<br>
  For example: `vagrant package --base CentOS-6.4-i386 --output caess-centos-6-i386.box`
3. Import the base box: `vagrant box add *NAME* *BOX* FILE`<br>
  For example: `vagrant box add caess-centos-6-i386 caess-centos-6-i386.box`

# Licensing
The overall license can be found in LICENSE.

The CentOS base boxes are based on the CentOS-6.2-x86_64_minimal base box definition distributed with the `veewee` gem as of August 2012. As derivative works, they fall under the license for `veewee` which is included at LICENSE.veewee.