# hanaurl

docker run -p 39013:39013 -p 39017:39017 -p 39041-39045:39041-39045 -p 1128-1129:1128-1129 -p 59013-59014:59013-59014 -h hxehost -v ${PWD}/data:/hana/mounts --ulimit nofile=1048576:1048576 --sysctl kernel.shmmax=1073741824 --sysctl net.ipv4.ip_local_port_range='60000 65535' --sysctl kernel.shmmni=4096 --sysctl kernel.shmall=8388608 --name hxehost saplabs/hanaexpress --agree-to-sap-license --passwords-url https://raw.githubusercontent.com/gimmesomethinggood/hanaurl/main/password.json

To get HANA Studio:  https://tools.hana.ondemand.com/#hanatools

When setting up HANA Studio follow the procedure on the above website, or:

Procedure
To install SAP HANA Tools, proceed as follows:

Get an installation of Eclipse 2024-06 (e.g., Eclipse IDE for Java Developers).
In Eclipse, choose in the menu bar Help > Install New Software...
For Eclipse 2024-06 (4.32), add the URL https://tools.hana.ondemand.com/2024-06
Press Enter to display the available features.
Select the desired features and choose Next.
On the next wizard page, you get an overview of the features to be installed. Choose Next.
Confirm the license agreements and choose Finish to start the installation.


Connecting to the DBs:

The SYSTEMDB:
Hostname: localhost
Instance Number:  90
Mulitple containers
- System Database
username:  SYSTEM
password: HXE#Hana1!

The Tenant DB:
Hostname: localhost
Instance Number:  90
Mulitple containers
- Tenant database:  HXE
username:  SYSTEM
password: HXE#Hana1!


useful links:

https://blogs.sap.com/2021/07/21/taming-sap-hana-express-database-docker-edition-with-macos-prepare/
