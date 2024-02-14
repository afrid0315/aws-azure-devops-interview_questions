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
**Answer.** A swap file or swap space is a portion of a computer's hard drive used as virtual memory when physical RAM is full. It prevents out-of-memory errors by temporarily storing inactive data. It's slower than RAM, so excessive swapping can impact performance. Proper configuration and sizing are important to maintain system stability without sacrificing performance.

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

#### 14. How do users create a symbolic link in Linux? What scenario you faced and how did you fix that?
**Answer.** Symbolic links, symlink, or soft links are shortcuts to files and directories. Users can create the symbolic link in Linux through the’ ln’ command. The general command to create a symbolic link is as follows:
```
ln -s <existing_source file> <optional_symbolic link>
```

Scenario: Suppose you have a symbolic link pointing to a file, and the target file gets deleted or moved. The symlink becomes a "dangling symlink," pointing to a non-existent location.

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

#### **29. What is RAID in Linux?
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

#### **36. What is a Linux virtual memory system? If its not present in hardware, how does it store data?
**Answer.** Virtual memory is a great memory management utility in any OS. You can use the virtual memory system as secondary memory. This memory is used by both software and hardware in Linux so that your system can cope with the lack of physical memory. Moreover, virtual memory is also used to compensate for the RAM usage by transferring the data temporarily from RAM to disk storage.

**Real-Life Example:**
Imagine you're working on a computer with limited RAM, and you have multiple applications open simultaneously. Virtual memory allows the operating system to use a portion of the hard disk as if it were additional RAM. When the physical RAM becomes fully occupied, less frequently used data is moved to the disk, making room for actively used data in RAM. This enables you to run more applications than the physical RAM would otherwise allow, preventing system slowdowns or crashes.

If virtual memory is not supported by hardware, the operating system would rely solely on software-based techniques to manage memory. In such a scenario, the operating system would still use disk storage as an extension of RAM when needed, but it would handle all memory management tasks without hardware assistance. This could involve techniques such as swapping, where parts of the program's memory are temporarily moved to disk when not actively in use, and then brought back into RAM when needed again. However, without hardware support like a Memory Management Unit (MMU), these operations might be less efficient and more reliant on CPU processing power.

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

#### 39. If you are facing any issue with an internal server error, How you will troubleshoot?
**Answer.** To troubleshoot an internal server error:
- Check Logs: Examine server logs for errors.
- Review Code: Look into recent code changes.
- Verify Permissions: Ensure correct file permissions.
- Test Components: Isolate and test components.
- Review Configuration: Check server configuration files.
- Update Software: Ensure all software is up-to-date.

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

#### 66. 

#### 67. How do you recursively copy files and directories in Linux using the cp command?
**Answer.** In linux we can simply use `-R` option with the `cp` command to recursively copy the file and directories.

For example: 

`cp -R sourece_durectory destination_directory`

#### 68. Let's say SSH is not working for some reason. How would you go over troubleshooting it?
**Answer.** To troubleshoot SSH connectivity issues, you can start by checking if the SSH service is running on the server, ensuring the correct port is open in the firewall, verifying network connectivity, checking SSH configuration files for errors, and reviewing SSH server logs for any error messages. Additionally, testing SSH connections from different client machines and using diagnostic tools like telnet or nc can help identify and resolve the problem.

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

#### **71. What is booting and explain are steps in detail (Linux/Windows).
**Answer.** 
Booting is the process of initializing a computer's operating system and making it ready for use.

**Linux Boot Process:**

- BIOS/UEFI: The computer's firmware (BIOS or UEFI) performs a Power-On Self-Test (POST) and initializes hardware.
- Boot Loader (GRUB): The boot loader, such as GRUB, loads the Linux kernel into memory from the boot partition.
- Linux Kernel Initialization: The kernel initializes hardware, mounts the root file system, and starts the init process.
- Init Process: The init process (or a modern equivalent like systemd) initializes user space components, services, and runs startup scripts.

**Windows Boot Process:**

- Power-On Self-Test (POST): Hardware is tested during POST, and the system's firmware (UEFI or BIOS) is activated.
- Boot Loader (Windows Boot Manager): The boot loader, often Windows Boot Manager, loads the Windows Boot Configuration Data (BCD) and presents a menu if multiple OS options exist.
- Windows Kernel Initialization: The Windows kernel (ntoskrnl.exe) is loaded into memory and initializes essential system components.
- Session Manager (Wininit.exe): The Session Manager starts, initializing system processes and drivers.
- Winlogon and User Initialization: Winlogon starts, and user-specific processes and services are initiated.
- User Interface: The graphical user interface (GUI) is presented, and the user can log in.

In both cases, the boot process involves initializing hardware, loading the operating system's kernel, and transitioning from a pre-boot environment to a fully functional user environment.

#### 72. What is the iptables command, and how to use it for network filtering?
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

#### 73. Managing system services and background processes.
**Answer. Managing System Services and Background Processes:**

- Use service management commands like systemctl (systemd) or service (SysV).
- Start, stop, restart, or enable/disable services.
- Monitor processes with commands like ps or top.
- Background processes using & at the end of a command.
- Manage cron jobs for scheduled tasks.
- Utilize tools like nohup to run processes immune to hangups.
  
#### **74. Linux Command for CPU memories and process troubleshooting with command.
**Answer.** To troubleshoot CPU, memory, and processes in Linux:

**CPU Usage:**

- Use top or htop command to view real-time CPU usage.
- mpstat provides CPU usage statistics.
- sar: Collects and reports system activity information, including CPU usage.
- vmstat: Reports system resource usage, including CPU utilization.
- pidstat: Reports statistics for Linux processes, including CPU usage.
  
**Memory Usage:**

- Check memory usage with free command.
- Analyze detailed memory info using vmstat or htop.

**Process Management:**

