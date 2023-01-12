# Ubuntu-20.04-Hardening
## Ubuntu server 20.04 Fresh install hardening with Ansible  
sudo apt install libopenscap8  
sudo apt install scap-security-guide  
echo 'deb http://download.opensuse.org/repositories/systemsmanagement:/Uyuni:/Stable:/Ubuntu2004-Uyuni-Client-Tools/xUbuntu_20.04/ /' | sudo tee /etc/apt/sources.list.d/systemsmanagement:Uyuni:Stable:Ubuntu2004-Uyuni-Client-Tools.list  
curl -fsSL https://download.opensuse.org/repositories/systemsmanagement:Uyuni:Stable:Ubuntu2004-Uyuni-Client-Tools/xUbuntu_20.04/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/systemsmanagement_Uyuni_Stable_Ubuntu2004-Uyuni-Client-Tools.gpg > /dev/null  
sudo apt update  
sudo apt install scap-security-guide  
## Intall ssg packages  
sudo apt install ssg-base ssg-debderived ssg-debian ssg-nondebian ssg-applications  
## ssg packages will be available in /usr/share/xml/scap/ssg/content  
ls /usr/share/xml/scap/ssg/content 
## download ssh packages and unzip  
wget https://github.com/ComplianceAsCode/content/releases/download/v0.1.60/scap-security-guide-0.1.60.zip  
unzip -q scap-security-guide-0.1.60.zip  
## packages available   
ls scap-security-guide-0.1.60 
## it contains ssg packages for ubuntu 20.04  
ls -al scap-security-guide-0.1.60/ssg-ubuntu2004-ds*  
## check available profiles  
## `–fetch-remote-resources` allows the oscap command to download remote components referenced from DataStream  
sudo oscap info --fetch-remote-resources scap-security-guide-0.1.60/ssg-ubuntu2004-ds.xml  


