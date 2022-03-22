More than 455 million websites in the world use Wordpress as a CMS - Content Management System. It is installed on top of the LAMP stack, in this lab
you will attempt to automate Wordpress installation using Ansible.


Manual Steps:

1. Install the following packages:
- php-mysqlnd
- php-fpm
- mariadb-server
- httpd
- tar
- curl
- php-json
2. Allow service HTTP and HTTPS in the firewall
3. Start and Enable the mariaDB service
4. Create a new database in mariaDB named wordpress and give new user admin access to the wordpress database with an appropriate password
5. Download and extract https://wordpress.org/latest.tar.gz
6. Copy the wordpress directory to /var/www/html/
7. Allow the HTTPD service system user access to the newly copied directory recursively and change SELinux security context to httpd_sys_rw_content_t
8. Once done successfully, navigate to your IP and follow the on screen steps.
