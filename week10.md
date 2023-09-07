# Week | 10 Cyber Security Controls    
## Task 1. Essential Eight Mitigation Strategies     
During the preparation of project draft in previous week, we designed a network for the owner of a multi-storey building. For the selected building, assumptions were made for designing the network efficiently. Based on the proposed network model, I selected four strategies which are regular backups, multi-factor authentication, user application hardening and patch application from three different mitigation strategies which are used to recover data and system availability, limit the extent of cyber security incidents and prevent malware delivery and execution. A detailed description of the selected strategies is provided below: 

1. Regular Backups
    For improving the system availability, and to reduce the risk of data loss it is crucial to regular backup of the data. Backing up data regularly ensures that all of the data are stored safely such that it can be recovered easily in case of incidents for restoring system functionality. For the recorded video footage from the CCTV cameras, I will implement a daily backup routine for the project scenario. Also, I can configure Network-Attached Storage (NAS) device to backup the footage automatically to cloud-based storage or external storage. 
    
2. Multi-factor authentication
    Multi-factor authentication is one of the most commonly used and successful authentication methods utilized for improving network security. By implementing multi-factor authentication on the tenants, rental agencies and owner devices as well as for certain integral cloud-based applications, I can ensure that the integrity of the network is maintained. I can implement MFA on the network to ensure that only the responsible personnel are allowed to access the CCTV system and recorded video storage. Also, the overall network security is improved by limiting the risk of unauthorized access with the use of the MFA method as it acts as an extra security layer for the network.

3. User Application Hardening
    For further enhancing network security, I will select the mitigation strategy of Restrict Administrative Privileges for the project scenario. I will ensure that the authorized individuals are only provided with administrative rights and other general users have their respective roles and responsibilities. By clearly defining the user roles and restricting the administrative rights to everyone, I can ensure that everyone cannot access and alter the sensitive information of the network. I will ensure strong password policies and provide roles-based access control to reduce the risk of insider threats and unauthorized access. 

4. Patch Application
    No system is perfect and is always prone to vulnerabilities. For the designed network scenario, I will use a patch application strategy to regularly update and patch applications in order to mitigate the known vulnerabilities. I will ensure that all of the devices utilized in the network such as cameras, NAS, routers and other devices are updated to the latest firmware and the respective security patches are installed. I can prevent the exploitation of known vulnerabilities by regularly checking the corresponding manufacture's website and updating the system regularly to ensure the smooth functioning of the network. 

**Reasons for selecting these strategies:**
Among the other strategies, I selected patch application, user application hardening, multi-factor authentication and regular backup as I found those strategies align directly with the project needs and requirement for addressing vulnerability management, user providleges, network acccess control and data availability. By focusing on these specific areas, I can make sure that the network can be safeguarded against potential cybersecurity incidents. Also, the mentioned strategies are easier to implement and also have lower user resistance in implementing the strategy.

## Task 2. Explore and Select NIST Controls   
Based on the project scenario and the selected mitigation strategies, here are six different base controls from at least three different families of controls that are relevant:

Family: System and Communications Protection (SC)

SC-7: Boundary Protection
Importance: This control is important for protecting the network from unauthorized access and preventing malicious activities from crossing the network boundary.
Implementation: Implement a firewall at the network perimeter to control incoming and outgoing network traffic. Configure the firewall to restrict access based on specified rules and policies.

Family: Access Control (AC)

AC-2: Account Management

Importance: Proper account management ensures that only authorized individuals have access to network resources, reducing the risk of unauthorized access and insider threats.
Implementation: Implement a centralized user management system to create and manage user accounts. Enforce strong password policies, enable multi-factor authentication for user accounts, and regularly review and disable unnecessary or inactive accounts.

AC-3: Access Enforcement

Importance: Access enforcement ensures that users can only access the resources and data they are authorized to, reducing the risk of unauthorized data exposure or modification.
Implementation: Implement role-based access control (RBAC) to enforce access controls based on user roles and responsibilities. Assign permissions and privileges to users based on their job functions and regularly review access rights to ensure they are up to date.

