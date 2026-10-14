<h1>DNS and Active Directory Health</h1>


<h2>Process</h2>

DNS Service Verification: Used netstat to confirm that DNS is listening on TCP and UDP port 53 on the domain controller's assigned IPv4 address. Successful DNS resolution and Active Directory DNS diagnostics were verified separately.

<img src="Screenshots/DNS service verification.png"/>

Active Directory DNS health: Used dcdiag to verify Active Directory DNS health and from the output, we can see that the Windows server JH-dc01 successfully passes both the connectivity test and the DNS test. We can also see that the domain jakehomelab.test successfully passed the DNS test.

<img src="Screenshots/AD health.png"/>

