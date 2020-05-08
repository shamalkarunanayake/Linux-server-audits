# IAA-IT17032070-miniproject
# Consist of server audit report .pdf file in repository
## Visit for practical demo 
-[Linux server audit](https://www.youtube.com/watch?v=6Gha-FzKgUI&t=529s)
-[Windows server audit](https://www.youtube.com/watch?v=ynt_0OsOWjg&t=56s)

## Below mentioned are the commands for installing and performing the following audits in linux server(Ubuntu 16.04).

## Linux server audits using Lynis tool
- dpkg -s apt-transport-https | grep -i status
- sudo apt-get install apt-transport-https
- sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys C80E383C3DE9F082E01391A0366C67DE91CA5D5F
- sudo add-apt-repository "deb [arch=amd64] https://packages.cisofy.com/community/lynis/deb/ xenial main“
- sudo apt-get update
- sudo apt-get install lynis
- lynis show commands
- lynis show settings 
- lynis update info
- sudo lynis audit system

## Linux server audits using Wapiti tool
- Sudo apt-get install wapiti
- hostname -i 
- wapiti http://10.140.0.3 -n 10 -b folder
- Download index.html

## Linux server audits using OpenSCAp tool
- sudo apt-get install libopenscap8 –y
- sudo apt-get install wget –y
- wget https://people.canonical.com/~ubuntu-security/oval/com.ubuntu.xenial.cve.oval.xml
- oscap oval eval --results /tmp/oscap_results.xml --report /tmp/oscap_report.html com.ubuntu.xenial.cve.oval.xml
- sudo cp /tmp/oscap_report.html /var/www/html/
- /var/www/html/oscap_report.html

