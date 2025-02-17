SSH remote key
--------------

Description
^^^^^^^^^^^

This role configure the ssh client authorized public key.

Instructions
^^^^^^^^^^^^

This role will ensure remote hosts is having currently defined ssh authorized public keys in their */root/.ssh/authorized_keys* file
(or sudo user home if not using root user).

These keys are set in file *group_vars/all/equipment_all/authentication.yml*.

Keep in mind that this file can be preceded with equipment_profiles groups.

Input
^^^^^

Mandatory inventory vars:

**hostvars[inventory_hostname]**

* authentication_ssh_keys

Output
^^^^^^

/root/.ssh/authorized_keys contains ssh public keys from inventory

Changelog
^^^^^^^^^

* 1.1.1: Allow keys to sudo user folder. Benoit Leveugle <benoit.leveugle@gmail.com>
* 1.1.0: Update to pip Ansible. Benoit Leveugle <benoit.leveugle@gmail.com>
* 1.0.3: Rename role. Benoit Leveugle <benoit.leveugle@gmail.com>
* 1.0.2: Clean. johnnykeats <johnny.keats@outlook.com>
* 1.0.1: Documentation. johnnykeats <johnny.keats@outlook.com>
* 1.0.0: Role creation. Benoit Leveugle <benoit.leveugle@gmail.com>
