Shell Script
----------------
    How many loops are there in shell script?
    How to convert lowercase to uppercase in shell script?
    How to create a user in 10 server.
    what if I want to create a user in 1000 server.
    what does "Tr -d" do?
    what does "grep -oP doll"?
    What is the difference between "sed -i" and "sed -e".
    How to create 100 files without using for loop? HInt: with the help of regular expression?
    How to find the file which is not modified in last 30 days?
    Do I need to mention shebang in the shell script?
    what is shebang in shell script?
    what are the various types of shell in Linux?
    Write a shell script for getting the kernel version of 3 server?
    How to use a parameter in shell script?
    How to find a specific patter in file and then remove the specific patter?
    What is the difference in 'su’ and 'su -’?
    What is $$ in shell script?
    What is $@ in shell script?
    Write a shell script for finding the odd even number?
    Find the second largest number using shell script?






User
-----
    * How to create the multiple user with a same uid? Hint: with -o option in useradd command.
        we can use "-o" option to create the multiple user with a same UID.
            #useradd -o -u 0 -g 0 -N -d /root/ -M root2 
        
    * A user is removed execute the permissions from a /bin directory then how will you add the execute permissions
        we can use any of the below command to restart the /bin permssion.
            #/lib/ld-linux.so /bin/chmod +x /bin
            #perl -e 'chmod 0755, "/bin"'
            
    * What is the meaning -m option in useradd?
        this means "Create the user's home directory if it does not exist"
        
    * How to set the account non-expires ?
        we can set "-M -1" for non expiry account
        #chage -M -1 <user>
        
    * How to ask to change the password to first login?
        we can use "-d" option to force the change the passwrod on first login
        #chage -d 0 [username]
        
    * In which file  the hiarcy of the user check like local user or network user.
        in this file "/etc/nsswitch.conf" hiarchy is mentioned.
        
    * What is the command to check the users related log?
        we can use command like "finger", "last" to see the user related activity.
        
    * What is the location of user log?
        the user log location is "/var/log/secure"
        
    * How to set the root password?
        we can set the root passwrod by login to "single user mode".
        
    * How many  primary Or secondary group we can create?
        A user can be part of 16 groups at a time.
        A user have 1 primary and 15 secondary group.
        
    * What is the difference between in rhel6 and rhel7 in terms of user creating?
        In rhel 6, the user uid started with 500 whereas in rhel 7, the user id started with 1000"
    
    * What is the umask value?
        It is the files and directory permission for users.
        
    * How to create a user with specific uid?
        we can use "-u" option to create a user with specific UID.
        
    * How to set the umask for a specific user?
        we can set the umask value in "/etc/profile" file
        
    * what is suid , guid, sticky bit?
        suid - it is a special file permission for executable files which enables other users to run the file with effective permissions of the file owner
        guid - it is a specical permission for group which allows member of the group to access the files.
        sticky bit - it is specaial permssion of direcory where only owner of the file can delete the file. For exaple, "/tmp" direcoty.
        
    * What is sticky bit? If I have given 777 permission on sticky bit then the other user will delete or edit the file?
        In this case, the file will not delete but can be edited.
        
    * What is the difference between 'su usernane’ and 'su - usernane’
        "su username" means user will be switced to his account but not moved to its home directory.
        "su - username" means user will be switched to his account and move to home its home direcory.
    






Filesystem
------
    What is the difference between ext4 and ext3 in terms of journel? Hint: in ext4 the journel is optional but in ext3 it is mandatory.
    Df -h command is hanging?
    How to extend the lvm?
    How to extend the raw file system. Hint: it's not possible
    Du df showing different output?
    There is a disk of 2 partition, both are working fine.but after rebooting, the one of the partition is not visible? Hint:  there is a problem with the cylinder in the partition. Correct that one it will work
    How to remove a file system?
    How to create an LVM?
    what is the suberblock?
    What is the difference between tune2fs and fsck?
    what is the disadvantage of lvm.
    how to recover lvm?
    how to recover suberblock?
    What is lvm striping?
    What is the difference between L and l in lvm?
    How to reduce the Root file system?
    Df command is hanging ? How do we identify the problem mount point? 
    How to extend swap using LVM?
    What is LVM mirror?
    What is lvm filter?
    How to extend the inode in the Linux?
    How to increase a physical memory of a VM on the fly?












