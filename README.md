# LinuxForDevops
Everything related to devops


top 100 linux commands -

ls — List directory contents
cd — Change directory
pwd — Print working directory
mkdir — Make directory
rm — Remove file or directory
cp — Copy file or directory
mv — Move or rename file or directory
touch — Create a new file
nano — Text editor
cat — Print the contents of a file
less — View file contents one page at a time
grep — Search for text in a file
find — Search for files and directories
ps — Display information about running processes
kill — Terminate a process
top — Display system resource usage
ifconfig — Configure network interfaces
ping — Test network connectivity
ssh — Secure shell, remotely access a server
scp — Secure copy, transfer files securely
rsync — Efficient file transfer and synchronization
tar — Archive files and directories
gzip — Compress files
gunzip — Uncompress files
df — Display disk space usage
du — Estimate file space usage
chmod — Change file permissions
chown — Change file ownership
su — Switch user or become superuser
sudo — Execute command as superuser
curl — Transfer data from or to a server
wget — Download files from the web
diff — Compare two files
uptime — Display system uptime
date — Display or set the system date and time
whoami — Print the current user
which — Show the location of a command
tar — Archive files and directories
gzip — Compress files
gunzip — Uncompress files
df — Display disk space usage
du — Estimate file space usage
lsblk — List block devices
mount — Mount file systems
umount — Unmount file systems
netstat — Display network connections
iptables — Firewall configuration
nmap — Network exploration and security auditing
ssh-keygen — Generate SSH keys
ssh-copy-id — Copy SSH keys to remote servers
htop — Interactive process viewer
wget — Download files from the web
ping — Test network connectivity
traceroute — Trace network path
curl — Transfer data from or to a server
dig — DNS lookup
service — Manage system services
systemctl — Manage system services
journalctl — View system logs
chroot — Change root directory for a process
crontab — Schedule tasks to run at specific times
at — Schedule tasks to run once at a specific time
awk — Process text files
sed — Stream editor
cut — Extract columns from text files
tee — Redirect output to multiple files
xargs — Build and execute command lines from standard input
tar — Archive files and directories
rsync — Efficient file transfer and synchronization
diff — Compare two files
tail — Display the last lines of a file
head — Display the first lines of a file
wc — Count lines, words, and characters in
sort — Sort lines of text files
uniq — Remove duplicate lines from text files
awk — Process text files
sed — Stream editor
cut — Extract columns from text files
tee — Redirect output to multiple files
xargs — Build and execute command lines from standard input
lsof — List open files and processes
scp — Secure copy, transfer files securely
hostname — Print or set system hostname
dig — DNS lookup
nslookup — DNS lookup
traceroute — Trace network path
mtr — Network diagnostic tool
curl — Transfer data from or to a server
openssl — SSL/TLS security protocol
sshfs — Mount remote file systems over SSH
netcat — Networking utility
tcpdump — Packet analyzer
telnet — Telnet client
nc — Netcat client
iptables — Firewall configuration
nmap — Network exploration and security auditing
zip — Compress files
unzip — Uncompress files
crontab — Schedule tasks to run at specific times
at — Schedule tasks to run once at a specific time.


Advanced Linux commands that are useful for DevOps engineers

1. rsync: A powerful command for synchronizing files and directories between different locations. It can be used for backup purposes, deploying files to remote servers, or syncing data between local and remote systems.
Example:

rsync -avz source_directory/ 
user@remote_host:destination_directory/

2. find: This allows you to search for files and directories based on various criteria such as name, size, modification time, and permissions. It is particularly handy for locating specific files within a large directory structure.

Example:
find /path/to/search -name "*.txt" -size +1M

3. grep: A versatile command-line tool for searching text patterns within files. It supports regular expressions and can be used to filter log files, search for specific content, or analyze output from other commands.

Example:
grep "error" logfile.txt

4. sed: Stream Editor is a powerful command-line utility for text manipulation. It can perform tasks like searching and replacing, inserting or deleting lines, and transforming text based on patterns.

Example:
sed 's/foo/bar/g' input.txt

5. awk: A scripting language designed for text processing and data extraction. It provides powerful pattern-matching and data manipulation capabilities, making it useful for processing structured data and generating reports.

Example:
awk '{print $1}' data.txt

6. lsof: Short for “list open files,” this command displays information about files opened by processes on a system. It is helpful for troubleshooting issues related to file locks, identifying network connections, and analyzing resource usage.

Example:
lsof -i :8080

7. tcpdump: A network packet analyzer command-line tool that captures and displays network traffic. It allows you to monitor and inspect network communication, making it useful for diagnosing network issues and analyzing protocols.

Example:
tcpdump -i eth0 tcp port 80

8. strace: Used for debugging and troubleshooting, strace traces system calls and signals made by a process. It can help identify issues related to file access, system resource usage, and process behavior.

Example:
strace -p <PID>

