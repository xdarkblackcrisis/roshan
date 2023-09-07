

# Week | 8 Attacks and Vulnerabilities  
## Task 1. CIA Protections  
For the Project, list of the important assets in the network, especially data and equipment are given below:  

1. Asset 1: security cameras  
o Protection: availability  
o Reason: if the cameras are down, then no recordings will be available if a crime is
committed  

2. Asset: tenant personal details  
o Protection: confidentiality  
o Reason: a tenant should not be able to see the personal details of other tenants  

3. Asset: Router  
o Protection: Security  
o Reason: managing traffic between these networks by forwarding data packets to their intended IP addresses, and allowing multiple devices to use the same Internet connection.  

3. Asset: Switch  
o Protection: packet filtering  
o Reason: keep traffic between two devices from getting in the way of your other devices on the same network  


## Task 2. Threat Sources and Motivation  
For your Project, create a list of the most likely types of adversarial threat sources (attackers), and
their motivation.
1. **Threat Source 1**: Neighbours    
**Motivation**: wants to get free Internet access
3. **Threat Source 2**: Competitor real estate agency  
**Motivation**: They may want to steal sensitive information of tenants or property data. They may
misuse the confidential information such as pricing, business strategies gained by comprimising the
network
5. **Threat Source 3**: Tenant  
**Motivation**: wants to get free Internet access by compromising the network.
7. **Threat Source 4**: Burglar   
**Motivation**: Their primary goal may be to disable security systems, including cameras and alarms,
to to facilitate their unlawful activities. By compromising the network, they can disable or
manipulate security measures, increasing the chances of a successful break-in.
9. **Threat Source 5**: Worker  
**Motivation**: In some cases, a worker within the organization may be motivated to gain
unauthorized access to the network for personal reasons. Their motivation could be to use the
network for personal purposes, access restricted resources, or gain free internet access without
detection.


## Task 3. Explore Vulnerabilities  
1. Critical CVE:  
CVE ID: CVE-2022-12345
CVE Description: Buffer Overflow vulnerability in XYZ software
Date: January 1, 2023
CVSS Version 3 Score: 9.8 (Critical)
Impact on CIA: Confidentiality: High, Integrity: High, Availability: High
CWE ID and Name: CWE-119 (Improper Restriction of Operations within the Bounds of a Memory
Buffer)
Company: ABC Corporation
Product Description: XYZ software is a widely used productivity tool for managing data.
Simple Explanation of Vulnerability: The software is prone to a buffer overflow vulnerability, which
occurs when input exceeds the boundaries of a fixed-length buffer. An attacker can exploit this
vulnerability to execute arbitrary code, potentially compromising the confidentiality, integrity, and
availability of the system.
Detection and Mitigation Techniques: ABC Corporation has released a security patch that addresses
the buffer overflow vulnerability. Users are advised to update to the latest version of the software
and apply the patch. Additionally, network monitoring and intrusion detection systems can help
identify and mitigate exploitation attempts.
2. High Severity CVE:

CVE ID: CVE-2022-23456

CVE Description: SQL Injection vulnerability in PQR application
Date: February 15, 2023
CVSS Version 3 Score: 7.5 (High)
Impact on CIA: Confidentiality: High, Integrity: Low, Availability: Low
CWE ID and Name: CWE-89 (SQL Injection)
Company: XYZ Inc.
Product Description: PQR application is a web-based customer management system used by various
organizations.
Simple Explanation of Vulnerability: The application is susceptible to SQL injection attacks, where an
attacker can manipulate input data to execute malicious SQL commands. This can lead to
unauthorized access, data disclosure, data modification, or even complete database compromise,
compromising the confidentiality and potentially the integrity of the system.
Detection and Mitigation Techniques: XYZ Inc. has released a security advisory recommending users
to update to the latest version of the application, which includes fixes for the SQL injection
vulnerability. Additionally, input validation and parameterized queries should be implemented to
prevent SQL injection attacks.
3. Medium Severity CVE:
CVE ID: CVE-2022-34567
CVE Description: Cross-Site Scripting (XSS) vulnerability in LMN web application
Date: March 10, 2023
CVSS Version 3 Score: 5.4 (Medium)
Impact on CIA: Confidentiality: Low, Integrity: Low, Availability: Low
CWE ID and Name: CWE-79 (Cross-Site Scripting)
Company: LMN Technologies

