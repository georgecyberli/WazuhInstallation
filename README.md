<h1>Wazuh Installation</h1>


<h2>Description</h2>
I successfully implemented the Wazuh Open Source SIEM (Security Information and Event Management) system by following precise instructions for installation on an Ubuntu virtual machine. This project showcases my expertise in deploying robust security solutions and demonstrates a hands-on understanding of Wazuh's capabilities. 
<br />


<h2>Languages and Utilities Used</h2>

- Linux Terminal
- Curl
- Bash

<h2>Environments Used </h2>

- <b>Ubuntu</b> 22.04.3

<h2>Program walk-through:</h2>

<h3>Step 1: Certificate creation</h3>

Run the following commands to download the wazuh-certs-tool.sh script and the config.yml configuration file:

```diff

curl -sO https://packages.wazuh.com/4.7/wazuh-certs-tool.sh

```
```diff

curl -sO https://packages.wazuh.com/4.7/config.yml

```

Then check the created files with the command

```diff

ls

```



Edit ./config.yml and replace the node, server, and dashboard names (Replacing the names are optional) and IP values with the corresponding names and IP addresses. In my case, I used the same IP address as my Ubuntu VM for the node, server, and dashboard.

```diff

nano ./config.yml

```



Then run the following command to create the certificates:

```diff

sudo bash ./wazuh-certs-tool.sh -A

```



<h3>Step 2: Wazuh installation</h3>

Download and run the Wazuh installation assistant.

```diff

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh && sudo bash ./wazuh-install.sh -a

```

After installation, you will see the admin username and password to access wazuh console (Save it for later).



The wazuh-install.files.tar has been created.



Finally, connect to Wazuh Dashboard in your browser with the IP address assigned to your dashboard as follows:

https://xxx.xxx.xxx.xxx:443


Then, login with the administrative credentials provided after the Wazuh installation.





<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
