# 高解像度視覚刺激システム
## 準備
### Node.js
- インストール方法
sudo apt-get install nodejs
sudo apt-get install npm

### GL-Console(https://github.com/KazukiHiraizumi/GL-Console)
- インストール方法
git clone https://github.com/KazukiHiraizumi/GL-Console
cd GL-Console
make kio
sudo make install

### Httpd "Lighttpd"
- インストール方法
sudo apt-get install lighttpd
- "/etc/lighttpd/lighttpd.conf"に以下を加える
server.modules += (
   "mod_cgi"
)
cgi.assign = ( ".sh"  => "/bin/bash" )
- Set Home path an
ln -fs /home/<your accont>/HRS /var/www/html

- 自動起動
sudo systemctl start lighttpd.service


## セットアップ
- Add "start.sh" as a Session Manager Startup Application
    or just type ./start.sh
- Display Language
  cd HRS
  ./jp.sh  //Japanese
  ./en.sh  //English

## Operation
- Connect to it via WebBrowser. The start URL is "home.html"
