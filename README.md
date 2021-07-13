## git

git config --global http.sslVerify false  
git config credential.helper cache  
git config credential.helper 'cache --timeout=54000'  
git config --global credential.helper 'store'  
echo "https://username:password@git.derbysoft.tm">$HOME/..git-credentials  

git branch -lvv  
git branch -rvv  
git branch -avv  

## view process or thread
#thread per line  
top -H  
top -Hp PID

#all threads  
ps -xH  

#threads on process  
ps -mq PID  

#perf look call stack  
perf record -g -p 55

#report memory map of a process  
pmap -x 75  

## network
#net stats  
netstat -s

#socket stats tcp listen  
ss -nlt

#socket tcp v6 stats exclude ESTAB   
sudo ss -t6 state all | grep -v ESTAB

#socket tcp time-wait state  
ss -tan state time-wait | wc -l

## CentOS version
cat /etc/redhat-release  
uname -a  
lsb_release  

## Firewall
firewall-cmd --get-active-zones  
sudo firewall-cmd --permanent --zone=public --add-port=9092/tcp  
sudo firewall-cmd --reload  

sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT  
sudo service iptables save  

## Change user
su username  
sudo su -s /bin/bash jenkins  
sudo -u jenkins bash  

## User group
#view group  
cat /etc/group  
#create  
groupadd  test  
#change group name  
groupmod -n new_name  old_name  
#delete group  
groupdel test2  
#view current user's group  
groups  
#view user_name's group  
groups user_name  

## Change owner or group
chown -R -v user:group testfile  

## check folder size  
du -ah -d 1 path  
#check folder size with summery  
du -sh path  

## SELinux  
#disable SELinux  
sudo setenforce 0  

#Permanently disable SELinux  
#Edit /etc/selinux/config  
SELINUX=disabled  

## Run in background
nohup ping www.ibm.com >filename 2>&1 &  
setsid ping www.ibm.com