Family: System and Information Integrity (SI)

SI-2: Flaw Remediation

Importance: Flaw remediation involves identifying and addressing software vulnerabilities to prevent exploitation by attackers.
Implementation: Establish a vulnerability management process to regularly scan network devices, applications, and systems for known vulnerabilities. Develop a patch management plan to ensure timely installation of security patches and updates.
SI-4: Information System Monitoring

Importance: Monitoring the network and information systems helps detect and respond to security incidents in a timely manner, reducing the impact of potential breaches.
Implementation: Implement network monitoring tools to capture and analyze network traffic. Monitor log files, security events, and system alerts for any signs of unauthorized access, abnormal activities, or security breaches.

Family: Incident Response (IR)

IR-4: Incident Handling
Importance: Having an incident handling capability enables prompt response and effective management of security incidents, minimizing the impact and recovery time.
Implementation: Develop an incident response plan that outlines the steps to be taken in case of a security incident. Establish an incident response team, define roles and responsibilities, and conduct regular incident response drills to ensure readiness.

## Task 3. Encrypt a File  
• Screenshot of the settings used to encrypt the file.  
![Image](./images/lab10task3.PNG)

Now, I need to share my file and secret key to friend. I will share with any file sharing media that has authentication.  

It has some limitations that are:  
Complex process.  
Unauthorised access.  
Keeping the secret key secret – that can be challenging.  

I think asymmetrical cryptography should be used for sharing secret key in order to more secure.

## Task 4. View Password Information Stored in Linux  
In OpenWRT Linux VM, a new user is added and then information stored about the password are viewed in
/etc/shadow.

1. Screenshot of /etc/shadow file entries that show new user and password information is given below:  
  I added user milan and set new poassword for this user.
![Image](./images/lab10task4.PNG)

2. Explanation of the password information stored in /etc/shadow, and the actual password is not stored are described below:  
  The `/etc/shadow` file in a openWRT stores password‐related information for user accounts in encrypted form. They are just text files, with one user per line. For example I added milan user and set password for it. It stored the encrypted using hash algorithm. The second field in the /etc/shadow file contains password‐related information. The Hash algorithm used, in this case 1 = MD5. 1=MD5 and 6 = SHA‐512. And another value between $$ called random value attached to passwowd gives new hash value. The last value after : give the information about Expiry and last changed. Actual password is not stored because protect an unauthorized user from getting stored password. 

## Task 5. Setup Key-Based Authentication  
![Image](./images/Task10Task51.png)
![Image](./images/T10Task5.png)
The public key is uploaded to the SSH server, the private key is kept safely on the user's device. The challenge that the server provides during authentication can only be unlocked using the appropriate private key. Compared to passwords, which can be more vulnerable to brute-force or dictionary assaults, this cryptographic technique offers a higher level of protection.
1. Password-related vulnerabilities must be eliminated: Users choose and manage passwords while using password-based authentication. Password reuse, weak passwords, or other password-based attacks.
2. Password-related vulnerabilities must be eliminated: Users choose and manage passwords while using password-based authentication. The security of the authentication process can be jeopardised by using weak passwords, reusing passwords, or password-based attacks (such phishing and keylogging). Key-based authentication eliminates the need for passwords, lowering the danger brought on by these flaws.
3. Resistance to offline assaults: In a password-based authentication system, an attacker with access to the password database on the server can try to decrypt hashed passwords using a variety of methods, such as rainbow table attacks. Key-based authentication makes it much more difficult for an attacker to carry out offline assaults because the private key is kept securely saved on the user's device and is not sent to the server.
4. Stronger defence against brute-force attacks: Key-based authentication frequently uses keys that are far longer and more difficult than standard passwords. Brute-force attacks against the authentication process are computationally impractical because of the length and complexity of the keys.
5. Better access management: Key-based authentication gives administrators more control over who can access the SSH server. At the server level, they may maintain and revoke public keys, giving administrators fine-grained control over who can log in and use the system.



