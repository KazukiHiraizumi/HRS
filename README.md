# HRS
4K Resolution Optical Stimulator

## Needed
### Node.js
- Install

### GL-Console(https://github.com/KazukiHiraizumi/GL-Console)
- Install

### Httpd "Lighttpd"
- Install
 sudo apt-get install lighttpd
- Configuration
 - Add below in "/etc/lighttpd/lighttpd.conf"
  server.modules += (
	 "mod_cgi"
  )
  cgi.assign = ( ".sh"  => "/bin/bash" )
 - Set Home path an
  ln -fs /home/<your accont>/HRS /var/www/html

- Auto start
 sudo systemctl start lighttpd.service


##Setup
- Add "start.sh" as a Session Manager Startup Application
    or just press ./start.sh
- Display Language
  cd HRS
  ./jp.sh  //Japanese
  ./en.sh  //English

##Operation
- Connect to it via WebBrowser. The start URL is "home.html"
