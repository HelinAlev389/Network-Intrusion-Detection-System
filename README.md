<h1>Network Intrusion Detection
System with Snort</h1>

<p><b>Task: </b>Develop a network-based intrusion detection system
using tools like Snort. Set up rules and alerts
to identify and respond to suspicious network activity.
You can even visualize the detected attacks.</p>

<h4>Coding in Two terminals</h4>

<h5>T1</h5>
<ol> 
  <li>Install Snort $ git clone https://github.com/snort3/snort3.git
  <li>ifconfig for checking your IP address and interface</li>
  <li>nmap -sX < IP_add ></li>
    <hr>
</ol>

<h5>T2</h5>
<ol> 
<li>Work as root</li>
<li>After installing snort, write nano /ect/snort/snort.lua</li>
<li>Check for HOME_NET and instead of 'any' write '< Your_IP_Add > '</li>
<li>snort -T -c /etc/snort/snort.lua</li>
<li>sudo tcpdump -i < your_interface ></li>
 
</ol>

<H3>Writing Rules</H1>

<ol>
  <li>Navigate to /etc/snort/rules</li>
  <li>Nano custom.rules for new rule file</li>
  <li>Add your rules

  <a href="https://youtu.be/HWuUW4XGxHo?si=T_z4D_2Mleqgra9S"></a>
```
    Example - credit - <a href="https://youtu.be/HWuUW4XGxHo?si=T_z4D_2Mleqgra9S"></a>

#RULES STRUCTURE

# <RULE actions> <protocol> <src ip add> <src port> <direction operator> <destination ip add> <destination port>



# ALERT ON ANY FTP CONNECTION ATTEMPT

alert tcp any any -> $HOME_NET 21 (msg: "FTP connection attempt"; sid:1000001; rev:1;)



# ALERT ON SPECIFIC IP SSH CONNECTION ATTEMPT

alert tcp any any -> 192.168.1.4 22 (msg: "SSH connection attempted"; sid:1000002; rev:1;)



# ALERT ON SPECIFIC WEBSITE VISITED

alert tcp any any -> $EXTERNAL_NET $HTTP_PORTS (msg: "Test eBay.com"; content: "Ebay.com"; nocase; sid:1000003; rev:1;)
```

</p>
</li>

<li>Save and run command short -T -c /etc/snort/snort.lua</li>
<li>Check Results</li>
</ol>
