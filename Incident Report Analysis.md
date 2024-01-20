**Incident report analysis**


<table>
  <tr>
   <td><strong>Summary</strong>
   </td>
   <td colspan="3" >Recently our company experienced a distributed denial of service (DDoS) attack that caused our network to be down for 2 hours before the cybersecurity team resolved the incident. The security investigated the incident and found that a malicious actor had sent a flood of ICMP pings through an unconfigured firewall.  This vulnerability allowed the malicious actor to overwhelm the company’s network through a DDoS attack.
   </td>
  </tr>
  <tr>
   <td>Identify
   </td>
   <td colspan="3" >The security team performed an internal audit to identify what part of the network was attacked.  Logs from our security information and event management (SIEM) tool were analyzed and it was discovered that an unconfigured firewall was the vulnerability used by the threat actor to attack the network.
   </td>
  </tr>
  <tr>
   <td>Protect
   </td>
   <td colspan="3" >To address the vulnerability and to prevent future attacks through this method, the security team implemented the following measures:
<ul>

<li>A new firewall rule to limit the rate of incoming ICMP packets allowed

<li>Source IP address verification on the firewall to check for spoofed IPs on incoming ICMP packets

<li>Network monitoring software to detect abnormal network traffic patterns

<li>An IDS/IPS system to filter out some ICMP packet based upon suspicious characteristics
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Detect
   </td>
   <td colspan="3" >Using a security information and event management (SIEM) tool, it was discovered that the threat actor sent a flood of ICMP pings into the company’s network through an unconfigured firewall.
   </td>
  </tr>
  <tr>
   <td>Respond
   </td>
   <td colspan="3" >The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services, and restoring critical network services.
   </td>
  </tr>
  <tr>
   <td>Recover
   </td>
   <td colspan="3" >The IT team restored all network services to allow all employees to perform their required duties.  All systems are back online.  No data was lost.
   </td>
  </tr>
</table>



---


```
Reflections/Notes: In the future the IT will be more diligent in making sure all new systems have all configurations up to stand, including firewall rules.
```
