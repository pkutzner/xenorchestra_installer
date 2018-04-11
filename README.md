# Xen-Orchestra (Community Edition) Installer

Xen-Orchestra (Community Edition) allows you to administer Citrix XenServer and XCP-NG as well as backup any VM's running on these systems. 

Confirm your VM's IP Address before starting the script so you know where to login to. 

The single line installer allows you to go from a bare-minimal installation of Ubuntu to fully operational. Run the following steps from a root shell. 

    sudo bash
    <password>
    sudo curl https://raw.githubusercontent.com/Jarli01/xenorchestra_installer/master/xo_install.sh | bash
    <password>
    
The default username and password are applied, admin@admin.net and admin for the password
    
If you don't want NFS capabilities run "sudo apt-get remove nfs-common".

* Do not use LAMP
* Optional to enable SSH access/highly recommended

# Goals/Backstory for this script

I've often am asked questions similar to "why can't this be run on CentOS or Fedora" to which my only reply is and has ever been: The goal was to be the CentOS of XOA. If XOA were RedHat the goal of XOCE would to be CentOS. 

That isn't to say that this installation script won't work on other distributions, please contribute and help us to spread XOCE to other platforms. 

Initially my goal was to simply setup and start using XOCE for a tiny production shop to be able to use an open source hypervisor (Citrix XenServer) and have a management tool/backup solution. Which was initially NAUBackup and XenCenter, when I found XOA and that there was an open source management solution and backup solution that wasn't script based I jumped for it. 

That goal transformed into the desire to assist the developers of XOA by using and hopefully finding any bugs or quirks that needed to be worked out while staying in line with the original goal of being as nearly compatibile as possible to XOA.

While the goal initially was to have a solution as close to XOA as possible, with the script came the ability and goal to automate the installation. This is a big goal of the solution today, while providing an as near-match solution as possible. 
