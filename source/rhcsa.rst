==========================
RHCSA Requirements (ex200)
==========================

Requirements for the RHCSA exam can be found at-
http://www.redhat.com/en/services/training/ex200-red-hat-certified-system-administrator-rhcsa-exam


Understand And Use Essential Tools
==================================

Shell Commands
--------------
*"Access a shell prompt and issue commands with correct syntax"*

.. rst-class:: build

    - terminal
    - screen
    - byobu

.. note::

    - Demo


Redirection
-----------
*"Use input-output redirection (>, >>, \|, 2>, etc.)"*

.. rst-class:: build

    - stdout to file:

        .. code-block:: sh

            $ echo 'hello world' > outfile
            $ echo 'wassup' >> outfile

.. rst-class:: build

    - stderr to stdout:

	    .. code-block:: sh

    		$ 2>&1

.. nextslide::
    :increment:

.. rst-class:: build

    - pipe:

        .. code-block:: sh

            $ ls -al | less

.. rst-class:: build

    - tee:

        .. code-block:: sh

            $ ls -al| tee output.txt| less


Grep
----
*"Use grep and regular expressions to analyze text"*

grep

    .. code-block:: sh

        $ grep [OPTIONS] REGEXP [FILE...]

description:
    grep  searches  the  named input FILEs (or standard input if no files are named, or if a single hyphen-minus (-) is given as file name) for lines containing a match to the given PATTERN.  By default, grep prints the matching lines.


Regex
-----
*"Use grep and regular expressions to analyze text"*

A regular expression (also called a "regex" or "regexp") is a way of describing a text string or pattern so that a program can match the pattern against arbitrary text strings, providing an extremely powerful search capability.

- The period (\.) matches any single character.
- \? means that the preceding item is optional, and if found, will be matched at the most, once.
- \* means that the preceding item will be matched zero or more times.
- \+ means the preceding item will be matched one or more times.


SSH
---
*"Access remote systems using ssh"*

**SYNOPSIS**
    - ssh [options] [user@]hostname [command]

**DESCRIPTION**
    ssh (SSH client) is a program for logging into a remote machine and for executing commands on a remote machine.  It is intended to provide secure encrypted communications between two untrusted hosts over an insecure network.

    If command is specified, it is executed on the remote host instead of a login shell.


Switch Users
------------
*"Log in and switch users in multiuser targets"*

    .. code-block:: sh

        $ su - <user>


Archiving
---------
To archive/unarchive directories:

.. rst-class:: build

- tar:

    .. code-block:: sh

        $ tar --selinux -czvf <directory.tgz> <directory> 
        $ tar xzvf <directory.tgz>

- star:

    .. code-block:: sh

        $ star -xattr -H=exustar -c -f=<directory.star> <directory> i
        $ star -x -f=<directory.star>


Compress
--------
To compress/uncompress a file:

.. rst-class:: build

- gzip:

    .. code-block:: sh

        $ gzip <file> 
        $ gunzip <file.gz>

- bzip:

    .. code-block:: sh

        $ bzip2 <file> 
        $ bunzip2 <file.bz2>


Text Files
----------
*"Create and edit text files"*

.. rst-class:: build

- vi
- nano

Files
-----
*"Create, delete, copy, and move files and directories"*

.. rst-class:: build

- create

    .. code-block:: sh

        $ touch <filename>
        $ mkdir <directory>

.. rst-class:: build

- delete

    .. code-block:: sh

        $ rm <file or directory>
        $ rmdir <empty directory>

.. nextslide::
    :increment:

.. rst-class:: build

- copy

    .. code-block:: sh

        $ cp <source> <destination>

.. rst-class:: build

- move

    .. code-block:: sh

        $ mv <source> <destination>


Links
-----
*"Create hard and soft links"*

.. rst-class:: build

- hard link:

    .. code-block:: sh

        $ ln /path1/file1 /path2/file2


- soft link:

    .. code-block:: sh

        $ ln -s /path1/file1 /path2/file2     


- check link:

    .. code-block:: sh

        $ ln -s /path1/file1 /path2/file2  


Permissions
-----------
*"List, set, and change standard ugo/rwx permissions"*

ls
    .. code-block:: sh

        $ ls -l /home/rdhender/
        drwxrwxr-x. 1 rdhender rdhender  38 Sep 22 21:09 rh_cert


.. nextslide:: 

groupings

    .. code-block:: sh

        $ ls -l /home/rdhender/
        drwxrwxr-x. 1 rdhender rdhender  38 Sep 22 21:09 rh_cert

- owner 
- group 
- other


