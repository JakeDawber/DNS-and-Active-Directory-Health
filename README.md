<h1>DNS and Active Directory Health</h1>


<h2>Process</h2>

DNS Service Verification: Used netstat to confirm that DNS is listening on TCP and UDP port 53 on the domain controller's assigned IPv4 address. Successful DNS resolution and Active Directory DNS diagnostics were verified separately.

<img src="Screenshots/DNS service verification.png"/>

Active Directory DNS health: Used dcdiag to verify Active Directory DNS health and from the output, we can see that the Windows server JH-dc01 successfully passes both the connectivity test and the DNS test. We can also see that the domain jakehomelab.test successfully passed the DNS test.

<img src="Screenshots/AD health.png"/>

DNS Server Service Status: Used the sc query dns command in Command Prompt to verify that the Windows DNS Server service was running.

The output returned STATE: 4 RUNNING, confirming that the DNS service was active.

<img src="Screenshots/AD health.png"/>
