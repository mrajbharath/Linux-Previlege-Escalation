# Linux-Previlege-Escalation
Before starting, I would like to point out - I'm no expert. As far as I know, there isn't a "magic" answer, in this huge area. This is simply my finding, typed up, to be shared (my starting point). Below is a mixture of commands to do the same thing, to look at things in a different place or just a different light. I know there more "things" to look for. It's just a basic & rough guide. Not every command will work for each system as Linux varies so much. "It" will not jump off the screen - you've to hunt for that "little thing" as "the devil is in the detail"
Enumeration is the key.
(Linux) privilege escalation is all about:
Collect - Enumeration, more enumeration and some more enumeration.
Process - Sort through data, analyse and prioritisation.
Search - Know what to search for and where to find the exploit code.
Adapt - Customize the exploit, so it fits. Not every exploit work for every system "out of the box".
Try - Get ready for (lots of) trial and error.
What's the distribution type? What version?
cat /etc/issue
cat /etc/*-release
cat /etc/lsb-release      # Debian based
cat /etc/redhat-release   # Redhat based
What's the kernel version? Is it 64-bit?
cat /proc/version
uname -a
uname -mrs
rpm -q kernel
dmesg | grep Linux
ls /boot | grep vmlinuz
What can be learnt from the environmental variables?
cat /etc/profile
cat /etc/bashrc
cat ~/.bash_profile
cat ~/.bashrc
cat ~/.bash_logout
env
set
Is there a printer?
lpstat -a
Applications & Services

What services are running? Which service has which user privilege?

ps aux
ps -ef
top
cat /etc/services

Which service(s) are been running by root? Of these services, which are vulnerable - it's worth a double check!

ps aux | grep root
ps -ef | grep root

What applications are installed? What version are they? Are they currently running?

ls -alh /usr/bin/
ls -alh /sbin/
dpkg -l
rpm -qa
ls -alh /var/cache/apt/archivesO
ls -alh /var/cache/yum/





