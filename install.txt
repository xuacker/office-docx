程序默认安装环境。ubuntu 16.04.4　　　理论支持常见的所有linux系统。
本工具完全开源，欢迎大家检测

全新安装的ubuntu16.04.4安装本工具的步骤大概如下。
以下操作需要在root权限执行。

1,拷贝当前目录到/root下
拷贝之后的目录结构如下：


root@ubuntu:~/office# pwd
/root/office
root@ubuntu:~/office# ls
GeoLite2-City.mmdb  docx_ip.py  files_log.db  ip.conf  orig  output  sessions  static  temp  views
root@ubuntu:~/office# 


２，安装程序依赖的系统组件。

apt-get update
apt-get install supervisor
apt-ge install python-pip
apt-get install p7zip-full p7zip p7zip-rar zip
pip install bottle
pip install python-docx
pip install ipcalc
pip install geoip2
pip install six
pip install beaker
pip install jinja2


3,设置程序开机自启动。
cat /root/office/supervisord.conf > /etc/supervisor/supervisord.conf