.. nextslide:: 

first symbol

    .. code-block:: sh

        $ ls -l /home/rdhender/
        drwxrwxr-x. 1 rdhender rdhender  38 Sep 22 21:09 rh_cert

- d — a directory
- \- (dash) — a regular file (rather than directory or link)
- l — a symbolic link to another program or file elsewhere on the system


.. nextslide:: 

other groups

    .. code-block:: sh

        $ ls -l /home/rdhender/
        drwxrwxr-x. 1 rdhender rdhender  38 Sep 22 21:09 rh_cert

- r — file can be read
- w — file can be written to
- x — file can be executed (if it is a program)
- \- (dash) — specific permission has not been assigned

.. nextslide::
    :increment:

chmod:

    .. code-block:: sh

        $ chmod o+w <filename>
        $ chmod 775 <filename>

.. nextslide::
    :increment:

identities

- u — the user who owns the file (that is, the owner)
- g — the group to which the user belongs
- o — others (not the owner or the owner's group)
- a — everyone or all (u, g, and o)

permissions

- r — read access
- w — write access
- x — execute access

actions

- + — adds the permission
- \- — removes the permission
- = — makes it the only permission

numeric

- r = 4
- w = 2
- x = 1
- \- = 0


Documentation
-------------
*"Locate, read, and use system documentation including man, info, and files in /usr/share/doc"*

.. rst-class:: build

- man pages:

    .. code-block:: sh

        $ man ps

- whatis:

    .. code-block:: sh

        $ whatis ps
          ps (1) - report a snapshot of the current processes
          ps (1p) - report process status

    .. code-block:: sh

        $ makewhatis

.. nextslide::
    :increment:

.. rst-class:: build

- apropos:

    .. code-block:: sh

        $ apropos ps
          capsh (1) - capability shell wrapper
          ...
          getpt (3) - open the pseudo-terminal master (PTM)

- info:

    .. code-block:: sh

        $ info ipc
        $ ls /usr/share/info

- app specific:

    .. code-block:: sh

        $ ls /usr/share/doc


Operate Running Systems
=======================

Normal Booting
--------------
*"Boot, reboot, and shut down a system normally"*

.. rst-class:: build

- reboot:

    .. code-block:: sh

        $ reboot
        $ systemctl reboot
        $ shutdown -r now
        $ init 6

- shutdown:

    .. code-block:: sh

        $ halt
        $ systemctl halt
        $ shutdown -h now
        $ init 0

.. nextslide::
    :increment:

.. rst-class:: build

- power off:

    .. code-block:: sh

        $ poweroff
        $ systemctl poweroff

- suspend:

    .. code-block:: sh

        $ systemctl suspend

.. nextslide::
    :increment:

.. rst-class:: build

- hibernate:

    .. code-block:: sh

        $ systemctl hibernate

- hibernate and suspend:

    .. code-block:: sh

        $ systemctl hybrid-sleep

Boot Targets - Before RHEL7
---------------------------
*"Boot systems into different targets manually"*

- 0: halt
- 1: single: maintenance level,
- 2: level without network resources (NFS, etc),
- 3: multi-user level without graphical interface,
- 5: multi-user level with graphical interface
- 6: reboot

.. nextslide::
    :increment:

.. rst-class:: build

- To get the current run level with the old way, type:

    .. code-block:: sh

        $ runlevel

- To change the current run level (where X is the run level), type:

    .. code-block:: sh

        $ init X


Boot Targets - RHEL7
--------------------
*"Boot systems into different targets manually"*

- **systemctl rescue**: to move to single user mode/maintenance level with mounted local file systems,
- **systemctl emergency**: to move to single user mode/maintenance with only /root mounted file system,
- **systemctl isolate multi-user.target**: to move to multi-user level without graphical interface (equivalent to previous run level 3),

.. nextslide::
    :increment:

- **systemctl isolate graphical.target**: to move to multi-user level with graphical interface (equivalent to previous run level 5),
- **systemctl set-default graphical.target**: to set the default run level to multi-user graphical mode,
- **systemctl get-default**: to get the default run level.


Interrupt Boot
--------------
*"Interrupt the boot process in order to gain access to a system"*

#. Boot the system and watch for the grub menu.
#. Select a kernel and hit "e".
#. Modify the ro argument to "rw init=/sysroot/bin/sh".
#. Type ctrl+x.
#. Chroot to access the system with "chroot /sysroot".
#. You are now in single user mode as root.


Processes
---------
*"Identify CPU/memory intensive processes, adjust process priority with renice, and kill processes"*

.. rst-class:: build

- To see server activity type:

    .. code-block:: sh

        $ top

.. rst-class:: build

- To get details about processes, type:

    .. code-block:: sh

        $ ps -edf

.. nextslide::
    :increment:

.. rst-class:: build

- To start a process with a low priority, type:

    .. code-block:: sh

        $ nice -n 10 <process>

.. rst-class:: build

- To change the priority of an already running process type:

    .. code-block:: sh

        $ renice +5 <process id>

.. rst-class:: build

- Alternatively:

    .. code-block:: sh

        $ renice +5 `pgrep <process name>`

.. nextslide::
    :increment:

.. rst-class:: build

- To kill the process type:

    .. code-block:: sh

        $ kill -9 <process id>

.. rst-class:: build

- Alternatively:

    .. code-block:: sh

        $ pkill <process name>

.. nextslide::
    :increment:

.. rst-class:: build

- To display details about IO activities, type:

    .. code-block:: sh

        $ iostat

.. rst-class:: build

- To show network card activities, type:

    .. code-block:: sh

        $ netstat -i

.. rst-class:: build

- To display socket activities, type:

    .. code-block:: sh

        $ netstat -a

.. nextslide::
    :increment:

.. rst-class:: build

- To get details about virtual memory activities (memory, swap, run queue, cpu usage, etc) every 5 second, type:

    .. code-block:: sh

        $ vmstat 5

.. rst-class:: build

- To get a full report of a server activity, type:

    .. code-block:: sh

        $ sar -A


Logs - General presentation
---------------------------
*"Locate and interpret system log files and journals"*

.. rst-class:: build

- System logs - /var/log 

.. rst-class:: build

- SELinux logs - /var/log/audit/audit.log 


Logs - Boot process
-------------------
*"Locate and interpret system log files and journals"*

Systemd manages the boot process and provides information about it.

.. rst-class:: build

- To get the boot process duration, type:

    .. code-block:: sh

        $ systemd-analyze

.. rst-class:: build

- To get the time spent by each task during the boot process, type:

    .. code-block:: sh

        $ systemd-analyze blame


Logs - Journal analysis
------------------------
*"Locate and interpret system log files and journals"*

Systemd also handles the system event log (syslog is not required).

.. rst-class:: build

- To get the content of the Systemd journal, type:

    .. code-block:: sh

        $ journalctl

.. rst-class:: build

- To get all the events related to the crond process in the journal, type:

    .. code-block:: sh

        $ journalctl /sbin/crond

.. rst-class:: build

- Note: You can replace /sbin/crond with \`which crond\`.

.. nextslide::
    :increment:

.. rst-class:: build

- To get all the events since the last boot, type:

    .. code-block:: sh

        $ journalctl -b


.. rst-class:: build

- To get all the events that appeared today in the journal, type:

    .. code-block:: sh

        $ journalctl --since=today


.. rst-class:: build

- To get all the events with a syslog priority of err, type:

    .. code-block:: sh

        $ journalctl -p err

.. nextslide::
    :increment:
    
.. rst-class:: build

- To get the 10 last events and wait for any new one (like tail -f /var/log/messages), type:

    .. code-block:: sh

        $ journalctl -f


Virtual Console - Standard procedure
------------------------------------
*"Access a virtual machine’s console."*

.. rst-class:: build

- KVM on X Windows:

    .. code-block:: sh

        $ virt-manager


.. rst-class:: build
    
- KVM on serial console.

    - Add ‘console=ttyS0‘ on kernel line in the /boot/grub2/grub.cfg:

    .. code-block:: sh

        $ grubby --update-kernel=ALL --args="console=ttyS0"


.. nextslide::
    :increment:
    
.. rst-class:: build

- Reboot the virtual machine:

    .. code-block:: sh

        $ reboot


.. rst-class:: build

- Connect to the console (here vm.example.com):

    .. code-block:: sh

        $ virsh console vm.example.com
        Connected to domain vm.example.com
        Escape character is ^]

        Red Hat Enterprise Linux Server 7.0 (Maipo)
        Kernel 3.10.0-121.el7.x86_64 on an x86_64

        vm login:

Virtual Console - Emergency procedure
---------------------------------------
*"Access a virtual machine’s console."*

.. rst-class:: build

- Connect to the physical host and shut down your virtual machine:

    .. code-block:: sh

        $ virsh destroy vm.example.com


.. rst-class:: build

- Find the virtual machine image file.

    - Defaults to /var/lib/libvirt/images

    .. code-block:: sh

        $ virsh dumpxml | grep "source file="
        <source file='/var/lib/libvirt/images/vm.example.com.img'/>      


.. nextslide::
    :increment:
    
.. rst-class:: build

- Map your virtual machine image file into the host environment (-a for add and -v for verbose):

    .. code-block:: sh

        $ kpartx -av /var/lib/libvirt/images/vm.example.com.img
        add map loop0p1 (253:2): 0 1024000 linear /dev/loop0 2048
        add map loop0p2 (253:3): 0 10240000 linear /dev/loop0 1026048

.. rst-class:: build

- Identify and mount the /boot partition:

    .. code-block:: sh

        $ mount /dev/mapper/loop0p1 /mnt

- Edit /mnt/grub2/grub.cfg file

- Add console=ttyS0 at the end of every line containing /vmlinuz.


.. nextslide::
    :increment:
    
.. rst-class:: build

- Unmount the partition:

    .. code-block:: sh

        $ umount /mnt

.. rst-class:: build

- Unmap the virtual machine image file (-d for delete and -v for verbose):

    .. code-block:: sh

        $ kpartx -dv /var/lib/libvirt/images/vm.example.com.img
        del devmap : loop0p2
        del devmap : loop0p1
        loop deleted : /dev/loop0

.. rst-class:: build

.. nextslide::
    :increment:
    
.. rst-class:: build

- Restart the virtual machine:

    .. code-block:: sh

        $ virsh start vm.example.com
        Domain vm.example.com started

.. rst-class:: build

- Connect to the virtual machine console:

    .. code-block:: sh

        $ virsh console vm.example.com
        Connected to domain vm.example.com
        Escape character is ^]

        CentOS Linux 7 (Core)
        Kernel 3.10.0-123.el7.x86_64 on an x86_64

        vm login:

Virtual Systems
---------------
*"Start and stop virtual machines"*

.. rst-class:: build

- Start:

    .. code-block:: sh

        $ virsh start <machine>

.. rst-class:: build

- Stop:

    .. code-block:: sh

        $ virsh shutdown <machine>

.. rst-class:: build

- Stop immediately

    .. code-block:: sh

        $ virsh destroy <machine>

.. nextslide::
    :increment:
    
.. rst-class:: build

- Delete:

    .. code-block:: sh

        $ virsh undefine <machine>

.. rst-class:: build

- Reboot:

    .. code-block:: sh

        $ virsh reboot <machine>

.. rst-class:: build

- Display configuration information:

    .. code-block:: sh

        $ virsh dominfo <machine>

.. nextslide::
    :increment:
    
.. rst-class:: build

- List virtual machines:

    .. code-block:: sh

        $ virsh list --all

Network Services
----------------
*"Start, stop, and check the status of network services"*

.. rst-class:: build

- Start:

    .. code-block:: sh

        $ systemctl start <service>

.. rst-class:: build

- Stop:

    .. code-block:: sh

        $ systemctl stop <service>

.. nextslide::
    :increment:
    
.. rst-class:: build

- Check:

    .. code-block:: sh

        $ systemctl is-active <service>

.. rst-class:: build

- Status:

    .. code-block:: sh

        $ systemctl status <service>


File Transfer
-------------
*"Securely transfer files between systems"*

.. rst-class:: build

- To transfer the local file to a remote host (here called centos) into the root‘s home directory, type:

    .. code-block:: sh

        # scp loc root@centos:loc
        root@centos's password: your password
        loc                                 100%   16     0.0KB/s   00:00    


.. nextslide::
    :increment:

.. rst-class:: build

- To copy all the files from a specified directory, type:

    .. code-block:: sh

        # scp /etc/ssh/\* root@centos:/tmp
        root@centos's password: your password
        moduli                              100%  236KB 236.5KB/s   00:00
        ssh_config                          100% 2123     2.1KB/s   00:00
        sshd_config                         100% 4442     4.3KB/s   00:00
        ssh_host_ecdsa_key                  100%  227     0.2KB/s   00:00
        ssh_host_ecdsa_key.pub              100%  162     0.2KB/s   00:00
        ssh_host_rsa_key                    100% 1679     1.6KB/s   00:00
        ssh_host_rsa_key.pub                100%  382     0.4KB/s   00:00

- Note: If directories appear in the list created by the \*, there are not transferred: you get a “not a regular file” error (use the tar command to transfer directories).

.. nextslide::
    :increment:
    
- Transfer of a remote file

    .. code-block:: sh

        # scp root@centos:/tmp/rem rem
        root@centos's password: your password
        rem                   100%   22     0.0KB/s   00:00    


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


