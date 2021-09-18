# port-forwading-virtualbox

### prerequisites
### Linux Users
* Install [VirtualBox](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/virtualbox/installation/virtualbox_install.sh)
* Install [OpenSSH](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/ssh/installation/openssh.sh)
### Windows Users
* Install [VirtualBox](https://www.virtualbox.org/)
* Install [PuTTY](https://www.putty.org/)

Download Virtual Disk Image(VDI)
choose your favourite linux Distribution 
* Download [osboxes](https://www.osboxes.org/)

![osboxes](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/osboxes.png)

And choose Virtual box and select favourite linux Distribution
In my case I Download CentOS 8.3 Desktop

![osboxes_web](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/osboxes_web.png)

After Extract the 64bit.7z file 

![vdi](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/vdi.png)

Click new and name the Operating System

![virtualbox_1](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_1.png)
Next, Allocate RAM size
![virtualbox_2](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_2.png)
Next, Hard Disk<br>
In this case, choose an existing virtual hard disk file

![virtualbox_3](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_3.png)
Choose our Extracted Virtual Disk Image(VDI).
![virtualbox_4](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_4.png)
Select location and Open it.
![virtualbox_5](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_5.png)
Choose the Virtual Disk Image(VDI).
![virtualbox_6](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_6.png)
Click to Create an Virtual Machine.
![virtualbox_7](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_7.png)
Now ,Virtual Machine is Created.
![virtualbox_8](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_8.png)
Click Settings and go to Network.<br>
And click Advanced Settings.
![virtualbox_9](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_9.png)
Open VirtualBox and select the VM you want to alter. Click Settings and then click on the Network tab. In the Network window expand the Advanced section and click Port Forwarding<br>
In the Port Forwarding Rules window, click the + button and fill out the new rule as such:

* Name - SSH
* Protocol - TCP
* Host IP - leave blank
* Host Port - 2222
* Guest IP - leave blank
* Guest Port - 22

![virtualbox_10](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_10.png)
Once you've filled that out<br>
click OK to save the rule.
![virtualbox_11](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_11.png)

![virtualbox_12](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_12.png)

In this case,click Start and click Headless Start(detachable mode)

One thing to note: Leaving the Host IP blank will default to 127.0.0.1 and leaving the Guest IP address blank will default to whatever IP address is assigned to the Guest. This is the most logical choice, as IP addresses change and you never know what address you'll be connecting from.<br>

If the guest VM isn't running, start it up and wait for the boot process to complete.
![virtualbox_13](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/virtualbox_13.jpeg)
# Connecting to the guest
# Linux Users
Now it's time to connect to the guest. As it stands, we're routing port 2222 on the Host to port 22 on the guest. So if you're on the Host machine, you'll Secure Shell to the guest with the command:

ssh -p2222 USERNAME@127.0.0.1O

Where USERNAME is a valid username on the Guest. You will be prompted for the user password and be given access.
* Username: osboxes
* Password: osboxes.org
* Root Account Password: osboxes.org



![ssh_1](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/ssh_1.png)

Checking OS version

![ssh_2](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/ssh_2.png)
Use exit command to logout the session
![ssh_3](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/ssh_3.png)
# Windows Users
Open PuTTY 
![putty_1](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/putty_1.png)
![putty_2](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/putty_2.png)
![putty_3](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/putty_3.png)
![putty_4](https://github.com/selvaraj-kuppusamy/port_forwading-virtualbox/blob/main/assets/putty_4.png)
