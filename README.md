<h1>Wazuh Installation</h1>


<h2>Description</h2>
I played a pivotal role in fortifying our company's cybersecurity posture by successfully implementing the Wazuh Open Source SIEM (Security Information and Event Management) system by following precise instructions for installation on an Ubuntu virtual machine, creating a robust platform for monitoring active endpoints. This project showcases my expertise in deploying robust security solutions and demonstrates a hands-on understanding of Wazuh's capabilities. 
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

<br />
<br />
Then check the created files with the command

```diff

ls

```
<img src="https://i.imgur.com/D6Pdzt5.png" height="80%" width="80%" alt="Show Created Files"/>
<br />
<br />

Edit ./config.yml and replace the node, server, and dashboard names (Replacing the names are optional) and IP values with the corresponding names and IP addresses. In my case, I used the same IP address as my Ubuntu VM for the node, server, and dashboard.

```diff

nano ./config.yml

```
<img src="https://i.imgur.com/2TI3nbB.png" height="80%" width="80%" alt="Show Created Files"/>
<br />
<br />


Then run the following command to create the certificates:

```diff

sudo bash ./wazuh-certs-tool.sh -A

```
<img src="https://i.imgur.com/E5CZXPg.png" height="80%" width="80%" alt="Show Created Files"/>
<br />
<br />


<h3>Step 2: Wazuh installation</h3>

Download and run the Wazuh installation assistant.

```diff

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh && sudo bash ./wazuh-install.sh -a

```

After installation, you will see the admin username and password to access wazuh console (Save it for later).



The wazuh-install.files.tar has been created.

<img src="https://i.imgur.com/pGVLfrc.png" height="80%" width="80%" alt="Show Created Files"/>
<br />
<br />

Finally, connect to Wazuh Dashboard in your browser with the IP address assigned to your dashboard as follows:

https://xxx.xxx.xxx.xxx:443


Then, login with the administrative credentials provided after the Wazuh installation.

Note: It should be able to be connected from a different computer in the same network as the Ubuntu server.



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
