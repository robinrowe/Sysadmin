# Sysadmin

4 June 2022 robin.rowe@cinepaint.org

* Hosts Testing
* Bind9 DNS Server
* MySQL Database Server
* Apache2 Web Server
* Postfix Mail Server
* Major Domo List Server
* sftp File Server
* Projeqtor CRM Server
* Forma LMS Server
* Agoracart Ad Server
* Jobberbase Job Server
* OpenAI
* ProjectSend
* Moodle
* BigBlueButton

# Testing with etc/hosts

When migrating to a new server, temporarily override DNS locally in the etc/hosts file to test the new server. This is a little complicated on Windows 11 because if opened in ordinary notepad, the file is read-only. Windows requires opening hosts using RunAs admin. In the Windows Searrch box (magnifier icon, desktop bottom left), type 'cmd' then right-click and choose to run as administrator. In the resulting cmd window, run this notepad command, then append the new server's ip address and host name:

	notepad %SystemRoot%\System32\drivers\etc\hosts
	
It takes effect as soon as the hosts file is saved. Note that Windows nslookup will still report the DNS IP address, but ping will use the IP address from hosts.

