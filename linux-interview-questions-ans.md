## Linux Interview Questions & Answers

#### 1. What is Linux?
**Answer.** Linus Torvalds developed Linux, a Unix-like, free, open-source, and kernel operating system. Mainly it is designed for systems, servers, embedded devices, mobile devices, and mainframes and is also supported on major computer platforms such as ARM, x86, and SPARC.

#### 2. Explain the basic features of the Linux OS.
**Answer.** Some basic features of Linux are:

Linux is free and easily available.
It is more secure than other operating systems because it uses security auditing and password authentication features.
Linux has its personal software repository.
It includes multiple languages throughout the world. Hence Linux supports different language keyboards.
It offers CLI and GUI to use different commands and applications such as Firefox, VLC, etc.

#### 3. Name some Linux Distros
**Answer.** There are various Linux distros but the following are the most commonly used:
- Ubuntu
- Debian
- CentOS
- Fedora
- RedHat

#### 4. What are the major differences between Linux and Windows?
**Answer.** The following table will help in understanding the differences between Linux and Windows:

| Comparison Factor | Linux  | Windows  |
| ------- | --- | --- |
| Free/Paid | It is a free and open-source OS. | It is not open-source and is free to use. |
| Security | Linux is highly secure. | Windows is less secure compared to Linux. |
| Path separator | As a path separator, it uses a forward slash. | Windows uses a backward slash between the directories. |
| Efficiency | Linux is more efficient than Windows. | Windows is less efficient. |
| Kernel type | It uses a monolithic kernel. | It uses a microkernel.|
| File system | Linux file systems are case-sensitive.| Its file system is case-insensitive. |

#### 5. Define the basic components of Linux.
**Answer.** Majorly there are five basic components of Linux:

**Kernel:** Linux kernel is a core part of the operating system that works as a bridge between hardware and software.

**Shell:** Shell is an interface between a kernel and a user.

**GUI:** Offers different way to interact with the system, known as the graphical user interface (GUI).

**Application programs:** It is designed to perform a bundle of tasks through a bundle of functions.

**System Utilities:** It is the software functions through which users manage the system.

#### 6. Elaborate all the file permission in Linux.
**Answer.** There are three types of file permissions in Linux:

- Read: Users open and read files with this permission.
- Write: Users can open and modify the files.
- Execute: Users can run the file.

#### 7. What is the Linux Kernel? Is it legal to edit it?
**Answer.** It is known as a low-level software system. The Linux kernel tracks the resources and provides a user interface. This OS is released under GPL (General Public License). Hence every project is released under it. So, you can edit the Linux kernel legally.

#### 8. Explain LILO
**Answer.** LILO, i.e., Linux Loader and is a Linux Boot loader. It loads the Linux operating system into memory and starts the execution. Most operating systems like Windows and macOS come with a bootloader. While in Linux, you need to install a separate boot loader, and LILO is one of the Linux boot loaders.

#### 9. What is Shell in Linux?
**Answer.** In Linux, five Shells are used:

- csh (C Shell): This shell offers job control and spell checking and is similar to C syntax.
- ksh (Korn Shell): A high-level shell for programming languages.
- ssh (Z Shell): This shell has a unique nature, such as closing comments, startup files, file name generating, and observing logout/login watching.
- bash (Bourne Again Shell): This is the default shell for Linux.
- Fish (Friendly Interactive Shell): This shell provides auto-suggestion, web-based configuration, etc.

#### 10. What is a root account?
**Answer.** The root is like the user’s name or system administrator account in Linux. The root account provides complete system control, which an ordinary user cannot do.

#### 11. Describe CLI and GUI in Linux.
**Answer.** CLI, i.e., command line interface. It takes input as a command and runs the tasks of the system. The term GUI refers to the Graphical User Interface or the human-computer interface. It uses icons, images, menus, and windows, which can be manipulated through the mouse.

#### 12. What is Swap Space?
**Answer.** Linux uses swap space to expand RAM. Linux uses this extra space to hold concurrently running programs temporarily.