- View running processes with ps command.
- Investigate detailed process information with pidstat.
- Kill a process using kill or pkill.
- Monitor process activity using strace or lsof.

#### 75. SSH connection troubleshooting.
**Answer. SSH Connection Troubleshooting:**

- Check Network Connectivity:
- Verify if the server is reachable.
- Ensure the SSH service is running on the server.
- Confirm that firewalls allow SSH traffic.
- Use correct username and password/key.
- Verify SSH server configuration.
- Ensure correct permissions for SSH keys.
- Check server logs for SSH errors.
- Verify SSH is running on the correct port (default is 22).
- Ensure client and server have compatible SSH versions.
- Try connecting from a different SSH client.
- Use -v or -vv with ssh for detailed debugging output.

#### 76. If the server appears to be running correctly in the AWS console, and you've confirmed that the inbound rules and security group settings allow port 22 and the instance is in a public subnet is correct. But, system is still not working. Any commands you can run to check where might be the issue lying with this?
**Answer.** Check SSH service status: ``sudo systemctl status ssh``
Verify SSH port connectivity: ``telnet <server_ip> 22``
Review system logs for SSH-related errors: ``sudo journalctl -u sshd``

#### 77. Processing a log file and fetching for few error codes from debugging prints. Can be solved using cat and sed.
**Answer. Processing Log File with cat and sed in Linux:**
- Use cat to display log content.
- Employ sed to filter specific lines, e.g., for error codes.
- Example: `cat logfile.txt | sed -n '/ERROR/p'` fetches lines containing "ERROR" from the log.

#### 78. You ping it you get a response right? What does that mean?
**Answer.** When you ping a server or device and receive a response, it means that the target device is reachable over the network and is responding to ICMP (Internet Control Message Protocol) echo requests. This indicates that there is connectivity between your computer and the target device.

#### 79. How do you check which ports are listening?
**Answer.** 
Checking Listening Ports:
- Use netstat -tulpn or ss -tulpn to display listening ports.
- Alternatively, use lsof -i to list open ports and associated processes.
- nmap can scan for open ports on a remote system.
  
#### 80. Write a shell script to generate a report on 10 top space-consuming workspaces (folders) with consumption details—> again a simple for loop with df & du commands.
**Answer.** 
```
#!/bin/bash

# Shell script to generate a report on top 10 space-consuming workspaces

echo "Top 10 Space-Consuming Workspaces:"
echo "---------------------------------"

# Loop through directories and calculate space consumption
for dir in /*; do
    if [ -d "$dir" ]; then
        space_consumed=$(du -hs "$dir" 2>/dev/null | awk '{print $1}')
        echo "$dir: $space_consumed"
    fi
done | sort -hrk 2 | head -n 10
```

#### 81. TOP and SAR command in detail. 
**Answer.** 
**TOP Command:**
- top provides real-time system resource monitoring.
- Displays CPU usage, memory, processes, and more.
- Interactive interface for dynamic updates.
- Press 'q' to exit.

**SAR Command:**
- sar (System Activity Reporter) collects, reports, and saves system activity data.
- Captures CPU, memory, disk, and network usage.
- Useful for performance analysis and historical data.
- Example: sar -u shows CPU usage.
  
#### 82. How would you debug if there is an issue with API output -> Discuss all the scenarios ranging from network connectivity to data in DB from where API fetches its data.
**Answer.** 
- Verify if the server hosting the API is reachable.
- Check for any network issues or firewalls blocking communication.
- Confirm the API service is running and accessible.
- Check server logs for errors related to the API.
- Ensure the API endpoint is correct.
- Verify the HTTP method (GET, POST, etc.) and parameters.
- Check if proper authentication tokens or API keys are provided.
- Confirm the user has the necessary permissions.
- Ensure the database from which the API fetches data is accessible.
- Check database logs for errors or slow queries.
- Inspect the data in the database to ensure it is accurate and up-to-date.
- Confirm that the API response matches the expected data.
- Validate that the API response adheres to the expected format (JSON, XML, etc.).
- Check for any error messages or unexpected data.
- Examine the HTTP status codes returned by the API (e.g., 200 for success, 404 for not found).
- Different status codes provide insights into the nature of the issue.
- Confirm if the API has rate limits, and ensure they are not exceeded.
- Check for rate limit-related error responses.
- If using a proxy or CDN, check for misconfigurations or issues affecting data transmission.

#### **83. Paging Concept.
**Answer.**

**Memory Management Technique:**
- Breaks physical memory into fixed-size blocks called pages.
- Logical memory divided into same-sized pages.
- Address Translation:
- Operating system maintains a page table for mapping logical to physical addresses.
- Allows non-contiguous allocation of memory.
**Advantages:**
- Efficient use of physical memory.
- Simplifies memory allocation and management.
- Used in Virtual Memory Systems.

#### 84. Explain what happens when www.amazon.com is clicked.
**Answer.** The browser initiates a Domain Name System (DNS) lookup to translate the human-readable domain (www.amazon.com) into an IP address.
- The browser sends an HTTP GET request to the IP address obtained from DNS, specifying the path ("/" in the case of the homepage).
Server Processing
- Amazon's web server receives the request, processes it, and generates an appropriate response.
- The server sends back an HTML page along with additional resources (images, stylesheets, scripts, etc.) required to render the page.
- The browser receives the response, parses the HTML, and starts rendering the webpage. It may make additional requests for linked resources.
- JavaScript on the page might make further requests for dynamic content or interact with the server asynchronously.
- The browser combines all elements and displays the complete Amazon webpage, allowing the user to interact with it.
- This process involves multiple network interactions, server processing, and client-side rendering to provide a seamless user experience when accessing www.amazon.com.

#### 85. System date/time management, network time protocol
**Answer. System Date/Time Management:**
Linux manages date and time through the system clock. The date command allows users to display and set the system date and time. System time is maintained using Coordinated Universal Time (UTC), and the time zone is configured in the /etc/localtime file.

