![image](https://user-images.githubusercontent.com/109401839/230745596-57cee9bd-687c-427d-b0db-d1080df77f7e.png)


<h1>Firewall Configuration in Microsoft Azure</h1>
This walkthrough demonstrates how to configure a firewall in Microsoft Azure to deny specific traffic to your VM.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Wireshark

<h2>Operating Systems Used </h2>

- Windows 10
- Linux

<h2>Walkthrough Steps</h2>

<p>
</p>
<p>
Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM.
  
 <img src="https://github.com/user-attachments/assets/d06bbcbf-d1b3-41c8-851a-b046cca82087" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
</p>
<p>Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic. 
</p>
<img src="https://github.com/user-attachments/assets/d34c02ee-7c49-4ca6-ad72-916ef63e8e6b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/492d8472-cc2e-4545-b36d-db662b66c7da" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/38a9f58a-2467-400c-bf53-9e9bd3c57747" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
</p>
<p>
Back in the Windows 10 VM, observe the ICMP traffic in Wireshark and the command line Ping activity. The requests should be timed out.
</p>  
<img src="https://github.com/user-attachments/assets/14296822-b2b3-48c5-a823-3eba3f0eb9fd" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/db750ccd-f8d9-47b5-8794-6e7da354c0d7" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<br />
</p>
<p>
Re-enable ICMP traffic for the Network Security Group on your Ubuntu VM. 
</p>
<img src="https://github.com/user-attachments/assets/a50ee6b8-0ff0-4845-ad1f-a57a8a2f78ec" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Back in the Windows 10 VM, observe the ICMP traffic in Wireshark and the command line Ping activity (should start working).
</p>
<img src="https://github.com/user-attachments/assets/cbbcd107-dfd4-44e2-a718-19b917e99bc2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
</p>
<p>
Use the command "Control-C" to stop ping activity.
</P>
<img src="https://github.com/user-attachments/assets/b56c28e9-1ae9-4594-9500-3c9bcd179598" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