Networking
-----
    What nmlci does?
    what we see or analysis in the tcpdump output
    How to detach the bonding interface?
    How to configure the network interface?
    What are the various types of network bonding?
    How to check the bonding status?
    What are the different mode in net bonding?
    What is the difference between active-active , active-backup, round-robin?
    What is mode 4 in network bonding?
    What is active link mode in network bonding?
    What is the time when kernel check for network bonding up or down Link?
    How to configure bonding?
    How to check the interface status?
    What is mitool?
    Can be create network bonding for 2 interface with different network?
    What is broadcast IP ?
    How to find the broadcast domain/ip of the network






General
------
    What is the default time for ssh to time out.

    
    * How to check whether the  server is virtual or physical?
        we can use the below cammand to find the virtual or physical
            #dmidecode -t system
            
    * Do we need ip tables if we already configured firewall on network?
        iptables provides the security on OS level. This will secure OS.
        
    * How to shutdown the server at 6.00 AM.?
        we can set the the shutdown command in crontab
    
    * A server is not pinging, how to troubleshoot?
        we can use the below steps:
        1. check if the traceroute is reachable to the server. if not then there might be network issue
        2. we will check the server in console.
    
    * What is the difference in Access time and modified time?
        Access time - it is the time when the file was last accessed or read.
        Modified time - it is the time when last modified.
        
    * What is the use of strace command?
        strace is a diagnostic, debugging and instructional userspace utility for Linux.
        
    * What is the configuration file for postfix?
        we can follow the below steps
        1. install the posfix package
            #yum install postfix
        2. edit the "/etc/postfix/main.cf" file and provide the relay host
             relayhost = mailrelay.comcast.com
        3. Restart the service
            #systemctl start postfix
    
    * How to scan the disk new disk?
        we can use the below command to scan the disk
            #echo "- - -" > /sys/class/scsi_host/host0/scan
            # for i in ls /sys/class/scsi_host/;do echo "- - -" >/sys/class/scsi_host/${i}/scan; done
                The dashes act as wildcards meaning "rescan everything". 
                The three values stand for 
                    1. channel, 
	                2. SCSI target ID, and 
	                3. LUN.
	                
    * What is the time for load average? It will 1 10 15 in sec.
        it is the total number of request executing to the total number of request waiting in the queue.
        
    * What is sar -b?
        it is will deisplay the report for I/O  information.
        

    * What is the procedure id 1and 0?
        1 - is the process id for init/systemd
        0 - is the UID for root
        
    * What is the difference in /bin and /sbin
        /bin - it contains all the user related commands
        /sbin - it contains all the system admin commands

    * How to check the active connection for a directory?
        we can use "lsof" to check the active connection.
            #lsof /directory
            

    * What is the difference between who and w?
        who - it will display all the user currently logged in the server
        w - it will display all the user currently logged in the server and tell what the user is doing.
        
    * What is the difference between the /var/log and /var/log/secure ?
        /var/log - contains all the logs
        /var/log/secure - contains user realted logs
    
    * What is the location for systemctl?
        The location of systemctl "/etc/systemd"
        
    * What is the default configuration file for kick start?
        "anaconda-ks.cfg"
        
    * What is the 5 column in the cron tab?
        1. minutes
        2. hours
        3. day
        4. month
        5. week
        6. commands

    * What is systemd?
        This is the first process to start in the server.
    
    * What is the minimum/default memory taken by SSH?
        4MB


    * Is all patch required server reboot?
        No, All patch do not required reboot.
        
    * How to troubleshoot if we are not able to ping, ssh to the server. Consider there is no issue with ssh service, firewall?
        1. Tracerooute the server
        2. get the console and see what is the issue
       
    * How to disable CPU and memory from the OS side?
        Below commads disable the CPU3 from the server.
            #echo 0 > /sys/devices/system/cpu/cpu3/online
            
    * How to allow or deny a specific host based on the service?
        We can mention the service in the "/etc/hosts.deny" file  
        
    What is the difference in OS migration and OS patching?       
    How to store the dmesg log automatically.        
    After patching, the kernel is going with kernel panic error?
    What is the SNMP? What is the default 2 port for SNMP?
    
    What is the difference between RAID1 and RAID 0?
    How to change in the LVM with the linear to mirror to the Raid?
    
    

    what are the different type of os installation?    
    What is the port of samba?
    How to check the system performance issue?
    
    How to run the command in the remote server with password less?
    How to perform the patching?
    How to troubleshoot the performance issue?
    Exept top what the other commands you use to view the performance statistics?
    What “---” in scan command.
    What are the things need to consider for increasing the performance of the server.
    What is IAC(infrastructure as a code in Linux)

        
    What is the parameters need to set when ssh is not  set on the remote the server and need to connect via service account?
    What is the difference between centos 6 and centos 7? Hint: introduction of docker of centos7

    How to configure samba?
    Which is a better os rhel, centos, Fedora?
    How to configure NTP?