**Network Time Protocol (NTP):**
NTP is a protocol used to synchronize system clocks over a network. In Linux, the NTP daemon (ntpd) or the more modern chrony is commonly used. Configuration files such as /etc/ntp.conf or /etc/chrony.conf define NTP server settings. NTP helps maintain accurate and synchronized time across a network, crucial for various system operations and applications.

#### 86. Explain the Process life cycle or Process states.
**Answer.** The process life cycle, or process states, describes the various stages a process goes through during its execution:

- New: The process is being created.
- Ready: The process is waiting to be assigned to a processor for execution.
- Running: The process is currently being executed on a processor.
- Blocked (Wait): The process is waiting for an event (e.g., I/O operation) to occur.
- Terminated (Exit): The process has finished execution or has been terminated by the operating system.

These states represent the dynamic progression of a process as it interacts with the operating system and other system resources.

#### **87. What are System calls?
**Answer.** System calls are functions provided by the operating system that enable applications to request services from the kernel, such as file I/O, process creation, and network communication. These calls provide a controlled interface between user-level programs and the underlying hardware, allowing processes to perform privileged operations in a secure manner. Examples include open(), read(), write(), and fork().

#### 88. What is inode or Explain the importance of inodes.
**Answer.** An inode, short for index node, is a data structure in a file system that stores information about a file or a directory. It includes metadata such as file permissions, ownership, size, and pointers to the actual data blocks on the disk. Inodes enable the operating system to manage and locate files efficiently.

#### 89. I have disk space available but the file is not getting created. Why?
**Answer.**
- Check if the user has the necessary permissions to create files in the specified directory.
- Verify if there are filesystem quotas in place, restricting the amount of space a user can use.
- Ensure that the filesystem has available inodes. Sometimes, even with space available, if there are no available inodes, you can't create new files.
- Check if there is a disk quota limit for the user, and the limit has been reached.
- Examine the filesystem for any corruption that might prevent file creation.
- Confirm that the filesystem supports the creation of files.
- Verify that the disk where the file is being created is mounted and accessible.

#### 90. What is postfix? why we use?
**Answer.** Postfix is a mail transfer agent (MTA), which is a software application responsible for routing and delivering email messages. Postfix is commonly used as a mail server to handle the sending, receiving, and delivery of emails within a network or over the Internet. Postfix is a popular and widely used MTA in the Unix/Linux community due to its reliability, performance, and security features. It is often used in conjunction with other components like Dovecot (for IMAP/POP3 services) and various spam filtering tools to create a comprehensive email server solution.

#### 91. By aws cli in linux post how can i know about distribution? 
**Answer.** To determine the Linux distribution on a system using the command line. By using below command we can check
``
cat /etc/os-release
``

#### 92. What is iostat?
**Answer.** iostat is a command-line utility that provides detailed statistics about CPU, I/O, and disk utilization on Linux systems. It is a part of the sysstat package, which needs to be installed on your system to use iostat. The iostat command can be useful for monitoring system performance and identifying performance bottlenecks.

#### 93. What are logical volumes in linux and how to create?
**Answer.** Logical volumes in Linux are a part of the Logical Volume Manager (LVM) system, allowing for dynamic disk space management. Logical volumes provide a flexible way to allocate and resize storage on Linux systems.

To create a logical volume:

- Initialize Physical Volumes: Use pvcreate to initialize the physical volumes (disks or partitions).
- Create a Volume Group: Use vgcreate to create a volume group, grouping one or more physical volumes.
- Create Logical Volumes: Use lvcreate to create logical volumes within the volume group, specifying size and other parameters.
- Format the Logical Volume: Use a command like mkfs to format the logical volume with the desired filesystem.
- Mount the Logical Volume: Use mount to mount the logical volume to a specific directory.
```
# Assuming /dev/sdb1 is a partition to be used as a physical volume
pvcreate /dev/sdb1
# Create a volume group named myvg
vgcreate myvg /dev/sdb1
# Create a logical volume named mylv with 10GB size
lvcreate -L 10G -n mylv myvg
# Format the logical volume with ext4 filesystem
mkfs.ext4 /dev/myvg/mylv
# Mount the logical volume to /mnt/mylv
mount /dev/myvg/mylv /mnt/mylv
```

#### 94. What is swap and buffer in linux?
**Answer. Swap:** Reserved space on disk used as virtual memory when physical RAM is full. Created to prevent system crashes due to memory exhaustion. 

**Buffer:** Temporary storage in RAM for I/O operations. Improves efficiency by holding data in memory before being written to or after being read from disk. Both enhance system performance but serve different purposes. Swap aids memory management, while buffers optimize I/O operations.

#### 95. How to monitor the linux files for any changes?
**Answer.** To monitor Linux files for changes, you can use the inotifywait command:
```
inotifywait -m -r -e modify,create,delete /path/to/directory
```
This command continuously monitors the specified directory (/path/to/directory) and reports any modifications, creations, or deletions of files. Adjust the options and events based on your monitoring needs.

#### 96. What is ctime and mtime in linux?
**Answer. ctime (change time):** 
Represents the last time metadata of a file (permissions, ownership) was changed. Altered when the file's metadata is modified.

**mtime (modification time):**
Indicates the last time the content of a file was modified. Changes when the file's actual data is updated. Both timestamps are part of a file's metadata and can be viewed using the stat command.

#### 97. Why nohup and & are used?
**Answer. nohup:**
Prevents a command from being terminated when the terminal is closed. Example: nohup command.

**& (ampersand):**
Runs a command in the background, allowing the terminal prompt to be used for other commands. Example: command & Together (nohup command &), they allow a command to run in the background and persist even if the terminal session is closed.

#### 98. What will happen if you get no space left on device?
**Answer.** If a system runs out of space on a device, it can lead to critical issues. Applications may fail to write data, logs, or temporary files, causing disruptions or crashes. System processes may malfunction, and essential services may become unavailable. It's crucial to regularly monitor disk space, implement proper alerting, and take proactive measures such as cleaning up unnecessary files or expanding storage capacity to avoid these situations.

