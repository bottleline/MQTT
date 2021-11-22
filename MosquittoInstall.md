## 1. MQTT 설치 (CentOS7)

sudo yum install mosquitto  
sudo yum install mosquitto-client  
  
sudo iptables -I INPUT -m tcp -p tcp --dport 1883 -j ACCEPT // 포트개방  
  
sudo service iptables save  
systemctl enable iptables  
systemctl restart iptables //iptable 재실행  


## 2. MQTTConfig 설정

mqttconf  
  
listener 8883  
allow_anonymous false  
password_file /etc/mosquitto/passwd  


## 3. Mysql 설치

yum -y install mariadb-server maridb-client  
systemctl enable mariadb // 시스템실행시 자동실행  
systemctl start maridb //서비스실행   
--------------------------------------------------------------------------  
mysql -u root -p //  로그인
