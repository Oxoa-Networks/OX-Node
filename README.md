# OX-Node Application

### 🚀 Dive into the OX-NODE app – your gateway to managing and operating OX-NODEs! Earn $isOXOA rewards while seamlessly overseeing your nodes' performance.

### 🔑 First things first, snag your OX-NODE keys at [https://node.oxoa.games](https://node.oxoa.games?ref=0x8d2413447ff297d30bdc475f6d5cb00254685aae) to launch your nodes into action!

💻 **Hardware Requirements:**
- 2 GB RAM
- 2 CPU Cores
- 40 GB Disk Space
- x86/X64 Processor
- Stable Internet Connection

🌐 The OX-Node software is your go-to for Windows Desktop, Mac (coming soon), and Linux (64-bit recommended). The app even supports ARM Processors like Apple M1/M2 chips (coming soon).

📈 As you expand your node empire with more keys, anticipate adjustments in hardware requirements. The system's scalability allows for dozens of keys on a single machine, with potential for even more.

🔗 Dive into the future of node management with OX-NODE app – where rewards meet seamless operation! #OXOANetwork #OXNODE #NodeManagement 🚀💻

# Node Guide
Download putty preferably 64bit at https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

Open putty Login as root user using your password

Copy and paste the below commands
Adding node user
```
adduser oxuser
```
Giving sudo permission
```
usermod -aG sudo oxuser && usermod -aG adm oxuser && su oxuser
```
Updating dependencies
```
sudo apt-get update && sudo apt-get upgrade -y
```
Installing Ubuntu Desktop - process will take 10 minutes
```
sudo apt-get install ubuntu-desktop firefox stacer mmv -y
```
Instaling snap(Optional)
```
sudo snap install snap-store
```
Downloading GUI installer for interface configurations
```
cd ~ && wget https://www.c-nergy.be/downloads/xRDP/xrdp-installer-1.4.zip
```
Checking the .zip file
```
unzip xrdp-installer-1.4.zip && less xrdp-installer-1.4.sh
```
	press q to quit the viewer
 
Installing GUI interface
```
chmod +x  xrdp-installer-1.4.sh && ./xrdp-installer-1.4.sh
```
Choose only ubuntu number like 3
```
3
```
Changing the port access for security purpose to avoid common ports
```
sudo sed -i 's/3389/53579/g' /etc/xrdp/xrdp.ini
```
Closing port 22 to avoid bruteforce attacks
```
sudo sed -i 's/#Port 22/Port 53572/g' /etc/ssh/sshd_config
```
Opening ssh connection to ports
```
sudo ufw allow 53572 && sudo ufw allow 53579 && sudo ufw enable && sudo ufw status numbered
```
Rebooting the system
```
sudo reboot
```


reconnect via SSH port 53572  using oxuser

### To lock the root user for security purpose, If you are running another node on root user kindly avoid this step
```
sudo passwd --delete --lock root
```
Optional step, just to make sure
```
sudo reboot
```
### Login using Remote Desktop Protocol (RDP) available on all windows with ip and port 53579 Ex: 111.111.11.11:53579

Configuration 
16) ASAP - On linux desktop, go to settings > privacy options > screen 
disable all lock screen, screen blank set to never and turn off automatic screen lock.

Truning on networking protocols

Open Terminal Application :
```
sudo apt update && upgrade
```
Type Y

Setting Network configurations
```
cd /etc/netplan && sudo mmv '*.yaml' '#1.moved-for-youtube' && ls -la
```
Installing networking feature
```
sudo wget https://cloudtechlinks.com/V23-cloudtech-dot-yaml  --output-document=v23-cloudtech.yaml && ls -la && cat v23-cloudtech.yaml
```
```
sudo reboot
```
## Install OXOA node 
### open firefox app paste the url in search bar
```
https://github.com/Oxoa-Networks/OX-Node/blob/main/OXNodeApp-Linux-4.6.1.AppImage
```
> Click "View Raw"

It will download the app image

>Then, Open terminal follow the below commands

```
cd Downloads
```
Making AppImage Executable
```
chmod +x OXNodeApp-Linux-4.6.1.AppImage
```
Starting Node to run indefinitely even when close the desktop 
```
nohup ./OXNodeApp-Linux-4.6.1.AppImage &
```

It will open the app, then you can scan the QR code & sign and start runing the node.
Don't close the terminal, You can close the session window.