#### 99. What is DNS caching?
**Answer.** DNS caching is the temporary storage of DNS (Domain Name System) query results by a system or network device. It helps improve efficiency and reduce latency by storing previously resolved domain names and their corresponding IP addresses, allowing quicker retrieval of this information without the need to repeatedly query DNS servers for the same data.

#### 100. What is HA Proxy LBR?
**Answer.** "High Availability Proxy Load Balancer," it generally means a High Availability (HA) configuration of the HAProxy load balancer. This setup is designed to provide continuous availability, fault tolerance, and efficient distribution of incoming network traffic across multiple servers.

#### 101. What is Sticky bit?
**Answer.** The sticky bit is a permission in Unix file systems that, when set on a directory, restricts the deletion or renaming of files within that directory to only the file owner. It is often represented by the letter "t" like this **"drwxrwxrwt for /tmp"** in the execute permission for others. This is commonly used on directories like /tmp to prevent users from deleting or renaming each other's files.

#### 102. How can you create a zero byte file using which command
**Answer.** You can create a zero-byte file using the touch command: ``touch filename``

#### 103. What is thread in OS?
**Answer.** A thread in an operating system is the smallest unit of execution within a process. It represents a single sequential flow of control within the process. Threads share the same memory space and resources of the process they belong to, enabling concurrent execution of multiple tasks within that process. Threads can execute independently, allowing for parallelism and multitasking within a program.

#### 104. How to check the services running in Linux tell the command? 
**Answer.** To check the services running in Linux, you can use the systemctl command. Use the following command to list all running services: ``systemctl list-units --type=service --state=running``

#### 105. Using which command will you list out all the empty files in Linux?
**Answer.** To list all empty files in Linux, you can use the find command along with the -empty option.
``find /path/to/directory -type f -empty``

#### 106. How to add volume permanently in linux/windows server?
**Answer.** To add a volume permanently in Linux, you need to edit the /etc/fstab file. Add an entry specifying the details of the volume, such as device, mount point, file system type, and options.``/dev/sdb1   /mnt/myvolume   ext4   defaults   0   0``

#### 107. Write python or shell script to mdify the cloud formation stack?
**Answer.** For python
```
import boto3

# Replace with your AWS credentials and region
aws_access_key = 'your_access_key'
aws_secret_key = 'your_secret_key'
region = 'your_region'

stack_name = 'your_stack_name'
parameter_key = 'ParameterKey'
parameter_value = 'NewValue'

# Create a CloudFormation client
cf_client = boto3.client('cloudformation', aws_access_key_id=aws_access_key, aws_secret_access_key=aws_secret_key, region_name=region)

# Get the current stack description
response = cf_client.describe_stacks(StackName=stack_name)
stack_description = response['Stacks'][0]

# Extract the current parameter values
current_parameters = stack_description['Parameters']

# Update the parameter value
for param in current_parameters:
    if param['ParameterKey'] == parameter_key:
        param['ParameterValue'] = parameter_value

# Modify the stack with the updated parameters
cf_client.update_stack(
    StackName=stack_name,
    UsePreviousTemplate=True,
    Parameters=current_parameters
)

print(f"Stack {stack_name} updated successfully.")
```

For Shell Script
```
#!/bin/bash
stack_name='your_stack_name'
parameter_key='ParameterKey'
parameter_value='NewValue'

aws cloudformation update-stack \
    --stack-name $stack_name \
    --use-previous-template \
    --parameters ParameterKey=$parameter_key,ParameterValue=$parameter_value

echo "Stack $stack_name updated successfully."
```

#### 108. Port number for tomcat? Can you use another port number and what is the path for how to change number?
**Answer.** The default port number for Apache Tomcat is 8080. You can change the port number by modifying the server.xml configuration file. Locate the server.xml file in the conf directory of your Tomcat installation. Most software packages, configuration files related to port numbers are often found in a "conf" (configuration) directory.

#### 109. Do you know how to be setting file path?
**Answer.** Yes, setting a file path involves specifying the location of a file. In various programming languages or systems, you can set file paths using variables, constants, or configuration files. Always consider the appropriate syntax for the specific language or environment you're working in.

#### 110. What is hikari-pool?
**Answer.** HikariCP is a high-performance JDBC (Java Database Connectivity) connection pool for Java applications, designed to efficiently manage and reuse database connections, improving application performance by reducing connection overhead.

#### 111. Trying to hit url getting blank page and now wanted to troubleshoot the error and need to verify port is listening or not and what you will do?
**Answer.** To troubleshoot a blank page when hitting a URL:

Use telnet your_server_ip your_port to check port availability.
Inspect server logs for errors.
Verify application and server configurations.
Check for recent changes that may have caused the issue.

#### 112. About utility and supervisor?
**Answer. Utility:**

Utilities are software tools designed to perform specific tasks or functions.
They are often command-line or GUI-based tools that aid in various operations.
Examples include grep for text searching, sed for text manipulation, and rsync for file synchronization.
Utilities simplify routine tasks, enhance productivity, and contribute to system administration and development processes.

**Supervisor:**

Supervisor is a process control system commonly used in Unix-like operating systems.
It monitors and manages processes to ensure they run continuously and reliably.
If a monitored process fails, Supervisor can restart it automatically.
Provides features like process grouping, logging, and configuration management.
Frequently used in server environments to maintain the stability and availability of critical services.

#### 113. Command to check wat all the server running using supervisor?
**Answer.** This command will display the status of all processes managed by Supervisor, showing their names, states, and other information. ``sudo supervisorctl status``

#### 114. About monit?
**Answer.** Monit is an open-source utility for monitoring and managing Unix systems. It monitors processes, files, directories, and system resources, and can perform automatic actions based on predefined conditions to ensure system stability.