Process
-------
        How to count the number of the httpd process  in the server?
        How to make a particular process active?
        What is Zombie process?
        How to prioritize the process?
        What process you are using for process management?
        How to restart a process?
        What is the difference between in init process and Systemd?
        What is the disadvantage in Systemd?
        How to find the child process from a pic?



Kernel
------
        How to disable ping in the servers?
        What is the file for kernel parameter?
        How to upgrade the kernel?
            What is monolethic kernal?
            What is kernal? How it works?
        How to change the default kernel in rhel 7?




Yum
------
    How to install a specific package eg: security pactches in the server?
    What is the difference between the rpm and yum?
    The rpm -qa is not showing any result. What might be the reason?
    How to create yum server?
    How to install package ?
    How to create a yum repo?
    How to recover the rpm database?
    How to create yum repository using one rpm?
    How to install gui in the Linux?
    How to downgrade a package when an application team complain about the application?
    How to create rpm?
    How to create yum repo?







NFS
------
    What is Nfs? Hint: strace command
    How to find the hang file system?
    What is Nfs stale?how u will resolve?
    What are the different services of NAS?
    So if we have multiple NAS mount point. So how we will find which mount is having problem?
    How to see the remote mount point of the NFS server?
    What is rcp service is not running on the server?
    How to configure the NFS from the server and client?
    What is the purpose of 'sync’ in NFS? Hint: it will sync with disk and file before writing it?
    What is NFS tale and how to resolve it?
    What are the different process in NFS?
    how to configure NFS?
    what is the difference between NFS and Samba?
    can be mount NFS in window?
    can we use NFS mount without mounting to the server?
    what are the various options in the NFS?
    what is root_squash?
    what is the difference in sync, async?
    How to mount a nfs permanently?
    What is rwrite and write in nfs?
    How to check the nfs version?
    What is nfs tale?
    What is reason the nfs tale happen?












Boot
------

    * How to increase the boot partition in Linux?
        It's technically possible, but there is NO supported method to do this, 
        and the unsupported method is very risky and can create instability in the disk.

    * How to boot the server in runlavel 4 and how to enable network in run level 4?
        we can use "/usr/sbin/telinit" comamnd to cahnge the runlevel
                #/usr/sbin/telinit <runlevel>
                
    * Explain boot process?
        1. BIOS (Basic Input output System). This will check physical hardware of the system and executes the MBR
        2. MBR (Master boot Record)- this will executes the Grub
        3. Grub (Grand unified Bootloader) - this will executes the kernel and mount the initramfs in a read only mode
        4. kernel - The kernel loads driver modules from initramfs and start the systemd process.
        5. Systemd - starts the default target.
        6. target - 

    * Explain the run level?
        below is the runlevel
            runlevel0.target (System halt/shutdown)
            runlevel1.target (Single-user mode)
            runlevel2.target (User-defined/Site-specific runlevels)
            runlevel3.target (Multi-user)
            runlevel5.target (Multi-user,graphical mode)
            runlevel6.target (Reboot)
            emergency.target (Emergency mode)

    * How to go to the single user mode?
    
    * What is initrd?
        Initrd means initial RAM disk. It mounts the root file system to read only mode.
  
      * What will happen initrd is deleted?
           In this case, the server will not boot and you will find "kernel not found error"
           
    * What is the difference between initrd and Initramfs?
        Initrd is deprecated, replaced by Initramfs,
        initrd was block device based, initramfs is file base.
        with initrd, you created a file system image. with initramfs, you create an archive with the files which the kernel extracts to a tmpfs.
    
    * How  does initram disk create?
        initrd can be created with “mkinitrd” command. The location of initrd is /boot directory. 
        The kernel version for which the initrd image is being created needs to be passed as an argument to the mkinitrd command.
            #mkinitrd /boot/initrd-latest.img $(uname -r)
            
    * How initram disk depends on kernel version?
        The kernel converts initrd into a “normal” RAM disk and frees the memory used by initrd
        
    * If the physical server is keep rebooting then how will you troubleshoot? Hint: the boot order may check.   
    * Why the size of MBR is 512 bytes? Explain the different components like partition table, segment, magic no    
    * How to troubleshoot  if MBR is currpted?
    * What is pxe boot? How it works?
    * What are the components required to set up PXE boot or how to setup PXE boot?
    
    
    