#### 13. What is the difference between hard links and soft links?
**Answer.** Here is the table that shows the difference between soft links and hard links:
| Hard Links  | Soft Links  |
| --- | --- |
| It includes original content Links.  | It includes the original file location.  |
| Hard links are faster as compared to soft links.| Soft links are slower.|
| It shares similar inode numbers.  | It shares different inode numbers.  |
| There is no relative path for hard links. | Relative paths are used for soft links. |
| It didn’t link the directories.  | It links the directories. |
| Any change in this link reflects other files directly. | Every change in this link reflects its hard link and the actual file directly.|
| It uses less memory. | It uses more memory. |

#### 14. How do users create a symbolic link in Linux?
**Answer.** Symbolic links, symlink, or soft links are shortcuts to files and directories. Users can create the symbolic link in Linux through the’ ln’ command. The general command to create a symbolic link is as follows:
```
ln -s <existing_source file> <optional_symbolic link>
```

#### 15. What do you understand about the standard streams?
**Answer.** Output and input in Linux OS are divided into three standard streams: 

- Stdin (standard input)
- stdout(standard output)
- stderr (standard error)
Under Linux, these standard streams channel communication of output and input between programs and their environment.

#### 16. How do you mount and unmount filesystems in Linux?
**Answer.** In this case, you can use the ‘mount’ and ‘umount’ commands.

**For mounting:**
First, identify the partition through the fdisk -l command. You can also use the lsblk command for it.
After identifying the partition, create the directory which will work as the mount point. For example, running the mkdir /mnt/mountpnt will create the mountpnt directory as the mount point.
Finally, you can run sudo mount <partition> <mount_point_directory> to complete the mounting.

**For Unmounting:**
Once you check if the specific filesystem is in use, you can run the `sudo umount <mount_point_directory>` for unmounting.

#### 17. How do you troubleshoot network connectivity issues in Linux?
**Answer.** There are multiple ways to troubleshoot the network connectivity and find the issue correctly:

**Check the Internet Connectivity:** First of all, please check if the internet connection option is on and also check the cables to find if there is any issue with it.

**Verify the Network Configuration:**
Please check that your network is configured correctly and the network interface has your IP address. You can check it by running the ip addr or ifconfig commands.
You can also run the ip route command to check if the default gateway is set properly.
Finally, verify the DNS server configuration in the /etc/resolv.conf file.

**Check the Firewall:**
Sometimes, firewall rules block the internet connection for the system’s security. Hence, you can run the ufw or iptables command to modify the firewall rules.

**Network Interface:**
You can restart your network interface through the ifup and ifdown commands. Once you restart the network interface, please reboot the system to make changes successful.

#### 18. How do you list all the processes running in Linux?
**Answer.** You can list the currently running process in Linux through various commands such as:

**ps Command:**
The ps command displays brief information about the running processes. You can use the ps -f or ps -ef command because the -f option shows the full-format result, and the -e option displays all processes. Moreover, you can use the ps auxf command to get a detailed list of processes.

**top and htop Command:**
The top command displays the real-time details about the system process and the complete resource usage.
The htop command is the improved version of the top command because it displays the color-coded list with additional features such as sorting, filtering, etc.

#### 19. What is the chmod command in Linux, and how do you use it?
**Answer.** You can use the chmod command to change the file permissions of the directories. It offers a simple way to control the read and write permissions. For instance, if you want to change the permission of the ABC.sh script and give it the write and executable permission, you can run the below command:

`chmod u+wx ABC.sh`

The chmod command is not limited to the write (w), read (r), and executable (x) permissions because there are symbolic modes and numeric modes, which you can learn from this guide.

#### 20. How do you check disk space usage?
**Answer.** There are some simple commands you can use to check disk space usage, such as:

**df Command:**
The df or disk-free command shows the used and the available disk space. You can use the additional options to check disk space differently. For instance, you can use the df -h command to check the disk usage in the human-readable format.

**du Command:**
The du or disk usage command estimates and shows the disk space usage, so running the du command with no option shows the disk usage of your current directory. However, you can run the following command to check the disk usage of a specific directory:

`du -sh ~/<directory> `

**ncdu Command:**
The NCurses Disk Usage, or ncdu command, displays more interactive disk usage. Similar to the du command, the ncdu command also requires the path of the specific directory to check its space.

#### 21. How do you find the process ID (PID) of a running process?
**Answer.** You can use the following command to find the Process ID or PID of the currently running process:

**pgrep Command:**
The pgrep command shows the PID of a process through its name or other different attributes. For example, you can find the PID of process_1 using the below command:

`pgrep <process_1>`

**ps Command:**
ps command not only displays the currently running process but also shows the process’s PID. However, if you want to check the PID of a specific process, you can combine the ps with the grep command:

`ps -e | grep -i <process_1>`

#### 22. What is the rsync command, and how do you use this command for synchronization?
**Answer.** The rsync command is used to synchronize and transfer the files in Linux. It synchronizes files between two local systems, directories, or a network. The basic rsync command contains the following:

`rsync <options> <source> <destination>`

For example, let’s synchronize between Documents and the Downloads directory. For this, you need to run the following command:

`rsync -av ~/Documents ~/Downloads`


If you want to go one step further, then you can use the below command:

`rsync -avz --delete ~/Documents ~/Downloads`

In the above command:
- The -a option preserves all the permissions and other attributes.
- The -v option displays the detailed output of the synchronization
- The -z allows compression that decreases the bandwidth use.
- The –delete option removes the file in the Downloads that do not exist in the Documents directory.

#### 23. How do you create a user account?
**Answer.** You can use adduser and useradd commands to create a user for the system.

`useradd Command:`

Let’s create a username, “Ron,” and provide a password for accessing the system:
```
useradd Ron 
passwd Ron 
```

You can also explore the useradd command’s additional options to modify the new user’s permissions and privileges.

`adduser Command:`

The adduser command is similar to the useradd command, so let’s create a username “Shawn”:
```
adduser Shawn
passwd Shawn
```

#### 24. How do you format a disk in Linux?
**Answer.** The mkfs or make file system command helps format the disk in the Linux system. All you need to do is use the following method to format the disk:

First, run the lsblk command to list the available partitions and identify which disk you want to format.

If the selected disk is mounted, then unmount it through the following command:

`umount <partition>`

Now, find the file system type of the disk, like EXT4, NTFS, or XFS. Once you are done then, run one of the following commands according to the file system type:
```
mkfs.ext4 <partition>
mkfs.xfs <partition>
mkfs.ntfs <partition>
```
Finally, mount the disk again through the mount command after the successful format. Moreover, please ensure that you have created a complete disk backup to eliminate the chances of data loss.

#### 25. How do you change the password for a user account?
**Answer.** Changing the password of a user account is simple because all you need to do is use the passwd command:

`passwd username`

For example, let’s change the password of a user “Ron” through the below command:

`passwd Ron `

Once you run the command, the system will ask you to enter and confirm the new password.

#### 26. What is the difference between a process and a thread?
**Answer.** In Linux, processes are the independent program, while a thread is the unit of execution. So here are the complete differences between process and thread:
| Comparison Factors  | Process  | Thread |
| --- | --- | --- |
| Creation time  | Creation time is higher  | Creation time is less. |
| Dependency | It is independent because it does not share memory. | It depends on other threads because they share some memory with other threads. |
| Resource  | Resource use is higher  | Requires lesser resources |
| Termination time | The termination time is higher | The termination time is less. |

#### 27. What is the ulimit command, and how do you use it?
**Answer.** The ulimit command controls the resource limit for the user process. You can use the ulimit command to set the limit on the system resource to prevent consuming the higher resources. This command contains multiple options to set the limit. For example, you can use the u option to set a maximum number of processes to 50:

`ulimit -u 50 `

#### 28. What is the find command, and how do you use it?
**Answer.** The find command searches for files based on different factors such as name, size, permissions, etc. Here is the basic command:

`find <directory> <file>`

For example, let’s find a Linux.txt file located in the Downloads directory through the below command:

