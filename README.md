<h1>SOC Automation</h1>



<h2>Description</h2>
This project demonstrates the integration of  Security Operations Center (SOC) components to automate incident detection, analysis, and response workflows. The setup showcases how Wazuh, Shuffle, VirusTotal, and TheHive work together to handle security events efficiently.
<br />

<h2>Objectives</h2>
- <b>Detects security events (e.g. Mimikatz activity) using Wazuh.</b>  <br/>
- <b>Automates alert handling and investigation using Shuffle workflows.</b> <br/>
- <b>Leverages VirusTotal for threat intelligence.</b>  <br/>
- <b>Creates and manages alerts in TheHive.</b> <br/>
- <b>Notifies the user via email to start an investigation.</b> <br/>


<h2>Tools Used</h2>

- <b>Wazuh</b> 
- <b>Shuffle</b>
- <b>VirusTotal</b> 
- <b>Thehive</b>



<h2>Steps Undertaken :</h2>

  1. <b>Setup Wazuh</b><br/>
     - Installed and configured Wazuh Manager to monitor a system.<br/>
     - Created custom security rules to detect Mimikatz activity.<br/>
     - Verified alert generation in the Wazuh Dashboard.<br/>


     <img src="https://i.imgur.com/xT3Zta7.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
     
<br />
<br />
 2. <b>Integrating Wazuh with Shuffle</b><br/>
     - Configured Wazuh to send alerts to Shuffle using its API.<br/>
     - Created a workflow in Shuffle to handle incoming alerts:<br/>
             Step 1: Extract SHA hash from the alert using regex.<br/>
             Step 2: Query VirusTotal for the reputation score of the hash.<br/>
             Step 3: If the hash is malicious, proceed to alert creation in TheHive.<br/>

<img src="https://i.imgur.com/UtLyP9K.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />

  3. <b>Using VirusTotal for Threat Intelligence</b><br/>
     - Integrated the VirusTotal API in Shuffle.<br/>
     - Sent extracted SHA hashes from Wazuh alerts to VirusTotal for analysis.<br/>
     - Configured conditions in Shuffle to determine the workflow based on VirusTotal scores.<br/>
<img src="https://i.imgur.com/hXAeu4L.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
 4. <b>Creating Alerts in TheHive</b><br/>
     - Connected Shuffle to TheHive via its API.<br/>
     - Automated alert creation in TheHive with details from Wazuh and VirusTotal.<br/>

<img src="https://i.imgur.com/aOnFdAY.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. <b>Email Notification</b><br/>
     - Configured Shuffle to send an email notification upon alert creation in TheHive.<br/>
     - Used a disposable email address for testing purposes.<br/>

  <br/>
<img src="https://i.imgur.com/KGkiCEX.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />

<h2>Outcomes:</h2>
     - Integrated the VirusTotal API in Shuffle.<br/>
     - Gained experience with SOC platforms and their integration.<br/>
     - Demonstrated the practical application of Wazuh, Shuffle, VirusTotal, and TheHive in cybersecurity operations.<br/>


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
