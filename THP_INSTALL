# THIS IS A WORK IN PROGRESS FILE, I STILL HAVE TO CLEAN IT UP AND ADD SEVERAL FUNCTIONS 
# TO MAKE THE PALYBOOK EASIER TO START. 10/8/2018
# Since this book is based off of the Kali Linux platform, you can download the Kali Linux distro from: http://www.kali.org/downloads/. I highly recommend you download the VMware image (https://www.offensive-security.com/kali-linux-vmware-arm-image-download/) and download Virtual Player/VirtualBox. Remember that it will be a gz-compressed and tar archived file, so make sure to extract them first and load the vmx file.


echo The Hacker Playbook 2
echo http://www.amazon.com/dp/1512214566/


# Once Your Kali VM is Up and Running
# Log in with the username root and the default password toor
# Open a terminal
# Change the password
# passwd

echo Update the image
apt-get update
apt-get dist-upgrade

echo Setup Metasploit database
service postgresql start
Make postgresql database start on boot
update-rc.d postgresql enable

echo Start and stop the Metasploit service (this will setup the database.yml file for you)
service metasploit start
service metasploit stop
Install gedit
apt-get install gedit
# Change the hostname - Many network admins look for systems named Kali in logs like DHCP. It is best to follow the naming standard used by the company you are testing
gedit /etc/hostname
echo Change the hostname (replace kali) and save
gedit /etc/hosts
echo Change the hostname (replace kali) and save

#reboot
#echo Optional for Metasploit - Enable Logging
#echo I list this as optional since logs get pretty big, but you have the ability to log every command and result from Metasploit’s Command Line Interface (CLI). This becomes very useful for bulk attack/queries or if your client requires these logs. *If this is a fresh image, type msfconsole first and exit before configuring logging to create the .msf4 folder.
#echo From a command prompt, type:
#echo “spool /root/msf_console.log” > /root/.msf4/msfconsole.rc
#echo Logs will be stored at /root/msf_console.log

echo Tool Installation
echo The Backdoor Factory:
# Patch PE, ELF, Mach-O binaries with shellcode.
git clone https://github.com/secretsquirrel/the-backdoor-factory /opt/the-backdoor-factory
cd the-backdoor-factory
./install.sh

#HTTPScreenShot
#HTTPScreenshot is a tool for grabbing screenshots and HTML of large numbers of websites.
#pip install selenium
#git clone https://github.com/breenmachine/httpscreenshot.git /opt/httpscreenshot
#cd /opt/httpscreenshot
#chmod +x install-dependencies.sh && ./install-dependencies.sh
#HTTPScreenShot only works if you are running on a 64-bit Kali by default. If you are running 32-bit PAE, install i686 phatomjs as follows:
#wget https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-1.9.8-linux-i686.tar.bz2
#bzip2 -d phantomjs-1.9.8-linux-i686.tar.bz2
#tar xvf phantomjs-1.9.8-linux-i686.tar
#cp phantomjs-1.9.8-linux-i686/bin/phantomjs /usr/bin/

echo SMBExec
echo A rapid psexec style attack with samba tools.
git clone https://github.com/pentestgeek/smbexec.git /opt/smbexec
cd /opt/smbexec && ./install.sh
Select 1 - Debian/Ubuntu and derivatives
Select all defaults
./install.sh
echo Select 4 to compile smbexec binaries
echo After compilation, select 5 to exit

echo Masscan
echo This is the fastest Internet port scanner. It can scan the entire Internet in under six minutes.
apt-get install git gcc make libpcap-dev
git clone https://github.com/robertdavidgraham/masscan.git /opt/masscan
cd /opt/masscan
make
make install

Echo Gitrob
Echo Reconnaissance tool for GitHub organizations
git clone https://github.com/michenriksen/gitrob.git /opt/gitrob
gem install bundler
service postgresql start
su postgres
createuser -s gitrob --pwprompt
createdb -O gitrob gitrob
exit
cd /opt/gitrob/bin
gem install gitrob