`find ~/Downloads -name Linux.txt`

Once you run the above command, the find command will start finding the Linux.txt in the Downloads directory and subdirectories.

#### 29. What is RAID in Linux?
**Answer.** The full form of RAID is the Redundant Array of Independent Disk that allows the system to combine the different physical disk drives into a logical unit. RAID is used to improve the system’s disk performance and data integrity. There are different RAID levels you can configure according to the requirements. Here is the detailed information about the RAID levels:
| RAID Level  | Description  |
| --- | --- |
| RAID 0  | It is called striping, which allows you to split the data into multiple disks without redundancy.  |
| RAID 1 | It is called mirroring, which allows you to create a complete copy of data on multiple disks. |
| RAID 5  | It distributes the parity information and data on multiple disks.  |
| RAID 6 | It is the improved version of RAID 5 as it uses two sets of parity information to provide higher data redundancy. |
| RAID 10 | It combines RAID 0 and RAID 1 to generate the set of mirror disks to improve performance and redundancy. |

#### 30. What are the challenges of using Linux?
**Answer.** There are numerous challenges that a user faces while using Linux:

- Linux shows hardware compatibility issues in certain devices because manufacturers prioritize Windows compatibility.
- Learning Linux is not easy because the configuration and commands require proper knowledge.
- Although Linux supports Steam, it still needs to be impressed regarding game compatibility and availability.
- Sometimes users face driver and firmware-related issues.

#### 31. What is the /proc file system?
**Answer.** /proc (Proc File System) is the virtual file system that shows information about the system and the Kernel data structures. It is the essential interface to access the system, perform debugging tasks, check the Kernel functioning, find process-related information, and many more.

Therefore, you can use /proc file system in Linux to get information about the system and modify the particular Kernel parameters at the runtime.

#### 32. How do you secure a Linux server?
**Answer.** There are multiple methods to secure the Linux server and protect it from data breaches, security threats, and unauthorized access. Here are some of these methods:

- Create a strong password.
- Update the server and apply security patches.
- Use secured protocols like SSH and configure it to use key-based authentication for higher security.
- Use the intrusion detection system (IDS) to monitor network traffic and prevent malicious activities.
- Configure the firewall to limit the inbound and outbound traffic on the server.
- Disable all unused network services.
- Create regular backups.
- Review logs and perform regular security audits.
- Encrypt network traffic and enable monitoring.

#### 33. What is strace command?
**Answer.** The strace command is the diagnostic utility by which you can trace and monitor the system calls generated by the process. It allows you to find how programs interact with Kernel and can be used for debugging and troubleshooting. For example, let’s find the system calls generated by the ls command:

`strace ls`

Once you run the above command, the system will start tracing the list command and show the system calls generated by it. Output from the above command includes information like call name, argument, and return values.

#### 34. How do you optimize Linux system performance?
**Answer.** You can optimize the Linux performance through various strategies to improve resource usage and efficiency. So some of the strategies are:

- Updates the system as per the latest one available.
- Optimize the disk, enable the caching, and optimize the access pattern.
- Manage memory and CPU usage.
- Disable the necessary services and use lightweight alternatives of the tools.
- Monitor the system resources regularly.
- Perform the Kernel parameter tune-up.
- Use tools like Performance Co-Pilot (PCP) to monitor system-level performance.

#### 35. How to administer Linux servers?
**Answer.** Administering a Linux server requires different strategies and management to maintain the overall functionalities. Here are some major strategies you can follow:

- Handle user account management and assign appropriate access permissions.
- Configure the system to optimize the performance, improve the security and maintain the network connectivity.
- Implement the backup strategy to perform regular backups of the server.
- Implement the monitoring tools to track resource usage, system performance, and network.
- Configure firewall, set up intrusion detection, manage user permissions and configure the SSH.
- Create a proper recovery planning that must include regular backup, critical configuration documentation, recovery process testing, and offsite storage.