#### 115. Differences between rpm and yum?
**Answer.** rpm is a low-level package manager for installing individual packages in Linux. yum is a higher-level package manager that simplifies package management by handling dependencies and providing an easier interface to install, update, and remove packages.

#### 116. What is GPG?
**Answer.** GPG stands for GNU Privacy Guard. It is a free and open-source software suite that provides cryptographic privacy and authentication for data communication. GPG is a complete implementation of the OpenPGP (Pretty Good Privacy) standard as defined by RFC4880.

#### 117. What is the significance of SIGKILL?
**Answer.** The SIGKILL signal in Linux is significant because it forcefully terminates a process. It is often used as a last resort when a process needs to be immediately and unconditionally stopped, without allowing it to perform any cleanup or graceful shutdown procedures. The SIGKILL signal cannot be ignored or handled by the process, making it a powerful tool for stopping misbehaving or unresponsive programs.

#### 118. How do you call the HTTP request method without a browser or curl?
**Answer.** You can use the telnet or netcat command to manually send an HTTP request without a browser or curl.

#### 119. What are the parameter available in the curl command?
**Answer.** The curl command has various parameters, some of the common ones include:

-X, --request: Specifies the HTTP request method.
-H, --header: Adds custom headers to the request.
-d, --data: Sends data in the request body.
-i, --include: Includes the HTTP headers in the output.
-o, --output: Writes output to a file.
-u, --user: Provides username and password for authentication.
-A, --user-agent: Sets the User-Agent header.
-v, --verbose: Enables verbose mode for detailed information.

#### 120. How to check boot logs in linux?
**Answer.** Use this command ``journalctl -b``

#### 121. What is Symbiosis Linux?
**Answer.** "Symbiosis Linux" is a specialized Linux distribution optimized for web hosting environments. It simplifies server management by providing tools for setting up domains, email accounts, databases, and security configurations.

#### 122. how to create zip file in linux?
**Answer.** To create a zip file in Linux, you can use the zip command. For example, to create a zip file named myfiles.zip containing file1.txt and directory1, you would run:
```
zip myfiles.zip file1.txt directory1
```

#### 123. what are the benefits of a multiprocessor system?
A multi-processor system refers to a computer system that contains more than one central processing unit (CPU) within a single physical machine. These multiple CPUs can work together to execute tasks simultaneously, thereby increasing the system's overall processing power and performance. In essence, it allows the system to perform multiple computations or tasks concurrently, improving efficiency and throughput compared to a single-processor system.
**Benefits:**
- Increased performance due to concurrent execution.
- Scalability by adding more processors.
- Higher throughput for handling multiple tasks simultaneously.
- Redundancy and fault tolerance capabilities.
- Efficient resource sharing and load balancing.
- Enhanced multitasking and parallel processing abilities.

#### 124. Explain about fork()?
**Answer.** fork() is a system call in Unix and Unix-like operating systems that creates a new process by duplicating the existing process. This results in two separate processes: the parent process and the child process. The child process is an exact copy of the parent process, except for a few differences such as their process IDs and return values from fork().

#### 125. What is a Scheduling Algorithm? Name different types of scheduling algorithms.
**Answer.** A scheduling algorithm determines the order in which tasks or processes are executed on a computing system.

Different types of scheduling algorithms include:

- First-Come, First-Served (FCFS): Processes are executed in the order they arrive.
- Shortest Job Next (SJN) or Shortest Job First (SJF): The next process to be executed is the one with the smallest execution time.
- Priority Scheduling: Processes are assigned priorities, and the one with the highest priority is executed first.
- Round Robin (RR): Each process gets a small unit of CPU time, and if it doesn't finish within that time, it's moved to the back of the queue.
- Multilevel Queue Scheduling: Processes are divided into different queues with different priorities, and each queue has its own scheduling algorithm.
- Multilevel Feedback Queue Scheduling: Similar to multilevel queue scheduling, but processes can move between queues based on their behavior.

#### 126. what is the difference between multitasking and multiprocessing OS?
**Answer.** Multitasking OS allows multiple tasks to run concurrently on a single CPU, while multiprocessing OS utilizes multiple CPUs to execute tasks simultaneously, enhancing overall system performance.

#### 127. What is the difference between paging and segmentation?
**Answer.** Paging and segmentation are memory management techniques used by operating systems:

Paging: Divides physical memory into fixed-size blocks called "pages" and logical memory into same-sized blocks called "frames." Processes are divided into pages, which are loaded into available frames in physical memory. Paging allows for efficient memory allocation but may lead to external fragmentation.

Segmentation: Divides the logical address space of a process into variable-sized segments. Each segment represents a logical unit of the program, such as code, data, or stack. Segmentation allows for more flexible memory allocation and sharing but may lead to fragmentation within segments.

#### 128. What is cache? What are its different types? Explain the entire process of searching in memory using hit and miss.
**Answer.** Cache is a high-speed memory subsystem that stores frequently accessed data or instructions to reduce the average time it takes to access them from the main memory. It serves as a buffer between the CPU and the slower main memory, speeding up data access by keeping copies of frequently accessed data closer to the processor.

Different types of cache include:

CPU Cache: Located on the CPU chip itself, CPU cache includes Level 1 (L1), Level 2 (L2), and Level 3 (L3) caches, with L1 being the smallest and fastest and L3 being the largest and slower.

Memory Cache: Also known as disk cache, memory cache stores frequently accessed data from the main memory in faster cache memory, such as RAM or SSDs.

The process of searching in memory using cache involves two scenarios: hit and miss.

Hit: When the processor requests data that is already present in the cache, it's called a cache hit. In this case, the data is retrieved directly from the cache, resulting in a fast access time.

Miss: If the requested data is not found in the cache, it's called a cache miss. The processor then needs to fetch the data from the slower main memory and load it into the cache for future access. This incurs a delay due to the longer access time of the main memory.

