## git

git config --global http.sslVerify false  
git config credential.helper cache  
git config credential.helper 'cache --timeout=54000'  
git config --global credential.helper 'store'  
echo "https://username:password@git.derbysoft.tm">$HOME/..git-credentials  



## 查看进程的线程数
#top的每一行显示一个线程。  
top -H  

#查看所有存在的线程，grep进一步过滤。  
ps -xH  

#指定的进程产生的线程数目。  
ps -mq PID  
       
       

## CentOS version
cat /etc/redhat-release  
uname -a  
lsb_release  

## firewall
firewall-cmd --get-active-zones
sudo firewall-cmd --permanent --zone=public --add-port=9092/tcp
sudo firewall-cmd --reload

sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
sudo service iptables save

## change user
su username
sudo su -s /bin/bash jenkins
sudo -u jenkins bash

## user group
cat /etc/group  
#创建组  
groupadd  test  
#将test组的名子改成test2  
groupmod -n test2  test  
#删除组  
groupdel test2  
#查看当前登录用户所在的组  
groups  
#查看apacheuser所在组  
groups apacheuser  
