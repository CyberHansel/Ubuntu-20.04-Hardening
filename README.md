# Ubuntu-20.04-Hardening
## Ubuntu server 20.04 Fresh install hardening  
* sudo apt-get install libopenscap8  
* wget https://security-metadata.canonical.com/oval/com.ubuntu.$(lsb_release -cs).usn.oval.xml.bz2  
* bunzip2 com.ubuntu.$(lsb_release -cs).usn.oval.xml.bz2  
* oscap oval eval --report report.html com.ubuntu.$(lsb_release -cs).usn.oval.xml  
* xdg-open report.html  




