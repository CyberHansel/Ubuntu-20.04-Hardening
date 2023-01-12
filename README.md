# Ubuntu-20.04-Hardening
## Ubuntu OSCAP check https://ubuntu.com/security/oval  
* sudo apt-get install libopenscap8  
* wget https://security-metadata.canonical.com/oval/com.ubuntu.$(lsb_release -cs).usn.oval.xml.bz2  
* bunzip2 com.ubuntu.$(lsb_release -cs).usn.oval.xml.bz2  
* oscap oval eval --report report.html com.ubuntu.$(lsb_release -cs).usn.oval.xml  
* xdg-open report.html  




