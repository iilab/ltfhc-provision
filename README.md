ltfhc-provision
===============

Prerequisite
  * Vagrant 1.6.3+
  * Ansible 1.7+

Cobbler in Vagrant. This is meant to be used in the lab or in the field for bare metal provisioning PXE booting AMOS-3002.

The laptop running the provisioning VM should be connected to the local network (and DHCP enabled).
The AMOS-3002 should be connected to the local network through LAN1.
The local network is assumed to be 192.168.1.0/24

 * ```git clone https://github.com/iilab/ltfhc-provision.git```
 * ```cd https://github.com/iilab/ltfhc-provision.git```
 * wget http://cdimage.debian.org/debian-cd/7.6.0/amd64/iso-dvd/debian-7.6.0-amd64-DVD-1.iso.
 * Run ```vagrant up```
   * If the playbook.yml has been updated then run ```vagrant provision```
 * Attach the AMOS-3002 directly to the ethernet port of the laptop
 * Reboot the AMOS-3002.
 * A fully unattended install should happen.
 * Verify that the EMR application is running in a browser: https://192.168.168.170/_utils

