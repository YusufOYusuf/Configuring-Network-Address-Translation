<h1>Configuring Network Address Translation</h1>


<h2>Description</h2>
In this lab, I learned to configure network address translation. NAT (network address translation) extends the number of usable Internet addresses. It translates private IP addresses to public addresses. It allows an organization to present a single address to the Internet for all computer connections.
<br />



<h2>Environments Used </h2>

- <b>Ubuntu 20.04.2 LTS</b> 
- <b>PuTTY SSH Client</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar click PuTTY SSH Client and proceed to put in the private IP address, port number, and click Telnet : <br/>
<img src="https://i.postimg.cc/4dNR1NMg/Screen-Shot-2022-08-10-at-3-22-12-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
<br />
In the R6 terminal window execute the following one line at a time:  <br/>
1.configure terminal<br/>
2. ip nat inside source static 10.0.0.2 122.1.1.1<br/>
3. ip nat inside source static 10.0.0.3 122.1.1.2<br/>
4. end<br/>
<img src="https://i.postimg.cc/jScDqCzV/Screen-Shot-2022-08-10-at-3-27-26-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the R6 terminal type the following commands to show the NAT configuration: <br/>
1.show ip nat translations <br/> 
2.configure terminal <br/>
<img src="https://i.postimg.cc/MGRKMTBK/Screen-Shot-2022-08-10-at-3-33-39-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
 
  
  
  
<br />
In the R6 terminal window execute the following commands to specify the inside and outside interface:  <br/>
1.interface e0/1 <br/>
2.ip nat inside <br/>
3.interface e0/0 <br/>
4.ip nat outside <br/>
5.end <br/>
<img src="https://i.postimg.cc/ZRmSgxM6/Screen-Shot-2022-08-10-at-3-41-12-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
Go to the side bar and open a new window for PuTTY SSH Client and type in the IP Address, port number, select Telnet, and click open.:  <br/>
<img src="https://i.postimg.cc/C5FfFDzq/Screen-Shot-2022-08-10-at-3-47-45-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the PC5 terminal window Ping 192.168.1.2 to observe that it allows you too:  <br/>
<img src="https://i.postimg.cc/9F9jWSHy/Screen-Shot-2022-08-10-at-3-51-37-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
   
  
<br />
Now in the R6 terminal type:  <br/>
1.show ip nat translations <br/>
<img src="https://i.postimg.cc/59mMjrPz/Screen-Shot-2022-08-10-at-4-08-22-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
  
  
 
 
  
  
  
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
