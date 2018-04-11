If you are having issues before you create an issue please check the following. (We'l be asking you to look at this information anyways)

# XOC Website not loading

       systemctl status xo-server.service
       
# XOC not updating or you're stuck on a specific version.     
       
If you ever get stuck on a specific revision of XO, or are receiving an alert saying "Please tell us who you are" from git you need to run the below:

       git config --global user.email "you@example.com"
       git config --global user.name "Your Name"
      
Provide your name and email address in the quoted sections, without quotes.

# Checking the logs

       journalctl -u xo-server -f -n 50
