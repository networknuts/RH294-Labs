Jax is an SRE with Digital Ocean. He has a requirement to host websites for multiple customers. Traditionally, he would host every website on a different
server, but this approach gets expensive as multiple virtual servers need to be created. The solution is to implement virtual hosting on Apache which 
would allow Jax to host multiple websites on a single server.

Customer A information:
Company Name: BR Architects
Company URL: brarchitects.com

Customer B information:
Company Name: Quick Pizza
Company URL: quickpizza.com

Write an Ansible Playbook to demonstrate Virtual Hosting on HTTPD.

Steps for manually configuring virtual hosting:

1. Install apache 
2. Allow port 80 or HTTP in the firewall
3. Create a directory for every customer in /var/www/html (example: /var/www/html/brarchitects and /var/www/html/quickpizza)
4. Copy files of respective customers to their respective directories
5. Backup existing httpd.conf file
6. Deploy new httpd.conf with new directory roots
7. Restart the service