Echo CMSmap
Echo CMSmap is a python open source CMS (Content Management System) scanner that automates the process of detecting security flaws
git clone https://github.com/Dionach/CMSmap /opt/CMSmap

Echo WPScan
Echo WordPress vulnerability scanner and brute-force tool
git clone https://github.com/wpscanteam/wpscan.git /opt/wpscan
cd /opt/wpscan && ./wpscan.rb --update

Echo Eyewitness
Echo EyeWitness is designed to take screenshots of websites, provide some server header info, and identify default credentials if possible.
git clone https://github.com/ChrisTruncer/EyeWitness.git /opt/EyeWitness

Echo Printer Exploits
Echo Contains a number of commonly found printer exploits
git clone https://github.com/MooseDojo/praedasploit /opt/praedasploit

Echo SQLMap
Echo SQL Injection tool
git clone https://github.com/sqlmapproject/sqlmap /opt/sqlmap

Echo Recon-ng
Echo A full-featured web reconnaissance framework written in Python
git clone https://bitbucket.org/LaNMaSteR53/recon-ng.git /opt/recon-ng

Echo Discover Scripts
Custom bash scripts used to automate various pentesting tasks.
git clone https://github.com/leebaird/discover.git /opt/discover
cd /opt/discover && ./update.sh

Echo BeEF Exploitation Framework
Echo A cross-site scripting attack framework
cd /opt/
wget https://raw.github.com/beefproject/beef/a6a7536e/install-beef
chmod +x install-beef
./install-beef

Echo Responder
Echo A LLMNR, NBT-NS and MDNS poisoner, with built-in HTTP/SMB/MSSQL/FTP/LDAP rogue authentication server supporting NTLMv1/NTLMv2/LMv2, Extended Security NTLMSSP and Basic HTTP authentication. Responder will be used to gain NTLM challenge/response hashes
git clone https://github.com/SpiderLabs/Responder.git /opt/Responder

Echo The Hacker Playbook 2 - Custom Scripts
Echo A number of custom scripts written by myself for The Hacker Playbook 2.
git clone https://github.com/cheetz/Easy-P.git /opt/Easy-P
git clone https://github.com/cheetz/Password_Plus_One /opt/Password_Plus_One
git clone https://github.com/cheetz/PowerShell_Popup /opt/PowerShell_Popup
git clone https://github.com/cheetz/icmpshock /opt/icmpshock
git clone https://github.com/cheetz/brutescrape /opt/brutescrape
git clone https://www.github.com/cheetz/reddit_xss /opt/reddit_xss

Echo The Hacker Playbook 2 - Forked Versions
Echo Forked versions of PowerSploit and Powertools used in the book. Make sure you clone your own repositories from the original sources.
git clone https://github.com/cheetz/PowerSploit /opt/HP_PowerSploit
git clone https://github.com/cheetz/PowerTools /opt/HP_PowerTools
git clone https://github.com/cheetz/nishang /opt/nishang

Echo DSHashes:
Echo extracts user hashes in a user-friendly format for NTDSXtract
wget http://ptscripts.googlecode.com/svn/trunk/dshashes.py -O /opt/NTDSXtract/dshashes.py

Echo SPARTA:
Echo A python GUI application which simplifies network infrastructure penetration testing by aiding the penetration tester in the scanning and enumeration phase.
git clone https://github.com/secforce/sparta.git /opt/sparta
apt-get install python-elixir
apt-get install ldap-utils rwho rsh-client x11-apps finger

Echo noSQLMap
Echo A automated pentesting toolset for MongoDB database servers and web applications.
git clone https://github.com/tcstool/NoSQLMap.git /opt/NoSQLMap

Echo Spiderfoot
Echo Open Source Footprinting Tool
mkdir /opt/spiderfoot/ && cd /opt/spiderfoot
wget http://sourceforge.net/projects/spiderfoot/files/spiderfoot-2.3.0-src.tar.gz/download
tar xzvf download
pip install lxml
pip install netaddr
pip install M2Crypto
pip install cherrypy
pip install mako


