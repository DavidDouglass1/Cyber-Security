# Cybersecurity Incident Report: 

# Network Traffic Analysis

<table>
<colgroup>
<col style="width: 80%" />
<col style="width: 19%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><p>Part 1: Provide a summary of the problem found in the
DNS and ICMP</p>
<p>traffic log.</p></th>
</tr>
<tr class="odd">
<th colspan="2" rowspan="2">The UDP protocol reveals that the DNS server
is unreachable. This is based on the results of the network analysis,
which show that the ICMP echo reply returned the error message: “UDP
port 53 unreachable.” The most likely issue is that the DNS server is
down or overloaded.</th>
</tr>
<tr class="header">
</tr>
</thead>
<tbody>
</tbody>
</table>

| Part 2: Explain your analysis of the data and provide at least one cause of the incident.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Time incident occurred today when customers of [<u>www.yummyrecipesforme.com</u>](http://www.yummyrecipesforme.com) reported not being able to access the website. The IT started the investigation by trying to reach the website but got the error “destination port unreachable.” The IT team then used the network analyzer tool, tcpdump, and tried to access the web site again. The analyzer tool showed that when the UDP packets were sent and the ICMP response was received an error message was shown: “UDP port 53 unreachable.” Port 53 is the port used by the DNS server so we suspect the DNS server is down and there is a possible threat actor(s) causing it. We should take steps to prevent further attacks. |
