# Cybersecurity Incident Report


<table>
  <tr>
   <td><strong>Section 1: Identify the type of attack that may have caused this </strong>
<p>
<strong>network interruption</strong>
   </td>
  </tr>
  <tr>
   <td>One potential explanation for the website's connection timeout error message is a DoS (Denial of Service) attack used by flooding the web server with SYN requests.
<p>
The logs show that there were two types of errors: 1. An HTTP/1.1 504 Gateway Time-out (text/html) error message. And 2. A timeout error due to the web server not receiving a [SYN, ACK] packet.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td><strong>Section 2: Explain how the attack is causing the website malfunction</strong>
   </td>
  </tr>
  <tr>
   <td>Normally when website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol:
<p>
1. A SYN packet is sent from the client device to the web server
<p>
2. The web server returns a [SYN, ACK] packet to the client device acknowledging the request
<p>
3. An ACK packet is sent from the client to the web server
<p>
The logs initially show some of the aforementioned communication was occuring.  However, the logs show that eventually the server was overloaded with SYN requests from IP 203.0.113.0 and the server was no longer able to respond. This is like a DoS attack and steps should be taken to address it immediately.
<p>
Steps to take:
<p>
1. Shut down the web server and restart.
<p>
2. Modify the firewall to block IP 203.0.113.0
<p>
3. Notify superiors of the incident because it’s likely the threat actor will continue with additional IP’s (spoofed or not) for more DoS attacks.
   </td>
  </tr>
</table>