Echo WCE
Echo Windows Credential Editor (WCE) is used to pull passwords from memory
Echo Download from: http://www.ampliasecurity.com/research/windows-credentials-editor/ and save to /opt/. For example:
wget www.ampliasecurity.com/research/wce_v1_4beta_universal.zip
mkdir /opt/wce && unzip wce_v1* -d /opt/wce && rm wce_v1*.zip

Echo Mimikatz
Echo Used for pulling cleartext passwords from memory, Golden Ticket, skeleton key and more
Echo Grab the newest release from https://github.com/gentilkiwi/mimikatz/releases/latest
cd /opt/ && wget http://blog.gentilkiwi.com/downloads/mimikatz_trunk.zip
unzip -d ./mimikatz mimikatz_trunk.zip

Echo SET
Social Engineering Toolkit (SET) will be used for the social engineering campaigns
git clone https://github.com/trustedsec/social-engineer-toolkit/ /opt/set/
cd /opt/set && ./setup.py install

Echo PowerSploit (PowerShell)
Echo PowerShell scripts for post exploitation
git clone https://github.com/mattifestation/PowerSploit.git /opt/PowerSploit
cd /opt/PowerSploit && wget https://raw.githubusercontent.com/obscuresec/random/master/StartListener.py && wget https://raw.githubusercontent.com/darkoperator/powershell_scripts/master/ps_encoder.py

Echo Nishang (PowerShell)
Echo Collection of PowerShell scripts for exploitation and post exploitation
git clone https://github.com/samratashok/nishang /opt/nishang

Echo Veil-Framework
Echo A red team toolkit focused on evading detection. It currently contains Veil-Evasion for generating AV-evading payloads, Veil-Catapult for delivering them to targets, and Veil-PowerView for gaining situational awareness on Windows domains. Veil will be used to create a python based Meterpreter executable.
git clone https://github.com/Veil-Framework/Veil /opt/Veil
cd /opt/Veil/ && ./Install.sh -c

#Burp Suite Pro
#Web Penetration Testing Tool
#Download: http://portswigger.net/burp/proxy.html. I would highly recommend that you buy the professional version. It is well worth the $299 price tag.

#ZAP Proxy Pro
#OWASP ZAP: An easy-to-use integrated penetration testing tool for discovering vulnerabilities in web applications.
#Download from: https://code.google.com/p/zaproxy/wiki/Downloads?tm=2
#Included by default in Kali Linux (owasp-zap)

#Fuzzing Lists (SecLists)
#These are scripts to use with Burp to fuzz parameters
#git clone https://github.com/danielmiessler/SecLists.git /opt/SecLists

Echo Password Lists
Echo For the different password lists, see the section: Special Teams - Cracking, Exploits, and Tricks

Echo Net-Creds Network Parsing 
Echo Parse PCAP files for username/passwords
git clone https://github.com/DanMcInerney/net-creds.git /opt/net-creds

#Installing Firefox Add-ons
#Web Developer Add-on: https://addons.mozilla.org/en-US/firefox/addon/web-developer/
#Tamper Data: https://addons.mozilla.org/en-US/firefox/addon/tamper-data/
#Foxy Proxy: https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-standard/
#User Agent Switcher: https://addons.mozilla.org/en-US/firefox/addon/user-agent-switcher/

#Wifite
#Attacks against WiFi networks
#git clone https://github.com/derv82/wifite /opt/wifite

Echo WIFIPhisher
Echo Automated phishing attacks against WiFi networks
git clone https://github.com/sophron/wifiphisher.git /opt/wifiphisher

Echo Phishing (Optional):
Echo Phishing-Frenzy
git clone https://github.com/pentestgeek/phishing-frenzy.git /var/www/phishing-frenzy
Echo Custom List of Extras
git clone https://github.com/macubergeek/gitlist.git /opt/gitlist

Echo *Remember to check http://thehackerplaybook.com/updates/ for any updates.