#### 36. What is a Linux virtual memory system?
**Answer.** Virtual memory is a great memory management utility in any OS. You can use the virtual memory system as secondary memory. This memory is used by both software and hardware in Linux so that your system can cope with the lack of physical memory. Moreover, virtual memory is also used to compensate for the RAM usage by transferring the data temporarily from RAM to disk storage.

#### 37. What do you understand about process scheduling in Linux?
**Answer.** Process scheduling is the mechanism that identifies the order of processes running on the system. In other words, process scheduling determines the order and execution time of multiple processes running on the system concurrently. This process scheduler of Linux is priority-based and uses a preemptive algorithm. It allocates CPU time for different processes to ensure efficient CPU resource usage. These processes are dynamic, and their order can change depending on many factors, such as resource usage, process behavior, and scheduling policies.

#### 38. What are the most important Linux commands?
**Answer.** There are a ton of useful commands in Linux, and here are some of the commonly used commands:

- ls: Display directory contents such as folders and files.
- mkdir: Used to create a new directory.
- pwd: Shows the current directory.
- top: Display system running processes and resource usage.
- grep: Search a specific pattern in a file.
- cat: Through this command, users can add multiple files and also display the content of the files.
- tar: Archives directories and files into a tarball.
- wget: Download files from the browser or web.
- free: Shows memory usage.
- df: Shows disk space usage.
- man: Gives a manual page for a specific command that displays instructions and details.

#### 39. What is the iptables command, and how to use it for network filtering?
**Answer.** The iptables command configures Netfilter firewall rules providing the network address translation, packet filtering, etc. iptables inspects the network packet and then manages them according to the defined rules. Here is how you can use the iptables command for network filtering: 

Run the below command to display the current iptables rules, including policies, chains, and other actions for the network:

`iptables -L`

The iptables configuration uses the predefined set of chains to process the network packages at different stages. So you can define rules to these chains for manipulating the network packets:

`iptables -A <chain> <options> -j <target>`

In the above command:
```
<chain>: Specifies the chain where you want to define a new rule.
<options>: Defines the conditions for the rule, like ports, protocols, etc.
-j <target>: Defines the target action when the packet matches the rule.
```
By default, iptables rules get automatically removed after the system reboot, but you can use the following command to make the rules persistent:

`iptables-save > /etc/iptables/rules.v4`

#### 40. How do you troubleshoot a Linux OS that fails to boot?
**Answer.** In case of the system boot failure, you can follow various approaches such as:

- Check the warning and error messages you get during the boot process because it can help you diagnose the issues.
- Check the boot logs to find the exact reason behind the boot error.
- Open the GRUB bootloader and check the boot options to solve the booting problems.
- Check the hardware connections like cables, RAM, cooling fan, etc.
- If the system shows an error message related to the Kernel, try to boot it with the older Kernel version from GRUB.
- Identify the last changes you made in the system before the boot.

#### 41. What is the init process in Linux?
**Answer.** The init or also called the initialization process is the first process that begins during the system boot. It is responsible for initializing and processing the system in its functional state. Hence, init works as the parent process because its process ID is 1. Originally Linux systems used to have SysV init, but now it is developed as the systemd init (an improved version of SysV).

#### 42. What is SMTP?
**Answer.** SMTP stands for Simple Mail Transfer Protocol. This set of communication guidelines allows the software to transmit electronic mail online. The main aim of SMTP is to set communication rules between servers. There are two models of SMTP:
- End-to-end model: This model is used to connect different organizations.
- Store-and-forward model: This model is used within an organization.

#### 43. What is LVM in Linux?
**Answer.** The full form of LVM is Logical Volume Manager, which provides an advanced disk management approach in Linux. It is a subsystem that allows a user to efficiently allocate the disk space on the physical storage device.

You can use the LVM to create the logical volume for easy storage management through various features like resizing, volume mirroring, and snapshots. LVM is a powerful utility for disk management where you need dynamic storage allocations.