Overall, the goal of caching is to maximize the number of hits and minimize the number of misses, thereby improving the overall performance of the system.

#### 129. My device is heating up very quickly. Troubleshoot the scenario device. justify your answer.
**Answer.** To troubleshoot a device heating up quickly:

- Check for Dust and Debris: Ensure that the device's vents and fans are clear of dust and debris, as blocked airflow can cause overheating.

- Monitor CPU and GPU Usage: Use system monitoring tools to check if any processes are consuming excessive CPU or GPU resources, leading to overheating.

- Close Background Applications: Close any unnecessary background applications or processes that may be running and consuming system resources.

- Update Drivers and Firmware: Ensure that device drivers and firmware are up to date, as outdated drivers can sometimes cause hardware components to work inefficiently, leading to overheating.

- Check for Malware: Perform a malware scan to check for any malicious software that may be running in the background and causing excessive CPU usage.

- Optimize Power Settings: Adjust power settings to optimize performance and reduce power consumption, which can help prevent overheating.

- Inspect Cooling System: Check if the device's cooling system, including fans and heat sinks, is functioning properly. Replace any faulty components if necessary.

- Avoid Overclocking: If applicable, avoid overclocking the device's CPU or GPU, as this can lead to increased heat generation.

By following these troubleshooting steps, you can identify and address the underlying causes of the device overheating, thereby improving its performance and prolonging its lifespan.

#### 130. Explain framing.
**Answer.** Framing is a technique used in data link layer protocols to delineate and identify the boundaries of frames within a stream of data. It involves adding special bit sequences called "flags" or "start-stop" bits at the beginning and end of each frame. These flags help the receiver identify the start and end of each frame, allowing for reliable transmission and reception of data packets over a communication channel.

#### 131. What is a bootstrap program in OS?
**Answer.** A bootstrap program, often referred to as a bootloader, is a small program stored in non-volatile memory (such as ROM or EEPROM) that initializes the operating system (OS) during the system boot process. It is typically the first program to run when a computer is powered on, and its primary function is to load the operating system kernel into memory and transfer control to it, thereby starting the operating system.

#### 132. Explain demand paging?
**Answer.** Demand paging is a memory management technique used by operating systems to efficiently manage memory resources. Instead of loading an entire program into memory when it starts, demand paging loads only the necessary portions of a program into memory as they are needed. When a process references a memory page that is not currently in physical memory, a page fault occurs, triggering the operating system to fetch the required page from disk into memory. This approach helps conserve memory by loading only the most essential pages into memory, reducing the overall memory footprint of running processes and improving system performance.

#### 133. What do you mean by RTOS?
**Answer.** RTOS stands for Real-Time Operating System. It is an operating system designed to manage real-time tasks with strict timing constraints. RTOS ensures that tasks are completed within specific time limits, making it suitable for applications where timing predictability and responsiveness are critical, such as industrial automation, aerospace systems, and embedded devices.

#### 134. Explain zombie process?
**Answer.** A zombie process is a terminated process that has completed its execution but still has an entry in the process table. It retains some process information, such as its process ID and exit status, but it no longer has an active execution context. Zombie processes typically occur when a parent process fails to call the wait() system call to retrieve the exit status of its terminated child process. These zombie processes consume system resources until their parent process acknowledges their termination by calling wait(), at which point they are removed from the process table.

#### 135. What is thrashing in OS?
**Answer.** Thrashing in operating systems refers to a state of excessive paging activity, where the system is spending more time swapping data between main memory and disk than executing useful work. It occurs when the system is overwhelmed by the demand for memory, causing a constant state of page faults and disk I/O operations, leading to a significant decrease in overall system performance.

#### 136. I am trying media over FTP from one device to another. The rate of transfer is very slow. Troubleshoot the scenario.
**Answer.** To troubleshoot slow media transfer over FTP:

- Check Network Connection: Ensure both devices are connected to a stable and fast network, preferably using wired connections for optimal speed.
- Verify FTP Server Configuration: Confirm that the FTP server's configuration allows for sufficient bandwidth allocation and concurrent connections.
- Check Device Resources: Verify that both the sender and receiver devices have adequate processing power, memory, and disk space to handle the transfer efficiently.
- Consider Network Congestion: Check for network congestion or bandwidth limitations, especially if multiple devices are sharing the same network.
- Review FTP Client Settings: Adjust FTP client settings to use passive mode, which can sometimes improve transfer speeds, especially in firewall-restricted environments.
- Optimize File Compression: If feasible, compress the media files before transferring them to reduce their size and speed up the transfer process.
- Monitor Transfer Speed: Use network monitoring tools to measure the actual transfer speed and identify any bottlenecks or limitations in the network or devices.
- Update Software and Drivers: Ensure that both the FTP client and server software, as well as network drivers, are up to date to benefit from performance optimizations and bug fixes.

By following these troubleshooting steps, you can identify and address the underlying issues causing slow media transfer over FTP, thereby improving the transfer speed and efficiency.

#### 137. Memory management, Memory pages, Basic commands?
**Answer.** Memory management involves organizing and controlling computer memory, ensuring efficient use of available resources.

Memory pages are fixed-size blocks used in virtual memory systems for memory allocation and management.

Basic commands for memory management include malloc (allocate memory), free (release memory), memset (set memory values), and memcpy (copy memory content).

#### 138. Troubleshooting: I am not able to connect to the internet.
**Answer.** To troubleshoot internet connectivity issues:

- Check Network Connection: Ensure cables are properly connected, and Wi-Fi is enabled if applicable.
- Restart Network Devices: Power cycle the modem and router to refresh connections.
- Check IP Configuration: Use commands like ipconfig (Windows) or ifconfig (Linux) to verify IP settings.
- Ping Network Resources: Test connectivity to websites or local devices using the ping command.
- Check DNS Settings: Verify DNS settings and try alternative DNS servers like Google DNS (8.8.8.8).
- Firewall and Security: Temporarily disable firewall or security software to check for blocking.
- Update Network Drivers: Ensure network drivers are up to date.
- ISP Status: Check if the internet service provider is experiencing outages.

