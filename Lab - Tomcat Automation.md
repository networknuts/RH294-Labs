Tim is an SRE working at a renowed MNC. His team is working on a Java based application, the developers have started writing the Java code and
have asked Tim to provide them with an instance of Tomcat to run and test the application. Since this Tomcat instance would be required multiple
times throughout the project, Tim has decided to write a Playbook to automate the provisioning of this Tomcat instance over a RHEL8.5 virtual machine.

The steps to install Tomcat manually are the following:

1. Ensure system is updated.
2. Install java-11-openjdk-devel package.
3. Download https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.60/bin/apache-tomcat-9.0.60.tar.gz archive file.
4. Extract the archive file.
5. Copy apache-tomcat-9.0.60 to /usr/local/tomcat9 .
6. Create a system user called tomcat.
7. Assign the system user tomcat owner and group ownership to /usr/local/tomcat9 recursively.
8. Copy the tomcat.service file to /etc/systemd/system/tomcat.service.
9. Start and enable the tomcat service.
10. Open ports 8080/tcp and 8443/tcp in the firewall.

Navigating to the server's IP on port 8080 should open the Tomcat home page if all steps are performed successfully. 