#### 44. What is the difference between UDP and TCP?
**Answer.** The following table shows the difference between UDP and TCP:
| Factors | UDP | TCP |
| --- | --- | --- |
| Connection-oriented | UDP does not establish a proper connection. | TCP is connection-oriented because it establishes a connection between the sender and receiver. |
| Reliability | UDP does not provide a reliability mechanism. | It guarantees reliable data delivery by retransmitting corrupt packets or lost packets. |
| Usage | It is used in low overhead, speed, and real-time communication applications. | It is used where ordered data is delivered, and reliable data must be delivered. |
| Applications | Video/voice conferencing, DNS, online gaming, streaming media, etc. | File transfers, email, web browsing, database transactions, etc. |

#### 45. What is /etc/resolv.conf file
**Answer.** The /etc/resolv.conf is the config file used for the DNS server resolution process. This config file is used to specify the DNS server, set up the search directive for domains, and configure the resolver options.

#### 46. What is the difference between absolute and relative paths in Linux?
**Answer.** Absolute path = It specifies the exact location of a file or directory from the root directory (“/”). We will notice that they always start with a forward slash (“/”).

For Example: `/home/user/jayesh/geeksforgeeks.txt`

Relative paths = It specifies the location relative to the current working directory. In this we do not start with a forward slash (“/”).

For Example: `documents/file.txt`

#### 47. What is the grep command used for in Linux?
**Answer.** The grep command is used to search for specific patterns within files or input streams. It allows us to find and print lines that we give to match the pattern.

For example: If we want to search `test` in a text file name “file.txt”. We use the following command

`grep "test" file.txt`

This command will search for the word `test` in the file named “file.txt” and print the matching lines.

#### 48. How do you check the status of a service or daemon in Linux?
**Answer.** To check the status of a service or daemon, we can use the `systemctl` command followed by the service name.

For example: If we want to display the status of the Apache Web server. We use the following command.

`systemctl status apache2`

It will show whether the service is running, stopped, or in an error state.

#### 49. What is the difference between /etc/passwd and /etc/shadow files?
**Answer.** The /etc/passwd file stores essential user information like usernames, user IDs, home directories, and default shells. Each line in the file represents a user account.

The /etc/shadow file contains encrypted passwords and other security-related information. It is only accessible by the root user or privileged processes

#### 50. How do you compress and decompress files in Linux?
**Answer.** To compress files in Linux, you can use the tar command along with gzip compression.

For example: If we want to create a file name “jayesh” with gzip compression. We use the following command.

`tar -czvf jayesh.tar.gz files`

This command will create a compressed archive file containg the specified “files”

To decompress the same, we use the following command.

`tar -xzvf jayesh.tar.gz`

#### 51. What is the difference between a process and a daemon in Linux?
**Answer.** A process is an executing instance of a program. It can be a foreground process that interacts with the user or a background process started by a user or another process.

A daemon is a background process that runs independently of user sessions. It is typically started at system boot time and performs system tasks or provides services. Daemons often have no user interaction and continue running even when users log out.

#### 52. How do you schedule recurring tasks in Linux?
**Answer.** We can use `crontab` command for performing recurring tasks in Linux. By adding entries to the crontab file, we can specify when and how frequently a command or script should be executed

For Example: If we want to execute a script name “geeks.sh” every day at 3:30 AM. We use the following command.

crontab -e\
This command opens the crontab file in an editor.

30 3 * * * /path/to/geeks.sh

#### 53. What is the sed command used for in Linux?
**Answer.** The sed command is used to perform text transformations on files. It can search for specific patterns and replace them with desired text.

For Example:

`sed `s/foo/bar/g` file.txt`

This command replaces all occurrences of “foo” with “bar” in the file name “file.txt”

#### 54. What are runlevels in Linux?
**Answer.** Runlevels in Linux define different system states, such as single-user mode or multi-user mode with or without a GUI. They determine which services start or stop during system startup and shutdown. The default runlevel is often set to a multi-user mode with a GUI (runlevel 5). Runlevel 3 is commonly used for a multi-user mode without a GUI.

#### 55. What is sudo in Linux?
**Answer.** The word “sudo” is the short form of “Superuser Do” that allows you to run the command with system privileges. With this command, you can get the system’s administrative access to perform various tasks. The sudo command requires a password before the execution to verify the user’s authorization.