#### 139. Scenario: You have 4 GB RAM Mobile, What do you think can we able to play 8GB Game.
**Answer.** No, it's unlikely. Mobile games typically require RAM similar to or slightly higher than their file size. Attempting to run an 8GB game on a device with only 4GB of RAM would likely result in performance issues or failure to run altogether due to insufficient memory. But, Virtual Memory: Your operating system uses virtual memory to compensate for limited RAM by temporarily storing data on disk. This allows you to run a 8GB game on a 4GB RAM system, but it may slow down performance due to frequent swapping between RAM and disk.

#### 140. What is starvation and aging in OS?
**Answer.** Starvation: Starvation occurs when a process is unable to proceed because it cannot access required resources, despite being eligible to do so. This situation can arise due to resource contention or scheduling algorithms favoring other processes excessively.

Aging: Aging is a technique used to prevent starvation in scheduling algorithms. It involves gradually increasing the priority of waiting processes over time, ensuring that all processes eventually get a chance to execute, even if they have been waiting for a long time.

#### 141. BSOD
**Answer.** BSOD (Blue Screen of Death) is a critical system error in Windows that causes the computer to display a blue screen with an error message. It indicates severe issues like hardware failures, driver conflicts, or system errors, requiring troubleshooting to resolve.

#### 142. What to do if laptop is hanging a lot?
**Answer.** If a laptop is hanging frequently, you can try the following steps:

- Check for Resource Usage: Use task manager or activity monitor to identify any processes consuming excessive CPU, memory, or disk resources.
- Close Unnecessary Programs: Close any unnecessary programs and browser tabs to free up system resources.
- Restart: Restart the laptop to clear memory and refresh system processes.
- Update Drivers and Software: Ensure that device drivers and software are up to date to address any compatibility issues or bugs.
- Check for Malware: Perform a malware scan to check for any malicious software that may be causing system slowdowns.
- Increase RAM: If possible, consider upgrading the RAM to improve system performance, especially if the laptop frequently runs out of memory.
- Disk Cleanup: Perform disk cleanup to remove temporary files, cache, and other unnecessary data that may be clogging up the system.
- Check Hardware: If the issue persists, it may indicate a hardware problem such as a failing hard drive or overheating. In such cases, consider seeking professional assistance.

#### 143. How to fix a slow computer?  
**Answer.** To fix a slow computer, you can try the following steps:

- Check for Malware: Run a malware scan to detect and remove any malicious software.
- Update Software: Ensure that the operating system and all installed software are up to date.
- Restart: Restart the computer to clear memory and refresh system processes.
- Check Resource Usage: Use task manager (Windows) or activity monitor (Mac) to identify processes consuming excessive CPU, memory, or disk resources.
- Disk Cleanup: Remove temporary files, cache, and unnecessary data to free up disk space.
- Disable Startup Programs: Disable unnecessary programs from starting automatically at boot to improve startup time.
- Upgrade Hardware: Consider upgrading hardware components like RAM or replacing a traditional hard drive with a solid-state drive (SSD) for improved performance.
- Optimize Settings: Adjust system settings for better performance, such as disabling visual effects or adjusting power settings.
- Defragment Hard Drive: If using a traditional hard drive, consider defragmenting it to optimize file access.
- Seek Professional Help: If the issue persists, consider seeking assistance from a professional technician or computer repair service.

#### 144. What is RAM ? What is a thread ? What is a Pthread ?
**Answer. RAM (Random Access Memory):** RAM is a type of computer memory that stores data and program instructions that the CPU needs to access quickly. It is volatile memory, meaning that its contents are lost when the computer is powered off.

**Thread:** A thread is the smallest unit of execution within a process. Threads share the same memory space and resources of the process they belong to but can execute independently, allowing for parallel execution of tasks within a program.

**Pthread:** Pthreads (POSIX threads) are a standardized thread API for Unix-like operating systems. They provide a set of functions for creating, managing, and synchronizing threads within a program, allowing developers to write portable multithreaded applications

#### 145. Can CPU goes beyond 100%?
**Answer.** No, the CPU cannot go beyond 100%. CPU usage percentages represent the proportion of time the CPU spends executing processes relative to its maximum capacity. Therefore, 100% CPU usage indicates that the CPU is fully utilized, and there are no additional processing resources available.

#### 146. How to install and use a software which need more space than the available space in your system ?
**Answer.** To install and use software that requires more space than available on your system, you can:

Free up disk space by removing unnecessary files or applications.
Use external storage devices such as USB drives or external hard drives to store additional data or install the software.
Consider upgrading your system's storage capacity by installing a larger hard drive or using cloud storage solutions.
But, alternative solutions such as using external storage devices or upgrading your system's storage capacity to accommodate the software.

#### 147. Difference between buffer and cache.
**Answer.** Buffer: A buffer temporarily stores data during input/output operations, typically to smooth out discrepancies in data transfer rates between devices.
Cache: A cache stores frequently accessed data or instructions to improve performance by reducing access latency. It holds copies of data from slower storage mediums, such as hard drives, in faster storage mediums, such as RAM or SSDs.

#### 148. Explain deadlock? How can we prevent it? Explain semaphores in layman language?
**Answer.** Deadlock: Deadlock is a situation in which two or more processes are unable to proceed because each is waiting for the other to release a resource, resulting in a standstill. It can be prevented by using techniques such as resource ordering, deadlock detection, and avoidance algorithms.

Semaphores: Semaphores are synchronization mechanisms used to control access to shared resources in a multi-threaded or multi-process environment. They act like counters and can be used to manage access to resources by allowing only a certain number of threads or processes to access them simultaneously.

