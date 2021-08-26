# Manila - Filesystems-as-a-service - on Jetstream2
 
Manila is the file share service project for OpenStack. Manila provides the management of file shares for example, NFS and CIFS, as a c    ore service to OpenStack. Manila works with a variety of proprietary backend storage arrays and appliances, with open source distribute    d filesystems, as well as with a base Linux NFS or Samba server.
Prereqs: Make sure you have the nfs client installed on your instance: *apt install nfs-common* for Ubuntu and *yum install nfs-utils*     for CentOS.
 

## To use Manila via Horizon 
 
### Create the share

1. Click on:  Project  → Share → Shares → Create Share

    ![image](../images/Manila1.png) &nbsp;       

2. Create a share with the following settings:
    - protocol - nfs,
    - share type - cephnfstype 
    &nbsp;  

    ![image](../images/Manila2.png)


### Add an interface on the Manila network to an instance

1. Click Compute → Instances screen

2. Click Attach Interface (under Create Snapshot tab at far right)


    ![image](../images/Manila3.png) &nbsp;


3. Attach to manila_testing (10.255.0.0/16) network.


    ![image](../images/Manila4.png) &nbsp;


4. The instance should show the interface.


    ![image](../images/Manila5.png)


### Attaching instance to the Manila network

1. On a running instance add an interface on the manila_testing network.