Now that you know how to configure a webserver and a load balancer, another commonly used component in an application hosting scenario is a caching server.
To do this, we will use Varnish which is a web application accelerator also known as a caching HTTP reverse proxy. Varnish Cache is really, really fast. 
It typically speeds up delivery with a factor of 300 - 1000x, depending on your architecture.

Steps to manually configure Varnish:

1. Ensure system is updated.
2. Allow port 80 in the firewall, Varnish needs to run on port 80.
3. Install the Varnish package.
4. Start and enable the Varnish service.
5. In the file /usr/lib/systemd/system/varnish.service you will find a line - " ExecStart=/usr/sbin/varnishd -a :6081 -f /etc/varnish/default.vcl -s malloc,256m"
Replace this line with " ExecStart=/usr/sbin/varnishd -a :80 -f /etc/varnish/default.vcl -s malloc,256m " 
6.  Perform a daemon-reload for the new service to be read.
7.  Copy the new default.vcl to /etc/varnish/default.vcl. Edit your webserver IP in the backend default section.
8.  Restart the service.

Navigating to the Varnish webserver should redirect you to your webserver. If you open the page console using a browser and check the properties, the 
request will be shown as delivered using Varnish Cache.


Diagram:

![alt-text](https://github.com/networknuts/RH294-Labs/blob/master/Untitled%20Diagram.drawio.png?raw=true)
