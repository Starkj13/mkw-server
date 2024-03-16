CoWFC Installer
======

This script installs the CoWFC front-end and back-end from https://github.com/EnergyCube/CoWFC

✅ Support Ubuntu 16.04 (Only tested on Ubuntu 16.04)

✅ Support Debian 10 (❌ LAN Reported not working ! Only tested on a VPS using a domain name)

🔨 Contributing
-------

Please open pull requests.

🔧 Error reporting
-------

Create a new issue and communicate all informations that you can.

📝 How to use
-------

![image](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/Ubuntu_logo.svg/100px-Ubuntu_logo.svg.png)

`mkdir /var/www ; cd /var/www && wget https://raw.githubusercontent.com/EnergyCube/cowfc_installer/master/cowfc.sh && chmod +x cowfc.sh && ./cowfc.sh`

After system reboot : `cd /var/www && ./cowfc.sh`

Remplace cowfc.sh with cowfc_for_aws_ubuntu_16.sh if you are using AWS.

![image](https://www.debian.org/logos/openlogo-nd-25.png) Debian
----

`wget https://raw.githubusercontent.com/EnergyCube/cowfc_installer/master/cowfc-debian.sh && chmod +x cowfc-debian.sh && ./cowfc-debian.sh`

🐬 Dolphin Emulator Connection
-------
After installing the CoWFC server, you need to connfigure the server by going to the admin dashboard.<br/>
The admin console is located on "http://'serverip'/?page=admin&section=Dashboard".<br/> 
Go over to "Game Whitelist" and add RMC.

Dolphine Emulator Config

1. Start Dolphin
2. Locate MKW and right-click on it and choose properties
3. Go over to Gecko-Code tab and enable it.
4. When enabled add a new line of code. (Disables SSL check)<br/>
   ```
   C0000000 0000000E
   3C004E80 60000020
   900F0000 3D808000
   618C3000 3C00017F
   6000CFFC 7C0903A6
   3D607474 616B7073
   800C0000 7C005800
   40A20034 394C0003
   392C0002 7D455378
   38600000 8C050001
   2C000000 38630001
   4082FFF4 8C0A0001
   9C090001 3463FFFF
   4082FFF4 398C0001
   4200FFC0 4E800020
   ```
   Cred [Vega](https://mariokartwii.com/showthread.php?tid=1149), for the noSSL code
6. Save and exit
7. Now is the Dolphine emulator configured

Computer Config
1. Change the DNS resolver on your computer to the ip of the CoWFC server.

Playing 🎮 <br/>
Now you should be able to launch MKW and go into the Nintendo WFC tab and start adding friends.

Have fun playing with your friends.

📖 Notes
-------

This script comes in 3 phases for Ubuntu. Each phase involves a reboot
-	Add the PHP 7.4 repo
-	Continue CoWFC install
-	Reboot after CoWFC install

This script comes in 1 phases for Debian.
-	Install CoWFC & Reboot

Ubuntu script use PHP 7.4 & MySQL\
Debian script use PHP 7.4 & MariaDB\
AWS Ubuntu 16.04 script use PHP 7.0 & MySQL

❤️ Credits
-------
kyle95wm\
EnergyCube\
[CooperAJ](https://www.youtube.com/watch?v=VUoE6R071oo&t=1040s)

