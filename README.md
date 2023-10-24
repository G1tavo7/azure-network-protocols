# azure-network-protocols
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 - From within the VM install wireshark (64-bit)
- Step 2 - we'll use ping to see it bouncing between VM1 to VM2
- Step 3 - In VM we'll open up SSH 

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/Q6Lkwbi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After downloading wireshark and statring it up this is how the screen will look. You'll use this to start capturing packets. You can see the live traffic that is happening within the VM. When you first start it most of it will be spam, every so often you'll see your ip address. To stop this to type ICMP(Internet control Messenger Protocol) in the long bar and it will stop.
</p>
<br />

<p>
<img src="https://i.imgur.com/FDjUYRL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this I pinged from VM1 to VM2 using the private ip address that I created in azure being 10.0.0.5. Then I opened up powershell typed ping and put the private ip of VM2. You then see the reply from the system. And as we talked about packets before you see it saying that it received and set 4 packets and lost 0. In the background you see that VM1 being the source is sending it to its destination being VM2. You also see after that I typed in 'google.com" a website everyone knows and put a -4(meaning ip4 address) and it did the same thing but using the google ip address. 
</p>
<br />

<p>
<img src="https://i.imgur.com/lkPWkdG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This slide is showing how to get into ssh. To get to this page you'll have to do a few steps before getting here. You can just go thru the VM1 , type in ssh labuser@10.0.0.5. So to clarify I'll break it down so its easier to understand, the ssh stands for SecureShell, the 'labuser' part came from azure being the name of the user, and the last part being 10.0.0.5 came from the ip address. You'll have to type in the user and password that was made in azure after. When entering the password it will look like you are not typing anything in but thats just a security measure.
</p>
<br />