#### 149. Explain different page replacement algorithm, and which is the most efficient?
**Answer.** Page replacement algorithms manage memory in operating systems by selecting which page to evict from memory when a new page needs to be loaded. Some common algorithms include:

FIFO (First-In-First-Out)
LRU (Least Recently Used)
LFU (Least Frequently Used)
Optimal
The most efficient page replacement algorithm depends on the system's workload and characteristics. However, the Optimal algorithm, which selects the page that will not be used for the longest time in the future, is theoretically the most efficient but often impractical due to its requirement of future knowledge. LRU is widely used in practice and often performs well in a variety of scenarios.

#### 150. Can round-robin be pre-emptive?
**Answer.** Yes, Round-Robin scheduling can be pre-emptive. In a pre-emptive Round-Robin scheduling algorithm, the CPU time allocated to a process is divided into time slices, and if a process does not complete within its time slice, it is pre-empted (interrupted) and moved to the end of the ready queue to allow other processes to execute. This ensures fairness in CPU allocation and prevents any single process from monopolizing the CPU for an extended period.

#### 151. What is Active directory?
**Answer.** In Linux, a directory refers to a file system directory structure, which organizes files and directories hierarchically. It is not equivalent to Active Directory, which is a centralized directory service primarily used in Windows environments for managing network resources. In Linux, directory services may be provided by solutions such as LDAP (Lightweight Directory Access Protocol) or OpenLDAP.

#### 152. What is Bash? How would you explain Bash/PowerShell to a non-technical person?
**Answer.** Bash (Bourne Again Shell) is a command-line shell and scripting language used in Unix-like operating systems, including Linux. It provides a text-based interface for interacting with the operating system, executing commands, and writing scripts to automate tasks.

To explain Bash/PowerShell to a non-technical person:

"Bash/PowerShell is like a digital assistant for your computer. It's a tool that lets you communicate with your computer using text commands instead of clicking buttons or icons. You can tell it to perform tasks like opening files, copying folders, or even writing programs, just by typing commands into a special window called a 'terminal' or 'command prompt'."

#### 153. 
**Answer.** 

#### 154. where are the USB drivers installed in Linux.
**Answer.** USB drivers in Linux are typically part of the kernel and are located in the 
```
/lib/modules/<kernel_version>/kernel/drivers/usb directory.
```

#### 155. Managing system services and background processes.
**Answer.** Managing system services and background processes involves starting, stopping, and monitoring tasks that run in the background of an operating system. This includes using commands like systemctl or service to control services, monitoring resource usage, and configuring automatic startup settings.

#### 156. How to view logs in windows?
**Answer.** To view logs in Windows, you can use the Event Viewer tool. You can access Event Viewer by typing "Event Viewer" into the Windows search bar and selecting the application from the results.
Another in-built option to view logs in Windows is the "Event Viewer" application, accessible through the Control Panel. You can navigate to "Control Panel" > "System and Security" > "Administrative Tools" > "Event Viewer" to access it.

#### 157. Which directory are log files stored?
**Answer.** In Linux, log files are typically stored in the /var/log directory.

#### 158. A user says that whenever they try to use the system, it keeps rebooting, what could be the cause of this? How would you go about trying to find out what's causing the issue?
**Answer.** The cause of the system continuously rebooting could be due to various reasons such as hardware issues, software conflicts, or system errors. To diagnose the problem, you can start by checking the system logs for any error messages or clues about the rebooting behavior. Additionally, examining recent changes to hardware or software configurations and running diagnostic tests on hardware components can help identify the root cause of the issue.

#### 159. A client's system/server is having bad performance, what could potentially be causing this? How would you go about trying to find out the cause of this problem?
**Answer.** Poor system/server performance could be caused by factors such as insufficient hardware resources, software issues, network congestion, or improper configuration. To diagnose the problem, you can start by checking system resource usage (CPU, memory, disk, network) and reviewing system logs for error messages or performance-related issues. Additionally, monitoring network traffic and conducting performance tests can help identify bottlenecks and determine the root cause of the problem.

#### 160. If I have to run a management script in my system at a particular time each day, how will I proceed? What exactly goes inside cron jobs scripts?
**Answer.** To run a management script at a particular time each day, you can use cron, a built-in scheduler in Unix-like operating systems. You'll create a cron job by editing the crontab file using the crontab -e command and specifying the script to run and the desired schedule (e.g., daily at a specific time).

Cron jobs scripts typically contain commands or scripts to be executed at scheduled intervals. They can include shell commands, paths to scripts or programs, and any necessary parameters or options.

#### 161. when you use ping does it only check network connectivity or does it check connectivity on a specific port?
**Answer.** When you use the ping command, it only checks network connectivity at the IP layer using ICMP echo requests and replies. It does not check connectivity on a specific port. If you want to check connectivity on a specific port, you would use other tools such as telnet, nc, or curl.

#### 162. What if you want to check connectivity on a certain website on a specific port, for example. You do Ping google.com You get a response right? It means that you can communicate with Google as in your laptop from where you ran that command is communicating with google.com Just fine. However, if you want to communicate with Google, let's say on port 8080. How would you check connectivity for that?

#### or

#### Let's say you create a website. Just for example, right? It's your own website, where you know you put in details about your life and stuff. And it's hosted on, let's say www yourname.com. Write your name means that can.com That's fine. So when you pick that you get a response. We have been in this from your own laptop or computer whatever you use, right? It means okay connectivity is there however you want to communicate to your website on a specific port. For example, let the port number be 8080 How would you check connectivity with your website on port 8080 Like what one would use?
**Answer.** To check connectivity to a specific website on a specific port, such as port 8080 for Google, you can use tools like telnet, nc (netcat), or curl. For example: ```telnet google.com 8080``` or ```telnet yourname.com 8080```

This command attempts to establish a connection to Google on port 8080. If successful, it indicates that there is connectivity to Google on that port.

