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

#all threads  
ps -xH  

#threads on process  
ps -mq PID  
       
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