#### 56. What is umask?
**Answer.** It is used for user file creation mode. When a user creates any file, then it has default file permission. Umask specifies restrictions for these permissions on the file, i.e., controls the permissions.

#### 57. How to find and kill a process in Linux?
**Answer.** You can use different commands to kill a process, but first, you must find the PID of that specific process. So, please run the below command:

`ps aux | grep <process>`

Once you get the PID of the process then run the kill command to end it:

`kill <PID>`

If you don’t want to find the PID, then you can use the pkill command to kill a process by its name:

`pkill <process>`

The pkill command sends a signal (by default, SIGTERM) to the matched processes, causing them to terminate.

#### 58. What is network bonding in Linux?
**Answer.** Network bonding is the process of creating a single network by combining two or more network interfaces. This combination of networks improves redundancy and performance by increasing bandwidth and throughput. The major benefit of network bonding is that the overall network works fine even if a single network in the bonding does not work properly.

#### 59. What is SELinux?
**Answer.** SELinux or also known as Security-Enhanced Linux, is the security framework. It offers an additional layer of security to improve access control and strengthen security. SELinux was developed to improve the security policies to prevent unauthorized access and exploitation. However, learning about SELinux is essential before working on it can create serious security issues.

#### 60. What is the purpose of the SSH protocol in Linux, and how do you securely connect to a remote server using SSH?
**Answer.** The Secure Shell (SSH) is a protocol in Linux which is used to establish a secure encrypted connection between a local and remote machine. It allows to securely access and manage remote servers. If we want to connect to a remote server using SSH. We can use the following command.

`ssh username@remote_ip`

Here replace the `username` with the desired username of the remote server and replace the `remote_ip` with the IP address of the remote server.

#### 61. How do you check the contents of a file without opening it in Linux?
**Answer.** In Linux we can use the `cat` command to view the content of a file without opening it in an editor form.

For example: If we want to check content of a file with file_name = `geeks.txt`

`cat geeks.txt`

#### 62. What is the purpose of the crontab file in Linux, and how do you schedule recurring tasks using cron jobs?
**Answer.** The crontab file in Linux is used to schedule recurring tasks or cron jobs. It contains a list of commands or scripts that are executed at specified time intervals. To edit the crontab file, you can use the crontab -e command. 

For example: If we want to run a script name `jayesh.sh` every day at 5 AM, we can use the following procedure.

First, we need to open the crontab in editorial format.

crontab -e

Secondly, add the entries in the crontab file.

0 5 * * * /path/to/jayesh.sh

#### 63. How do you find and replace text in a file using the sed command in Linux?
**Answer.** The sed command (stream editor) can be used to find and replace text in a file. The basic syntax is sed ‘s/pattern/replacement/g’ filename.

For example: to replace all occurrences of “true” with “False” in a file

`sed 's/true/False/g' file_name`


#### 64. What is the purpose of the sudoers file in Linux, and how do you configure sudo access for users?
**Answer.** The sudoers file in Linux controls the sudo access permissions for users. It determines which users are allowed to run commands with superuser (root) privileges. To configure sudo access, you can edit the sudoers file using the visudo command. 

For example:

sudo visudo

Now add this line anywhere in the file. For instance, if we want to grant a user full sudo access.

user_name ALL=(ALL) ALL

#### 65. How do you change the ownership of a file or directory in Linux using the chown command?
**Answer.** In Linux, you can change the ownership of a file or directory using the chown command. The basic syntax is chown new_owner: new_group filename. 

For example: If we want to change the ownership of a file to user “Jayesh” and group “users”.

chown jayesh:users file_name

#### 66. What is the purpose of the ping command in Linux, and how do you test network connectivity to a remote host?
**Answer.** Ping command is used to test the network connectively between the local and remote hosts. It basically sends an ICMP echo request packet to the remote host and waits for the corresponding echo reply packet.

For example: If we want to check the connectivity to a remote host, we use the following command.

