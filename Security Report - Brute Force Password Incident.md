# Security incident report


<table>
  <tr>
   <td colspan="2" ><strong>Section 1: Identify the network protocol involved in the incident</strong>
   </td>
  </tr>
  <tr>
   <td rowspan="2" colspan="2" >After analyzing the tcpdump files, it was determined that the protocol impacted in this incident was hypertext transfer protocol (HTTP) at the appplication layer.  The website prompts users to download a malicious file that operates on the application layer to redirect users from www.yummyrecipesforme.com to www.greatrecipesforme.com.
   </td>
  </tr>
  <tr>
  </tr>
</table>



<table>
  <tr>
   <td><strong>Section 2: Document the incident</strong>
   </td>
  </tr>
  <tr>
   <td>1. The cybersecurity team was tasked with investigating after the website owner tried to login into the administrator account but was denied.
<p>
2. I created a sandbox on a virtual machine to start the investigation.’
<p>
3. I started the network protocol analyzing tool, tcpdump, to document our network logs.
<p>
4. As soon as I accessed <a href="www.yummyrecipesforme.com">www.yummyrecipesforme.com</a>, I was prompted to download an executable file.  I downloaded the file and ran it.
<p>
5. My browser then redirected me to <a href="www.greatrecipesforme.com">www.greatrecipesforme.com</a>, which was designed to look similar to the original website with one exception: the recipes were offered for free.
<p>
6. The tcpdump shows each of the steps taken.
<p>
7. Our senior analyst confirms that the website was compromised. He found injected javascript code that directs the user to download a file.  The executable file was confirmed to contain code to redirect a visitor’s browser from <a href="www.yummyrecipesforme.com">www.yummyrecipesforme.com</a> to <a href="www.greatrecipesforme.com">www.greatrecipesforme.com</a>.
<p>
8. The cybersecurity then discovers that the web server was subject to a brute force attack in which the threat actor was able to determine the administrator password.
<p>
9. The password was still set to default and there were no safeguards against a brute force attack on the web server.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td><strong>Section 3: Recommend one remediation for brute force attacks</strong>
   </td>
  </tr>
  <tr>
   <td>1.It is highly recommended to enforce a strong password and 2FA authorization of the password on the web server and to implement password management system to limit and monitor login attempts.
   </td>
  </tr>
</table>
