============
Introduction
============


The Workshop
============

Details
-------
- The goal of the workshop is to prepare for the Red Hat Certified System
  Administrator and Engineer exams.
- 7pm - 9pm Thursdays.
- Scheduled 8 weeks but we can extend it.


Facilitator
-----------
.. rst-class:: build

- Robb Hendershot
- ~10 years as Linux Sys Admin for Lockheed Martin
- RHCSA RHEL4/RHEL5
- RHCSA RHEL6
- Taking RHEL7 exams 2nd week of October


Intros
------
- Name
- Linux/Unix background
- Why you are here


Useful Resources
----------------
- Prereq test

- Cert Depot Study Guide -
  http://www.certdepot.net/rhel7-rhcsa-exam-objectives/


RHEL Overview
=============
.. rst-class:: build

- Red Hat Enterprise Linux
- RHEL line started in 2003
- RHEL5 supported into 2020
- RHEL6 supported into 2023
- RHEL7 supported into 2027
- Many variants including Scientific Linux and Oracle Linux
- CentOS - Unsupported downstream version
- Fedora - Unsupported upstream version


RHCSA
=====

**Red Hat Certified System Administrator (RHCSA)**

An RHCSA certification is earned when an IT professional demonstrates the core
system-administration skills required in Red Hat Enterprise Linux environments.


RHCSA Prep Classes
------------------
**For Windows Admins**

- Red Hat System Administration I (RH124)
- Red Hat System Administration II (RH134)


**For Linux Admins**

- RHCSA Rapid Track Course (RH199)


RHCSA Exam
----------
**Exam**

- EX200 - Red Hat Certified System Administrator (RHCSA) exam ($400)

**Web Page**

- http://www.redhat.com/en/services/certification/rhcsa


RHCE
====
**Red Hat Certified Engineer (RHCE)**

A Red Hat Certified Engineer (RHCE) is a Red Hat Certified System Administrator
(RHCSA) who possesses the additional skills, knowledge, and abilities required
of a senior system administrator responsible for Red Hat Enterprise Linux
systems.

RHCE Prep Classes
-----------------
**For Windows Admins**

- Red Hat System Administration I (RH124)
- Red Hat System Administration II (RH134)
- Red Hat System Administration III (RH254)


**For Linux Admin**

- RHCSA Rapid Track Course (RH199)
- Red Hat System Administration III (RH254)
- RHCE Certification Lab (to re-certify)

RHCE Exam
---------
**Exam**

- EX200 - Red Hat Certified System Administrator (RHCSA) exam ($400)
- EX300 - Red Hat Certified Engineer (RHCE) exam ($400)

**Web Page**

- http://www.redhat.com/en/services/certification/rhce


RHCSA Requirements (ex200)
==========================
Requirements for the RHCSA exam can be found at-
http://www.redhat.com/en/services/training/ex200-red-hat-certified-system-administrator-rhcsa-exam


RHCSA Requirements (ex200)
==========================
Understand and use essential tools
----------------------------------
- Access a shell prompt and issue commands with correct syntax
- Use input-output redirection (>, >>, \|, 2>, etc.)
- Use grep and regular expressions to analyze text
- Access remote systems using ssh
- Log in and switch users in multiuser targets
- Archive, compress, unpack, and uncompress files using tar, star, gzip, and
  bzip2

.. nextslide::

- Create and edit text files
- Create, delete, copy, and move files and directories
- Create hard and soft links
- List, set, and change standard ugo/rwx permissions
- Locate, read, and use system documentation including man, info, and files in
  /usr/share/doc


Operate running systems
-----------------------
- Boot, reboot, and shut down a system normally
- Boot systems into different targets manually
- Interrupt the boot process in order to gain access to a system
- Identify CPU/memory intensive processes, adjust process priority with
  renice, and kill processes
- Locate and interpret system log files and journals
- Access a virtual machine's console
- Start and stop virtual machines
- Start, stop, and check the status of network services
- Securely transfer files between systems


RHCSA Reqs - Configure local storage
------------------------------------
- List, create, delete partitions on MBR and GPT disks
- Create and remove physical volumes, assign physical volumes to volume
  groups, and create and delete logical volumes
- Configure systems to mount file systems at boot by Universally Unique ID
  (UUID) or label