9. sar: The System Activity Reporter (sar) command collects, reports, and analyzes system activity data such as CPU usage, memory usage, disk I/O, and network statistics. It is useful for monitoring system performance and identifying bottlenecks.

Example:
sar -u 1 5

10. tmux: A terminal multiplexer that allows you to create and manage multiple terminal sessions within a single window. It enables you to detach and reattach sessions, run commands in the background, and maintain persistent sessions.

Example:
tmux new -s mysession


The Linux/Unix file system hierarchy base begins at the root and everything starts with the root directory. 

These are the common top-level directories associated with the root directory:

Directories	Description

 /bin	 binary or executable programs.
/etc	system configuration files.
/home	home directory. It is the default current directory.
/opt	optional or third-party software.
/tmp	temporary space, typically cleared on reboot.
/usr	 User related programs.
/var 	log files.

Some other directories in the Linux system:

Directories 	Description

/boot	
It contains all the boot-related information files and folders such as conf, grub, etc.

/dev	
It is the location of the device files such as dev/sda1, dev/sda2, etc.

/lib	
It contains kernel modules and a shared library.

/lost+found	
It is used to find recovered bits of corrupted files.

/media	
It contains subdirectories where removal media devices are inserted.

/mnt	
It contains temporary mount directories for mounting the file system.

/proc	
It is a virtual and pseudo-file system to contains info about the running processes with a specific process ID or PID.

/run	
It stores volatile runtime data.

/sbin	
binary executable programs for an administrator.

/srv 	
It contains server-specific and server-related files.

/sys	
It is a virtual file system for modern Linux distributions to store and allows modification of the devices connected to the system.

Exploring directories and their usability:

We know that Linux is a very complex system that requires an efficient way to start, stop, maintain and reboot a system, unlike Windows operating system. In the Linux system some well-defined configuration files, binaries, main pages information files are available for every process. 

Linux Kernel File:
/boot/vmlinux – The Linux kernel file.

Device Files:
/dev/hda – Device file for the first IDE HDD.
/dev/hdc – A pseudo-device that output garbage output is redirected to /dev/null.

System Configuration Files:
/etc/bashrc	It is used by bash shell that contains system defaults and aliases.
/etc/crontab	A shell script to run specified commands on a predefined time interval.
/etc/exports	 It contains information on the file system available on the network.
/etc/fstab	Information of the Disk Drive and their mount point.
/etc/group	 It is a text file to define Information of Security Group.
/etc/grub.conf	It is the grub bootloader configuration file.
/etc/init.d	 Service startup Script.
/etc/lilo.conf 	 It contains lilo bootloader configuration file.
/etc/hosts	Information of IP and corresponding hostnames
/etc/hosts.allow	It contains a list of hosts allowed accessing services on the local machine.
/etc/host.deny	 List of hosts denied accessing services on the local machine.
/etc/inittab	 INIT process and their interaction at the various run levels.
/etc/issue	Allows editing the pre-login message.
/etc/modules.conf	It contains the configuration files for the system modules.
/etc/motd	 It contains the message of the day.
/etc/mtab 	Currently mounted blocks information.
/etc/passwd 	 It contains username, password of the system, users in a shadow file.
/etc/printcap 	 It contains printer Information.
/etc/profile	 Bash shell defaults.
/etc/profile.d	It contains other scripts like application scripts, executed after login.
/etc/rc.d	 It avoids script duplication.
/etc/rc.d/init.d	 Run Level Initialisation Script.
/etc/resolv.conf	DNS being used by System.
/etc/security	 It contains the name of terminals where root login is possible.
/etc/skel	Script that initiates new user home directory.
/etc/termcap	An ASCII file that defines the behavior of different types of the terminal.
/etc/X11	Directory tree contains all the conf files for the X-window System.

User Related Files:

/usr/bin	 It contains most of the executable files.
/usr/bin/X11 	Symbolic link of /usr/bin.
/usr/include	 It contains standard files used by C program.
/usr/share	It contains architecture independent shareable text files.
/usr/lib	 It contains object files and libraries.
/usr/sbin	It contains commands for Super User, for System Administration.

Virtual and Pseudo Process Related Files:

/proc/cpuinfo	CPU Information
/proc/filesystems	It keeps useful info about the processes that are currently running.
/proc/interrupts	 it keeps the information about the number of interrupts per IRQ.
/proc/ioports	Contains all the Input and Output addresses used by devices on the server
/proc/meminfo	It reports the memory usage information.
/proc/modules	Currently using kernel module.
/proc/mount	Mounted File-system Information.
/proc/stat	It displays the detailed statistics of the current system.
/proc/swaps	 It contains swap file information.

Version Information File:
/version – It displays the Linux version information.

Log Files:

/var/log/lastlog	 It stores user’s last login info.
/var/log/messages	 It has all the global system messages
/var/log/wtmp	It keeps a history of login and logout information.

To check the Linux directories, open the terminal and execute sudo -s followed by system password to give root privilege. Then after changing the current home directory to the root directory and check the list of all available directories in the base directory as shown below. 