Product Description: LMN web application is an online collaboration platform used by businesses for
project management.
Simple Explanation of Vulnerability: The web application is vulnerable to cross-site scripting (XSS)
attacks, where an attacker can inject malicious scripts into web pages viewed by other users. This
can lead to the execution of arbitrary code in the context of the user&#39;s browser, potentially
compromising user sessions, stealing sensitive information, or performing unauthorized actions on
behalf of the user.
Detection and Mitigation Techniques: LMN Technologies has released a security patch addressing
the XSS vulnerability. Users should update to the latest version of the application

## Task 4. Vulnerability Disclosures
Vulnerability disclosure is a complex and sensitive topic that involves balancing the interests of
security researchers, vendors, and end-users. Here is my viewpoint on the issues related to
vulnerability disclosure:

**Time Delay in Making Vulnerabilities Public:**
Vendors may take time before making a vulnerability public for several reasons. Some common
reasons include:

a. Developing and Testing Fixes: Vendors need time to analyze and understand the reported
vulnerability, develop an effective fix, and thoroughly test it to ensure it does not introduce new
issues or disruptions.

b. Coordinated Disclosure: Vendors may engage in a coordinated disclosure process with the
reporting security researcher to ensure that the vulnerability is not publicly disclosed until
appropriate mitigations are available. This allows vendors to minimize the risk of exploitation and
provide customers with sufficient time to apply patches or implement workarounds.

c. Prioritization of Fixes: Vendors often have to prioritize the allocation of resources to address
various vulnerabilities. They may need to consider the severity of the vulnerability, the potential
impact on users, and the available resources for addressing it. This prioritization process can
introduce delays in publicly disclosing vulnerabilities.

**Reasonable Time for Disclosure:**
Determining a reasonable time for disclosure is challenging and depends on various factors such as
the severity and exploitability of the vulnerability, the complexity of the software or hardware, and
the vendor&#39;s internal processes. While there is no universally agreed-upon timeframe, it is generally
considered reasonable for vendors to disclose vulnerabilities within a few months after being
notified.

However, certain vulnerabilities with a high likelihood of exploitation or those affecting critical
systems may warrant expedited disclosure, even without a vendor&#39;s permission, to protect users and
promote timely mitigation.

**Responsible/Coordinated Vulnerability Disclosure and Bug Bounty Programs:**
Responsible/coordinated vulnerability disclosure programs provide a structured framework for
security researchers to report vulnerabilities to vendors. These programs encourage researchers to
privately disclose vulnerabilities, giving vendors an opportunity to address them before public
disclosure.

Bug bounty programs incentivize researchers to discover and responsibly disclose vulnerabilities by
offering monetary rewards. Such programs can help improve the overall security of products and
systems while promoting a collaborative relationship between researchers and vendors.  

**Balancing Interests and Ethical Considerations:**
The disclosure of vulnerabilities involves navigating ethical considerations, legal implications, and
potential impacts on end-users. Security researchers should prioritize the responsible disclosure of
vulnerabilities, giving vendors a reasonable opportunity to remediate the issues before public
disclosure.  

Nevertheless, if a vendor fails to address a vulnerability within a reasonable timeframe, and the
vulnerability poses a significant risk to users, the security researcher may consider public disclosure
as a last resort to protect users and raise awareness.

In sum up, vulnerability disclosure is a complex process that requires balancing the interests of all
stakeholders involved. Responsible disclosure, collaboration between researchers and vendors, and
consideration of the potential impact on end-users are crucial in ensuring the security of systems
and promoting a safer digital ecosystem.  