- Add new partitions and logical volumes, and swap to a system
  non-destructively


RHCSA Reqs - Create and configure file systems
----------------------------------------------
- Create, mount, unmount, and use vfat, ext4, and xfs file systems
- Mount and unmount CIFS and NFS network file systems
- Extend existing logical volumes
- Create and configure set-GID directories for collaboration
- Create and manage Access Control Lists (ACLs)
- Diagnose and correct file permission problems


RHCSA Reqs - Deploy, configure, and maintain systems (1)
--------------------------------------------------------
- Configure networking and hostname resolution statically or dynamically
- Schedule tasks using at and cron
- Start and stop services and configure services to start automatically at boot
- Configure systems to boot into a specific target automatically
- Install Red Hat Enterprise Linux automatically using Kickstart
- Configure a physical machine to host virtual guests
- Install Red Hat Enterprise Linux systems as virtual guests


RHCSA Reqs - Deploy, configure, and maintain systems (2)
--------------------------------------------------------
- Configure systems to launch virtual machines at boot
- Configure network services to start automatically at boot
- Configure a system to use time services
- Install and update software packages from Red Hat Network, a remote
  repository, or from the local file system
- Update the kernel package appropriately to ensure a bootable system
- Modify the system bootloader


RHCSA Reqs - Manage users and groups
------------------------------------
- Create, delete, and modify local user accounts
- Change passwords and adjust password aging for local user accounts
- Create, delete, and modify local groups and group memberships
- Configure a system to use an existing authentication service for user and
  group information


RHCSA Reqs - Manage security
----------------------------
- Configure firewall settings using firewall-config, firewall-cmd, or iptables
- Configure key-based authentication for SSH
- Set enforcing and permissive modes for SELinux
- List and identify SELinux file and process context
- Restore default file contexts
- Use boolean settings to modify system SELinux settings
- Diagnose and address routine SELinux policy violations


RHCE Requirements (ex300)
=========================
Requirements for the RHCE exam can be found at -
http://www.redhat.com/en/services/training/ex300-red-hat-certified-engineer-rhce-exam


RHCE Reqs - System configuration and management
-----------------------------------------------
- Use network teaming or bonding to configure aggregated network links between
  two Red Hat Enterprise Linux systems
- Configure IPv6 addresses and perform basic IPv6 troubleshooting
- Route IP traffic and create static routes
- Use firewalld and associated mechanisms such as rich rules, zones and custom
  rules, to implement packet filtering and configure network address
  translation (NAT)
- Use /proc/sys and sysctl to modify and set kernel runtime parameters


RHCE Reqs - System configuration and management
-----------------------------------------------
- Configure a system to authenticate using Kerberos
- Configure a system as either an iSCSI target or initiator that persistently
  mounts an iSCSI target
- Produce and deliver reports on system utilization (processor, memory, disk,
  and network)
- Use shell scripting to automate system maintenance tasks


RHCE Reqs - Network services
----------------------------
- Install the packages needed to provide the service
- Configure SELinux to support the service
- Use SELinux port labeling to allow services to use non-standard ports
- Configure the service to start when the system is booted
- Configure the service for basic operation
- Configure host-based and user-based security for the service


RHCE Reqs - HTTP/HTTPS
----------------------
- Configure a virtual host
- Configure private directories
- Deploy a basic CGI application
- Configure group-managed content
- Configure TLS security


RHCE Reqs - DNS
---------------
- Configure a caching-only name server
- Troubleshoot DNS client issues


RHCE Reqs - NFS
---------------
- Provide network shares to specific clients
- Provide network shares suitable for group collaboration
- Use Kerberos to control access to NFS network shares


RHCE Reqs - SMB
---------------
- Provide network shares to specific clients
- Provide network shares suitable for group collaboration
- Use Kerberos to authenticate access to shared directories


RHCE Reqs - SMTP
----------------
- Configure a system to forward all email to a central mail server


RHCE Reqs - SSH
---------------
- Configure key-based authentication
- Configure additional options described in documentation


RHCE Reqs - NTP
---------------
- Synchronize time using other NTP peers


RHCE Reqs - Database services
-----------------------------
- Install and configure MariaDB
- Backup and restore a database
- Create a simple database schema
- Perform simple SQL queries against a database


Workshop Prep
=============
- Install RHEL on VM

