#!/bin/bash
# Linux Privilege Escalation Script
# Save this script as "linux_priv_esc.sh" and execute with "bash linux_priv_esc.sh"

# Enumeration
echo "### Enumeration ###"

# Operating System
echo "## Operating System ##" >> OperatingSys.txt
cat /etc/issue >> OperatingSys.txt
cat /etc/*-release >> OperatingSys.txt
cat /etc/lsb-release >> OperatingSys.txt
cat /etc/redhat-release >> OperatingSys.txt

# Kernel version
echo "## Kernel Version ##" >> KernalData.txt
cat /proc/version >> KernalData.txt
uname -a >> KernalData.txt
uname -mrs >> KernalData.txt
rpm -q kernel >> KernalData.txt
dmesg | grep Linux >> KernalData.txt
ls /boot | grep vmlinuz- >> KernalData.txt

# Environmental Variables
echo "## Environmental Variables ##" >> EnvVar.txt
cat /etc/profile >> EnvVar.txt
cat /etc/bashrc >> EnvVar.txt
cat ~/.bash_profile >> EnvVar.txt
cat ~/.bashrc >> EnvVar.txt
cat ~/.bash_logout >> EnvVar.txt
env
set

# Printer
echo "## Printer ##" >> printer.txt
lpstat -a >> printer.txt

# Applications & Services
echo "### Applications & Services ###"

# Services running and their user privileges
echo "## Services and User Privileges ##" >> runningserv.txt
ps aux >> runningserv.tx
ps -ef >> runningserv.tx
top >> runningserv.tx
cat /etc/service >> runningserv.tx

# Services running as root
echo "## Services Running as Root ##" >> rootserv.txt
ps aux | grep root >> rootserv.txt
ps -ef | grep root >> rootserv.txt

# Installed applications and their versions
echo "## Installed Applications and Versions ##" >> instapps.txt
ls -alh /usr/bin/ >> instapps.txt
ls -alh /sbin/ >> instapps.txt
dpkg -l >> instapps.txt
rpm -qa >> instapps.txt
ls -alh /var/cache/apt/archives >> instapps.txt
ls -alh /var/cache/yum/ >> instapps.txt

# Misconfigured services and vulnerable plugins
echo "## Misconfigured Services and Vulnerable Plugins ##" >> misconfigs.txt
cat /etc/syslog.conf >> misconfigs.txt
cat /etc/chttp.conf >> misconfigs.txt
cat /etc/lighttpd.conf >> misconfigs.txt
cat /etc/cups/cupsd.conf >> misconfigs.txt
cat /etc/inetd.conf >> misconfigs.txt
cat /etc/apache2/apache2.conf >> misconfigs.txt
cat /etc/my.conf >> misconfigs.txt
cat /etc/httpd/conf/httpd.conf >> misconfigs.txt
cat /opt/lampp/etc/httpd.conf >> misconfigs.txt
ls -aRl /etc/ | awk '$1 ~ /^.*r.*/' >> misconfigs.txt

# Scheduled jobs
echo "## Scheduled Jobs ##" >> schedjob.txt
crontab -l >> schedjob.txt
ls -alh /var/spool/cron >> schedjob.txt
ls -al /etc/ | grep cron >> schedjob.txt
ls -al /etc/cron* >> schedjob.txt
cat /etc/cron* >> schedjob.txt
cat /etc/at.allow >> schedjob.txt
cat /etc/at.deny >> schedjob.txt
cat /etc/cron.allow >> schedjob.txt
cat /etc/cron.deny >> schedjob.txt
cat /etc/crontab >> schedjob.txt
cat /etc/anacrontab >> schedjob.txt
cat /var/spool/cron/crontabs/root >> schedjob.txt

# Plain text usernames and passwords
echo "## Plain Text Usernames and Passwords ##" >> unampwds.txt
grep -i user [filename] >> unampwds.txt
grep -i pass [filename] >> unampwds.txt
grep -C 5 "password" [filename] >> unampwds.txt
find . -name "*.php" -print0 | xargs -0 grep -i -n "var $password" >> unampwds.txt

# Communications & Networking
echo "### Communications & Networking ###" >> commnet.txt


# NICs and connections
echo "## NICs and Connections ##" >> commnet.txt
/sbin/ifconfig -a >> commnet.txt
cat /etc/network/interfaces >> commnet.txt
cat /etc/sysconfig/network >> commnet.txt

# Network configuration settings
echo "## Network Configuration Settings ##" >> netconfig.txt
cat /etc/resolv.conf >> netconfig.txt
cat /etc/sysconfig/network >> netconfig.txt
cat /etc/networks >> netconfig.txt
iptables -L >> netconfig.txt
hostname >> netconfig.txt 
dnsdomainname >> netconfig.txt

# Other users and hosts communicating with the system
echo "## Users and Hosts Communicating with the System ##" >> netconfig.txt
lsof -i >> netconfig.txt
lsof >> netconfig.txt