`ping remote_host_ip`

Here replace `remote_host_ip` with the Ip address of the host

#### 67. How do you recursively copy files and directories in Linux using the cp command?
**Answer.** In linxux we can simply use `-R` option with the `cp` command to recursively copy the file and directories.

For example: 

`cp -R sourece_durectory destination_directory`

#### 68. What is the purpose of the netstat command in Linux, and how do you view network connections and listening ports?
**Answer.** The netstat command in Linux is used to display active network connections, routing tables, and listening ports. To view network connections and listening ports, use the netstat command with appropriate options. 

For example: If we want to display all listening TCP ports, we can use the following command.

`netstat -tuln`

#### 69. How do you set up a static IP address in Linux using the command-line interface?
**Answer.** To set up a static IP address in Linux using the command-line interface, you need to modify the network configuration file. The location and name of the file may vary depending on the Linux distribution, but commonly it is /etc/network/interfaces. Open the file with a text editor and modify the configuration to set a static IP address, subnet mask, gateway, and DNS servers.

For example: 

- iface eth0 inet static
- address 192.168.1.100
- netmask 255.255.255.0
- gateway 192.168.1.1
- dns-nameservers 8.8.8.8 8.8.4.4

Save the file and restart the network service or reboot the system for the changes to take effect.

#### 70. How to copy a file to multiple directories in Linux?
**Answer.** We can copy a file to multiple directories in Linux by these methods and command xargs, find, tee and shell loop.

- xargs command on Unix/Linux operating system converts input from standard input into an argument list for a specified command.
- The command find initiates a search and allows actions to be performed based on the search results.
- The tee command reads standard input and copies it to both standard outputs and to one or more files.

#### 71. What is booting and explain are steps in detail (Linux/Windows).
#### 72. What is virtual memory & do why we need this in OS. Explain with real-life examples.
#### 73. If you are facing any issue with an internal server error, How you will troubleshoot?
#### 74. Linux Command for CPU memories and process troubleshooting with command.
#### 75. What are the “top“ command in Linux and the “star“ command.
#### 76. Use of Traceroute & Nslookup command.
#### 77. Few Linux questions-processing a log file and fetching for few error codes from debugging prints. Can be solved using cat and sed.
#### 78. Write a shell script for tasks performed in (c) —> I wrote a simple for loop command.
#### 79. Discussion on how to debug disk space issue in Linux
#### 80. Write a shell script to generate a report on 10 top space-consuming workspaces (folders) with consumption details—> again a simple for loop with df & du commands.
#### 81. Questions on file processing, solutions involved a cat, sed, awk, tail, head, grep -B, sort, unique, etc
#### 82. How would you debug if there is an issue with API output -> Discuss all the scenarios ranging from network connectivity to data in DB from where API fetches its data.
#### 83. OS boot process (Win/Linux)
#### 84. Memory management, Memory pages, Buffer, and Caches, Basic commands
#### 85. System date/time management, network time protocol
#### 86. Managing Users and groups
#### 87. File permissions
#### 88. Managing software – installation, uninstall, upgrade, etc.
#### 89. Managing system services and background processes
#### 90. Remote management of a system – SSH, RDP, etc.
#### 91. Network protocols – FTP, HTTP (web servers), SMTP (mail server)
#### 92. System automation – cron, batch jobs, windows startup tasks
#### 93. Booting Process in Detail.
Booting Process troubleshooting.
Bootable Device not found. Troubleshoot it.
SSH connection troubleshooting.
How do you check which ports are listening?
The device is slowing down, Troubleshoot it.
Commands to check for CPU Utilization.
TOP and SAR command in detail.
Paging Concept.
What are System calls?
Explain about fork().
Explain the Process life cycle or Process States.
How to check for Disk Free space.
I have disk space available but the file is not getting created. Why?
Explain the importance of inodes.
The device is Heating up. Troubleshoot it.
How do PING and TRACERT commands work?
Explain what happens when www.amazon.com is clicked.
Explain DHCP DORA Process.
Write a program for printing the permutations of a string.
