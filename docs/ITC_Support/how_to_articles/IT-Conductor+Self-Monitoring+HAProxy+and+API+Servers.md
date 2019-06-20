IT-Conductor Self-Monitoring HAProxy and API Servers
====================================================

How to monitor IT-Conductor\'s API Servers and HAProxy Load Balancers,
Engines (Core and Jetty Slaves).  If there are problems with the API
servers (currently 4 that are load-balanced), the HAProxy should detect
it, then the AWS Route 53 will declare either 1 or both LB\'s
unhealthy.  The API servers are responsible for communications with
customer\'s ITC Gateways, and effectively receive monitoring data from
customer sites.

Step-by-step guide
------------------

Demonstration

1.  Access to service.itconductor.com as IT-Conductor administrator

2.  Access to AWS EC2 Console (optional for stopping/starting/editing
    VM)

3.  Access to SSH from OZPERFTEST01 to AWS - If Kill of the Java Jetty
    engine is required, or to monitor \'top -H\'

Recording

 

Related articles
----------------

-   Page:

[IT-Conductor Self-Monitoring HAProxy and API
Servers](file:///D:\wiki\spaces\ITCSupport\pages\29720882\IT-Conductor+Self-Monitoring+HAProxy+and+API+Servers)
