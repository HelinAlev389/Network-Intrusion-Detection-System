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
