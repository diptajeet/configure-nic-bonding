Role Name
=========
Configuring NIC Bonding in Linux System

Requirements
------------
- Expects CentOS/RHEL 6.x based system
- Minimum Ansible Version : 1.2
- Expects the system is connected to a yum repository
- Expects the system has 2 connected NIC interfaces - eth0 & eth1
- The system already has an ip address configured on eth0
- A backup of current NIC configuration shall be available under /etc/sysconfig/network-scripts/

This playbook configures a basic active-backup NIC bonding with a static IP Address on Linux system. To use this, first edit the "inventory" file to contain the hostnames of the machines on which you want NIC Bonding configured.

Running the Playbook:
----------------
Then run the playbook, use this:

ansible-playbook configure-nic-bonding.yml -i inventory

When the playbook run completes, you should be able to see the bonding configured as bond0 with two slave interfaces eth0 & eth1.

This is a very simple playbook and could serve as a starting point for developing more complex NIC bonding playbooks.

License
-------

MIT

Author Information
------------------

Diptajeet Khan