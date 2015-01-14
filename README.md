Bluecain is a collection of Kickstart files that are used to test the
CentOS deployment process.

The aim is to not only test the installer, but also typical roles
that people deploy CentOS for.

--------------------------------------------------------------------

Here is what needs doing :
- Write a kickstart file that would  install to either a 'blank' disk or
to a disk that already has a previous OS

- Write a bash shell script that can be run on the machine, which would 
do some tests and exit with '0' if all goes well.

- Please name the kickstart file in a way that it ends in .cfg

- Please name the test script exactly the same as the kickstart file but 
ending in .sh


--------------------------------------------------------------------

Here is what happens at test time:

- When the distro tree is in place the kickstart would be used to run 
through an install.

- Once the install is done, the machine or vm will reboot

- post reboot, an ssh connection is made to the installed machine or vm, 
with the test script being ssh'd over.

- test script is run, and hopefully exits with 0

These steps are run for every kickstart file included in this git repo


--------------------------------------------------------------------

Feel free to contribute against centos 5,6 or 7 (or common ones ) for 
bare metal installs, Xen installs and KVM installs.

Xen and KVM installs are run via python-virtinstall. 

