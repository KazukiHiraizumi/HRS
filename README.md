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
 Add below in "/etc/lighttpd/lighttpd.conf"
  server.modules += (
	 "mod_cgi"
  )
  cgi.assign = ( ".sh"  => "/bin/bash" )
- Auto start
 sudo systemctl start lighttpd.service


