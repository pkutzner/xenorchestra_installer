If you are having issues before you create an issue please check the following. (We'll be asking you to look at and provide this information anyways)

# XO Website not loading

       systemctl status xo-server.service
       
 A properly running system should look similar to this:
  
       	systemctl status xo-server.service
	● xo-server.service - XO Server
	   Loaded: loaded (/lib/systemd/system/xo-server.service; enabled; vendor preset
	   Active: active (running) since Wed 2018-04-11 08:51:41 EDT; 51s ago
	 Main PID: 710 (node)
		Tasks: 10 (limit: 4915)
	   Memory: 120.2M
		  CPU: 2.209s
	   CGroup: /system.slice/xo-server.service
			   └─710 /usr/local/bin/node ./bin/xo-server
       
# XO not updating or you're stuck on a specific version.     
       
If you ever get stuck on a specific revision of XO, or are receiving an alert saying "Please tell us who you are" from git you need to run the below:

       git config --global user.email "you@example.com"
       git config --global user.name "Your Name"
      
Provide your name and email address in the quoted sections, without quotes and once done try updating again. 

# Checking the logs

This will check and continually update the last 50 log files for your XOCE installation and thus is subject to any specific issues you're encountering. Just keep this command at the ready to check on things if you need too. 

       journalctl -u xo-server -f -n 50

# Required Dependencies 

Your system must be able to install the following list of dependencies, usually this is automatic but some distributions might not have the required repositories. Plese confirm you can install these before creating a ticket. 

Check your distribution respositories list ie: ```/etc/apt/sources.list``` for multiverse. 

* build-essential 
* redis-server 
* libpng-dev 
* git 
* python-minimal 
* libvhdi-utils 
* nfs-common

These dependencies (on Ubuntu) are available from the ```multiverse``` and ```universe``` repositories. 
