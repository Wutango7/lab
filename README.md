# lab
Materials used:

Books
Destination CISSP 
Think like a Manager 

Practice Exams
Boson Practice Exam 
50 CISSP Practice Questions. Master the CISSP Mindset 
CCC Practice Exams 
ISC2 Community page 
Pocket Prep CISSP 
Destination CISSP Practice Questions 

Videos
CISSP Exam Cram - Inside Cloud and Security 
Why you will pass the CISSP exam 
Mind Maps 

Misc.
Sunflower Guide pdf 

Policies - Documents that communicate management's goals and objectives. Provides authority. Corporate laws
Standards - Specific hardware and software solutions, mechanisms, and products. Ex: McAfee, ISO 27001
Procedures - Step-by-step descriptions on how to perform a task. 
Baseline - Minimal implementation methods/levels for security mechanisms and products.
Guidelines - Recommendations or suggested actions.

STRIDE - Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Evaluation of Privilege - Microsoft, less strategic
PASTA - Attacker-focused, risk-centric methodology
DREAD - Damage, Reproducibility, Exploitability, Affected Users, Discoverability. Measure and ranks severity of threats

SLR vs. SLA

SLR - Outlines detailed service descriptions, service level targets, and mutual responsibilities.
SLA - Performance levels, governance, security, compliance, liabilities.

Lattice-based Models
Bell-LaPadula - Lattice-based Confidentiality - Simple security property, Star Property, Strong Start Property
Biba - Lattice-based Integrity - Simple Integrity property, Star integrity, invocation Property

Lipner Implementation - Combines both Bell-LaPadula and Biba. 

Rule-Based Models
Information Flow - Helps to identify covert channels. Tracks the flow of information
Clark-Wilson - Rule-based Integrity - Prevents unauthorized subjects from making any changes. Prevents authorized subjects from making bad changes, maintains consistency of the system.
Brewer-Nash (The Chinese Wall) - Rule-based confidentiality Prevents conflicts of interest
Graham-Denning - Rules pertaining to allowing a subject to access an object
Harrison-Ruzzo-Ullman - Rule-based Integrity - Focused on access rights via a finite set of rules available to edit the access rights of a subjects.

Certification - Comprehensive technical analysis of a solution or a product to ensure it meets the desired needs.
Accreditation - Official management signoff of certification for a set period of time.

Common Criteria - ISO 15408

Security Kernel - Controls access to any asset. It's the implementation of controlling access is the security kernel. Completeness - Impossible to bypass the mediation. Isolation - Tamper-proof. Only authorized individuals should be able to change rules. Verifiability - Aspect of assurance. Being able to verify that the kernel is working properly. Done through logging and monitoring.

TCB - Trusted Computing Base - All protection mechanisms within an architecture. Hardware, firmware, software processes.

CPU - Brains of a computer, Performs instructions. Fetch, Decode, Execute, Store
Supervisor State - Higher privilege level. System kernel runs here, allowing full access to all of the instructions and capabilities of a CPU.
Problem State  Lower privilege level. Limited access to CPU instructions. Standard operating mode. Solves problems.

Time-division Multiplexing - Process isolation determined by the CPU. CPU allows very small slots of time to each process.
Memory segmentation - Separating memory segments from each other to protect the contents.

Firmware - Software that provides low-level control of hardware systems.
Middleware - Acts as an intermediary between two applications. It can speak the languages of two disparate applications and communicate between them.

Race condition - Short window of time between when something is used and when authorization or access for that use is checked.

ICS - Control systems related to industrial processes and critical infrastructure.

Types of ICSs

SCADA - System architecture that comprises computers, networking, and proprietary devices as well as GUIs for management. Small and large-scale industrial infrastructure.
DCS - Process control systems that monitors, controls and gathers data from controllers and sensors. Controlled locally.
PLC - Used to control manufacturing processes. Ease of programming and diagnosis of process problems.

CaaS - Package of software that contains all the components needed to run the software on any system. Can allow for multiple programming language stacks.
FaaS - Serverless and microservices. Runs without server architecture. Used to provide specific business functionality.

SPML - Services Provisioning Markup Language - Deprecated XML-based, standard to allow cooperating users, resource owners, and services providers of a federation to exchange information for provisioning.
SAML - Security Assertion Markup Language - XML-based OASIS standard that uses security tokens. Used for service requests.
OAuth - Federation Identity Management that works in conjunction with OpenID. Provides users and applications with secure delegated access.

XSS - Involves injecting a malicious script into a trusted website. Target is the user's browser.
     Stored/persistent - Attacker finds a vulnerable website, injects code, the user visits the website, the browser automatically downloads and executes the code, information is sent to the attacker.
     Reflected/Nonpersistent - Attacker sends a malicious URL to a victim, Victim clicks the URL, vulnerable website reflects malicious code to the victim, victim's browser executes reflected code, JavaScript code executes.
CSRF - Relies on persistence facilitated by cookies in browsers. Attacker forges a request, Attacker embeds a forged request in a hyperlink and sends it to a victim, victim clicks the link sending the request to a legitimate entity. Attacker is logged in as the victim. Target is the web server. 

Differences
XSS - Unwanted action performed on a user's browser. User's browser (client) runs malicious JavaScript code. User's browser is exploited.
CSRF Unwanted action performed on a trusted website. Website (server) executes a command from trusted user's browser. Web server is exploited.

IV - Random number that is used in conjunction with the key and fed into a cryptographic algorithm when encrypting plaintext. Used to prevent patterns in ciphertext.
Confusion - Focuses on hiding the relationship between the key and the resulting ciphertext. If one bit of the key is changed, half of the bits in ciphertext changes.
Diffusion - If a single bit of plaintext is changed, the half of the bits in ciphertext should change. Hides the relationship between plaintext and ciphertext.
Substitution - Characters are replaced with a different character. GUBBINS > JXEELQV
Transposition - The order of characters is rearranged GUBBINS > BINBUGS

Synchronous - Timing element is involved. Encryption/decryption requests are performed immediately
Asynchronous - Dictated by some other element or entity that requires input. Encryption/decryption requests are processed in batches.

Stream - Used for things to process one bit at a time. Used for hard drives
Block - Used for things like software and emails.

ECC advantage over RSA is that it allows for a shorter key with the same level of security. ECC is faster and more efficient. Useful for there is limited bandwidth, computational power, and storage like on mobile phones.

Factoring - Used for large prime numbers. Multiplication is done quickly and easily. Multiplies prime numbers.
Discrete logarithms - Any prime number is raised to the power of another prime number. Much faster.

Diffie-Hellman is widely used due to its power of using session keys. Allows for VPN solutions. Allows for fast encryption and decryption.

Symmetric algorithms are used for bulk processing and speed. Asymmetric algorithms are used to exchange symmetric keys with hybrid cryptography.

The primary goal of MICs is to ensure that messages remain unchanged from the time of creation to the time they're read. It's for integrity.

S/MIME - Standard for public key encryption and provides security services for digital messaging applications. Requires the establishment or utilization of a public key infrastructure (PKI) in order to work.

Differences between MIME and S/MINE 

MIME doesn't address security issues. S/MIME added email messaging features such as digital signatures for authentication, encryption, and hashing for message integrity and nonrepudiation of origin.

Cryptanalytic Attacks vs. Cryptographic Attacks

Cryptanalytic Attacks - Ciphertext only, known plaintext, chosen plaintext, chosen ciphertext, linear and differential, and factoring. Goal is to determine the key.
Ciphertext only - Most difficult attack, Known plaintext - Plaintext/ciphertext pair is available, Chosen plaintext - All elements except the key are known; plaintext is attacked. Chosen ciphertext - All elements except the key are known; ciphertext is attacked.

Cryptographic Attacks - Man-in-the-middle, replay, temporary files, implementation, side-channel, dictionary attack, rainbow tables, birthday, and social engineering.
Linear and differential. Differential analysis is a form of chosen-plaintext attack. Linear uses a known-plaintext attack.

Encapsulation - Application to Physical is encapsulation. Each layer adds its own header and trailer information to the existing data.
Decapsulation - Physical to Application is decapsulation.

OSI

Application - Interacts data from the user. Used to initiate communications. Responsible for protocols and data manipulation. HTTP, Telnet, FTP.
Presentation - Prepares data so that it can be used by the application layer. Makes data presentable for applications. Encryption and Decryption.
Session - Used to open and close communications between two devices. Ensures the session stays open long enough to transfer all data exchanges. PAP, CHAP, EAP, NetBIOS, RPC
Transport - Used for end-to-end communication between two devices. Reassembles segments into data. Flow control. TCP and UDP.
Network - Transfer of data between two different networks. Deals with breaking segments into packets. Routing. ICMP and Ipsec.
Data - Deals with data transfer between two devices on the same network. Breaks packets into smaller frames.
Physical - Physical equipment with data transfer. Cables and switches. Data conversion into bit streams from 1s and 0s.

Polling - Devices poll from each other to learn if any information needs to be transmitted. 

CSMA - Devices are connected to the same carrier, the same wire, and there for each device can sense the wire to identify if another device is transmitting.
CSMA/CA - Used within wireless networks. Uses two lanes of communication. 
CSMA/CD - Collision Detection - Detects collusions after the information has been transmitted. All wired networks use CSMA/CD

ARP - Allows IP addresses to be mapped to physical addresses.
RARP - Allows physical addresses to be mapped to IP addresses.

PPP - Used to allow remote access, typically via VPN solutions.
PAP - Prompts for a user to provide a User ID and password when establishing a connection. Passwords are in plaintext.
CHAP - Passwords are encrypted during transmission. Challenges are sent in regular intervals behind the scenes. 
EAP - Most robust and flexible authentication protocol. Allows for digital certificates and smart keys. Used for WPA2.
PEAP - Improved version of EAP. Encapsulates EAP within an encrypted and authenticated TLS tunnel.

SRTP - Secure version of RTP. Supports encryption authentication integrity and replay attack protection. Used for streaming voice and video over IP.
SIP - Responsible for initiating, maintaining, and terminating voice and video sessions.

Differences between Smurf and Fraggle
Smurf - Attacker spoof their IP address to match the victim's, Attacker sends multiple ICMP echo requests, ICMP replies are sent to the attacker.
Fraggle - Sends UDP packets to a system.

Bastion host - Hardened hosts and applications that sit within the DMZ.

NAT - Allows you to translate private IP addresses to public ones and vice versa
PAT - Allows for port translation. Uses port numbers for IP addresses. Uses port assignments.

Dual-Homed Host - Allows support at all OSI layers using two network cards.
Screened Host - Combines Dual-Homed Host and packet filtering. Allows screening for bastion hosts. Acts as a barrier.
Screened Subnet - Two firewalls are used and between them is a subnet such as a DMZ.
Three-Legged Firewall - Three connection points. 

Allow List (Whitelist) - Following list may be allowed. All other addresses are not permissible.
Deny List (Blacklist) - Following list may not be allowed. All other addresses are permissible.

Endpoint security focuses on protection of devices found on corporate networks and seeks to minimize the attack surface. Laptops, mobile devices, printers, IoT, etc.

Tunneling is the process of taking a datagram and placing it inside the data portion of another datagram. 
Encapsulation - Places the original datagram inside the data portion of another one.

GRE - Tunneling protocol that can encapsulate a variety of protocols and route them over IP networks. Allows for both IPv4 and IPv6 traffic. Not considered secure. No encryption.
Split Tunneling - Allows a user to access disparate resources without having traffic pass through the VPN. Allows to send portions of traffic with also encryption. Can be bypassed.

SSH-Layer 7
SOCKS-Layer 5
SSL/TLS-Layer 4
IPsec-Layer 3
L24
Pptp-layer2

IPsec
AH - Provides integrity, data-origin authentication, and replay protection.
ESP - Provides everything plus confidentiality through encryption of the payload.
Transport Mode - Uses the header of the original packet, followed by the AH or ESP header, then the payload.
Tunnel Mode - New header, encapsulates the AH or ESP header and the original IP header and payload.

RADIUS - Application-layer protocol that allows a user to connect to and access network resources. Designed for dial-in networking for AAA.
TACACS+ - Uses TCP and encrypts all transmitted packets. More Secure version of RADIUS.
Diameter - Enhanced version of RADIUS by adding EAP.

Identification -Refers to the assertion of a user's identity or a process to a system.
Authentication - Refers to the verification of an identity through knowledge, ownership, or characteristic.
Authorization - Refers to the level of access defined for the identified and authenticated user or process.
Accountability - Refers to proper identification, authentication, authorization that is logged and monitored.

Asynchronous - One time  passwords (Less common)
Synchronous - One time passwords (more common)

Smart Card - Contains a small embedded integrated circuit that performs calculations.
Memory Card - Memory stored on a card on a magnetic strip on the back of the card.

SEASAME - Secure European System for Applications in a Multi-Vendor Environment - Like Kerberos for enabling single sign-on. Supports symmetric and asymmetric cryptography.

SAML Components:
Assertion - Authentication, Authorization, and other attributes. 
Protocol - Defines how entities request and respond to requests.
Bindings - Mapping of SAML onto standard communication protocols like HTTP.
Profiles - Defines how SAML can be used for different business use cases.

Authorization mechanisms

DAC - Asset owner determines who can access the asset. Owner decides
Mandatory - System decides based on labels.
RBAC - Based on rules. Granular.
Role-based - Job functions or roles.
Attribute-based - Granular and based on user attributes like job function, type of device, working hours, etc.

eXtensible Access control Markup Language (XACML) - Defines and enables attribute-based access control. Allows attribute-based access to be implemented in a standardized manner.

Validation: Asks questions like: Is this the right product being built? Used to verify requirements. Are we building the right product?
Verification: confirmation of a product. Is the product being built correctly? Testing is used here. Are we building the product right?]

Role of a security professional is to Identify risks, advise testing processes to ensure risks are appropriately evaluated, provide advice and support to stakeholders.

Security testing stages:
Plan - Capture related requirements to a system before any design takes place.
Design - What types of controls the system should have to protect security principles.
Develop - Confirm the required controls are being developed correctly.
Deploy - Moving an application from a testing environment to production.
Operate - Configuration management reviews to ensure the product is working as intended.
Retire - Safely disposing from an old place to a new one.

SAST vs. DAST

SAST - looks at the underlying source code of an application while the application is not running. White box testing.
DAST - Examines an application and system as the underlying code executes. Black box testing.
Fuzz - Random dynamic testing.
     Mutation dumb fizzes - randomly changed by flipping bits or replacing random input. 
     Generation - New input is developed from scratch. Fuzzer must understand the input structure.

Positive Testing - Response of a system based upon normal usage and expectations. Checks to see if an application is running as designed.
Negative Testing - Focuses on the response of a system when normal errors are introduced.
Misuse Testing - Focuses on trying to break the system.

Boundary value analysis - Identifying where there are changes in behavior. Focuses on groups that exhibit the same behavior.
Equivalence partitioning - Evaluates and test against groups of inputs that exhibit the same behavior. Focuses on testing extreme ends of input values.

Decision Table Analysis - Different input combinations are used with their corresponding system behavior/output and then captured onto a table.
State-Based Analysis - Set of abstract states that a unit of software can take are defined and tests compare its actual state to the actual state. Taking the baseline and testing against it. Actual state vs. expected state.

Vulnerability assessment testing process

Reconnaissance - Passively gather publicly available information
Enumeration - Actively enumerate through target IP addresses and ports.
Vulnerability Analysis - Identify potential weaknesses.
Execution - Attempt to exploit the vulnerabilities.
Document Findings - Identify severity of findings and report to appropriate audiences. 

Banner grabbing - helps identify software and versions
Fingerprinting - Looks at how the packet is formed and similar attributes to identify the unique characteristics of a system.

Differences between CVE and CVSS
CVE - List of security flaws and vulnerabilities that are publicly disclosed for awareness and risk mitigation. Used to identify vulnerability and records the specific time.
CVSS - A framework used to give metrics and characteristics to a vulnerability. Uses a scoring system. Assigns a number between 0 and 10. 

Circular overwrite - Once the log file reaches the maximum size or length, log entries start to overwrite. It's from the earliest to the most recent.
Clipping levels - Focuses on when to begin logging. Logging failed login attempts. Predefined thresholds are used.

Real User Monitoring - Monitors user interactions and activity within a website or application.
Synthetic performance monitoring - examines functionality as well as functionality under performance under load. Runs scripted transactions.

KRI - Forward-looking metrics that indicate the achievement of performance targets. Provides insights about risk events that have already affected the organization.
KPI - Backward-looking metrics that indicate the level of exposure to operational risk. Helps to better monitor potential future shifts in risk conditions.

SMART Metrics - Specific, Measurable, Achievable, Relevant, Timely. Used for goal setting, taking action, etc.

Internal vs. external, vs. third party
Internal - Employees focused on organizational processes.
External - Employees focusing on vendor processes.
Third Party - Independent auditors focusing on vendor processes.

SOC 1 - Financial reporting risks
SOC 2 - Five trust policies of security, availability, confidentiality, processing integrity, and privacy. Goes over controls related to security.
SOC 3 - Stripped down and sanitized version of a SOC 2 report used for marketing.

Type 1 report focuses on the design of controls at a point int time. Focuses on paperwork, policies, procedures, and baselines. Point in time evaluation.
Type 2 - Focuses on design of controls as well as operating effectiveness over a period of time.

Executive (Senior) Management - Sets the proper tone from the top, promotes the audit process, and provides support where needed.
Audit Committee - Composed of members of the Board to give insight.
Security Officer - Advice on security related risks to be evaluated.
Compliance Manager - Ensure corporate compliance is being taken placed with laws and regulations.
Internal Auditors - Company employees who provide assurance that corporate internal controls are operating effectively.
External Auditors - Provides an unbiased and independent audit report for tests.

Real evidence - Tangible physical objects like hard drives and USB drives.
Direct evidence - requires no inference. Video footage.
Circumstantial evidence - Indirect evidence that is by implication or inference. Someone was at the scene when it occurred.
Corroborative evidence - Supports facts or elements of the case. Supports other facts.
Hearsay evidence - Testimony by witnesses who were not present.
Best evidence rule - Original evidence rather than a copy or duplicate is the best evidence.
Secondary evidence - Reproduction or a substitute of evidence. Log files.

MOM - Motive Opportunity Means - Serves as a guide when conducting an investigation. Searches for the reason why the criminal committed the crime.
Locard's Exchange Principle - Whenever a crime is committed, something is taken and something is left behind. Example, pictures, carpets, fingerprints, etc.

Artifacts - remnants of a breach or attempted breach of a system or network. May or may not be relevant to an investigation or response.

SIEM Capabilities:
Aggregation - Massive gathering of logs into a central repository.
Normalization - Events/logs eliminate duplicates and helps clean up the data into the same format. Eliminates redundancy to allow easy analyzation for suspicious activity.
Correlation - Lines up events to determine the problem.
Secure Storage - Keeps a copy of all logged events in a secure repository that is only read-only to prevent tampering or deletion.
Analysis and reporting refers to SIEM system rules. SIEMs should have relevant logs based on organizational risks, budget, and regulations.

UEBA - User and entity Behavioral Analysis - Engines within SIEM solutions that focuses on the analysis of user and entity behavior. Based on machine learning to create a baseline of usual behavior.

Failure models

Fail-soft (Fail-open) Fails into a state of less security. Example: A firewall fails and allows all traffic
Fail-secure (Fail-closed) Falls into a state of the same or greater security. Blocking all traffic if it fails.
Fail-safe - Fails into a state that prioritizes the safety of people. Doors and fire alarms.


Type	Data backed Up.	Backup Time	Restore Time	Storage
Mirror	Exact copy with no compression.	Fastest	Fastest	High
Full	ALL DATA.	Slowest	Fast	High
Differential	Full and then changes since the last full backup.	Moderate	Moderate	Moderate
Incremental	Full and then changes since last backup.	Fast	Slow	Lowest

Archive bit - 0 means no backup is required, 1 means a backup is required.

CRC - Math used to ensure the integrity of data. Used to validate data. Used to also detect accidental changes to data at rest or in motion.

RAID	Data Redundancy	Read/Write Performance	Min. # of Drives	Extra info
0 Striping	No	Highest	2	All about increasing read/write performance. No data resiliency
1 Mirroring	Yes	Moderate	2	Great Data resiliency. No performance improvement.
1+0 Striping + Mirroring	Yes	Highest	4	Performance and resiliency. Requires more hard drives.
5 Parity Protection	High	High	3	Good balance of performance and resiliency. Requires less hard drives than RAID 10.

BCM - The business function and processes that provide the structure, policies, procedures, and systems to enable the creation and maintenance of BCP and DRP plans.
BCP - Focuses on the survival of the business and the capability for an effective response; strategic.
DRP - Focuses on the recovery of vital technology infrastructure and systems; tactical.

MTD/MAD	Maximum amount of time that an organization's critical processes can be impacted. RTO should never exceed the MTD.
RTO	Amount of time expected to restore services or operations to a defined service level.
RPO	Maximum amount of data that can be lost in terms of time.
WRT	Time needed to verify the integrity of systems and data as they are being brought back online.

Order goes from RPO, RTO, MTD, WRT.

Read-through test - Easiest test. Ensures that major components of the DRP is included.
Walkthrough test - All key stakeholders convene in a conference room and walk through the plan. Everyone walks through the process.
Simulation test - All key stakeholders convene plus a moderator.

Parallel test - Scenario is responded to with people located where they would be during an actual situation. People work with systems parallel to production systems.
Full-interruption or full-scale test - Backup, production, or primary systems are used to respond to the situation. It's a full-scale test. Production is impacted.

Three goals of BCM
Safety of people, minimization of damage, and survival of the business.

CMM Stages
Initial - Marked by new or unrefined processes that might be considered reactive or chaotic.
Repeatable - Ability to consistently repeat certain processes for projects.
Defined - Well-defined and well-documented processes. It's a shift from a reactive approach to a planned proactive approach.
Managed - Use of meaningful metrics is incorporated for better process management and improvement.
Optimized - Processes are continually improved using tools

Canary testing - Hyper focused testing of new application code/features by pushing out the changes to a small subset of users versus pushing out to all users.
Smoke testing - Focuses on quick preliminary testing after a change is made to identify any simple failures or the most important existing functionality that worked before the change was made.

Assembler - Read programs and convert  low-level assembly language into machine language.
Compiler - Reads programs and converts high-level language into machine language.
Interpreter - Converts high-level language one line at a time into machine language at runtime.

CI - Development mindset and set of practices that frequently pursues small code changes and updates to code libraries.
CD - Delivers applications to production, user review, and testing environments. Used to test code changes quickly.
Cdep - Ensures that tested and accepted code is deployed to production.

Polymorphism code - Code that can change based upon requirements.
Polyinstantiation - Something being instantiated into multiple separate or independent instances.

Types of obfuscation 
Lexical obfuscation - Modifies the look of the code. (Removing comments, debugging information, and changing the format.
Data obfuscation - Modifies the data structure.
Control Flow obfuscation - Modifies the flow of control through the code. (reordering statements, methods, loops, etc.

Primary Key -One or more columns whose values uniquely identify a row within a relational database.
Foreign key - One or more columns whose values in a table refer to the primary key in another table.

Concurrency - The ability for multiple processes to access or change shared data at the same time.
Locks - Prevents data corruption when multiple users try to write to the database simultaneously.

ACID - Relates to how information and transactions in an RDBMS environment should be treated.
Atomicity - All changes take effect or none at all.
Consistency - Consistent with all rules.
Isolation - Transactions are invisible to other users until complete
Durability - Completed changes will not be lost.

Buffer overflow - A common problem with applications. When information is sent to a storage buffer that exceeds the capacity of the buffer. Could lead to elevat3ed privileges and could launch malicious code.
ASLR - Protects against buffer overflows. It randomizes the locations of where system executables are loaded into memory. Prevents users from learning how a program operates.
Bounds Checking - Input to a variable is checked to ensure it is within the same bounds.

API - Provides a way for applications to communicate with each other. APIs are translators
REST - More flexible and lighter weight than SOAP. HTTP based, fast, outputs in CSV, JSON, RSS, and XML.
SOAP - Older, more rigid and standardized, XML-based. Strong error handling.

Coupling - Level of relatedness between units of a code base. Low coupling is better than high coupling.
Cohesion - Code that makes up a unit of software. High Cohesion is better than low cohesion.

Between-the-lines attack: Where an attacker intercepts or modifies communication between devices/people communication over a network. Man-in-the-middle
Memory reuse (object reuse) - Where remnants of data that relate to a previous operation are accidently or intentionally read, used, or otherwise disclosed. Residual data should be cleared from the memory




CISSP Boson Study

ISO 27001 - Focuses on security governance. Directing and controlling IT security. Defines a standard for creating an ISMS to provide governance for IT security.
ISO 27002 - Focuses on security controls. Security Policy, Organization of Information Security, HR security, Asset Management, Access control, cryptography, etc.
ISO 17799 - Transformed into ISO 27002.
COBIT - IT management framework created by ISACA and ITGI. Focuses on Planning and organization, Acquisition and implementation, Delivery and support, Monitoring and evaluation.

NIST 800-30 - Assessing risk
NIST 800-37 - Risk Management Framework
NIST 800-66 Used for HIPPA
CCTA Risk Analysis and Management Method (CRAMM) - Establishes a three-stage approach to risk evaluation that analyzes technical as well as nontechnical security aspects.
Facilitated Risk Analysis (FRAP0 - A low-cost method of evaluating risk for on system or process at a time.
Security Officers Management and Analysis Project (SOMAP) - An open-source method of evaluating and managing risk.
Spanning Tree Analysis - Trees of all possible threats that do not apply to an asset
Value at Risk (VAR) - Identifies a profile of acceptable risk for a company in order to determine the most cost-effective risk mitigation method.

Double encoding - Used to bypass a web application's existing directory traversal security check. HTTP is submitted to the web server for directory traversal attacks. ../ to %2F.
Forced browsing - Attacker searches for unliked content on a web server. Can be used to access content that should not be available to the attacker. Used to also look for unlinked directories within URLs. 

802.11n - 600 Mbps with MIMO support. Can use 2.5 and 5.0 GHz Frequency ranges
802.11b - 11 Mbps and DSSS with 2.4 GHz 
802.11g - Uses 54 Mbps and OFDM with 2.4 GHz
802.11a - Uses 54 Mbps a 2.4 GHz

Ring Model with Privileges 
0 - Kernel
1 - OS components 
2 - Device drivers
3 - Users

MAC - Model that uses security levels of resources and users to grant access to resources. Government levels like, 'Secret' 'Top Secret'.

Swapping - Memory protection technique that copies an entire process to a disk. Information in a process is moved from primary memory to secondary memory, such as a hard drive. Processes are moved to a secondary memory node.
Paging - Memory protection technique that copies a fixed-length block of memory to a disk.
Write Once Read Many (WORM) storage - Process of writing data to a medium that can never be written to again. Data can be retrieved from the medium an infinite number of times. Puts it into a CD-R format that can never be erased or rewritten.

Keyboard-interactive - SSH authentication method that works by prompting a user for answers to a series of questions.

Security administrator - Responsible for user account management and reviews of audit data in a client/server architecture. 
System administrator - Monitors and maintains the systems and applications in a distribute computing environment.
System operator - Found in mainframe environments as well as thin-client systems in a distributed computing environment. 
Power user - a role that is typically found in a distributed computing environment. Heightened-privilege account that enables a user to perform some tasks that typically users cannot perform on their own.

Oauth 2.0 - Open standard used for authorization frameworks that provides a third-party application with delegated access to resources without providing the owner's credentials to the application.
XACML - XML-based open standard developed by OASI. Used to define access control policies. Used commonly for SDN systems.
SAML - Open standard developed by OASIS. Used to exchange authentication and authorization information. Enables a user to gain access to multiple independent systems on the Internet after being authenticated. 
SPML - XML-based open standard used for SSO. Used for LDAP information in XML format.

Dilution - When an entity uses a trademarked term as a generic term.
Cybersquatting - Intellectual property attack that focuses on infringement of a trademark. An entity registers an Internet domain name that infringes on a different entity's trademark.
Typo squatting - Occurs when an entity registers an Internet domain name that is a common misspelling or is closely related to the trademark.

Incident Response Phases:
DRMRRL
Detection - Looking through logs or analyzing network traffic.
Response - Activating the incident response team.
Mitigation - Containing the incident to prevent further damage.
Reporting - Documenting the security incident so that management and law enforcement can be informed.
Recovery - Returning the system to the production environment.
Remediation - Process of understanding the cause of the security breach.
Lessons Learned  - Process of reviewing the incident to determine improvements for future incidents. 

Routers are used to create multiple broadcast domains on your company's network
Bridges are used to create separate collision domains.

Brute-force attacks typically only have the ciphertext.

NAC can quarantine a host that does not comply with a security policy. Prevents hosts form accessing the network if they do not comply with requirements.

SDN - Intelligent network architecture in which a software controller assumes the control plane functionality for all network devices. 
Data plane - Network infrastructure devices. Encapsulation and decapsulation of packets happen on this plane.
Management plane - Telnet, SSH, SNMP, Syslog works on this level. Enables an admin to connect to and manage a network device.
Control plane - Responsible for network decision-making in a controller-based network and a traditional network
Application plane - Consists of SDN applications.

OSPF - Link-state routing protocol that learns the entire network topology of an area.
RIP - distance-vector routing protocol

Five rules of evidences - Be authentic, Be accurate, Be complete, Be convincing, Be admissible.

Directive - Define appropriate use and behavior within an organization.
Deterrent - Dissuade attacks.
Preventive - Stops and prevents - IPS.
Compensating - Supplements controls.
Detective - Monitor or send alerts.
Corrective - Repair damage.
Recovery - Restore a system.

Mutual authentication - A host offers proof of identity to each other. Kerberos. Can prevent a client from divulging information to a rogue server.
FIM - Process of providing access to a company's data resources to organizations or parties that are not owned by the company.

Risk Acceptance - Occurs when a company or group chooses to leave an asset unprotected rather than undergo the time and expense to protect an asset.
Risk Avoidance -  eliminates the use of a technology or a service altogether rather than deal with the risks.

Incremental - Only backs up files that have modified since the last full or incremental backup.
Differential - Only backs up files that have been modified or created since the last full or incremental backup.

Dual stacks enable a host to communicate with both IPv4 and IPv6 hosts.

Collision domain - A network segment where collisions can occur when frames are sent among the devices on that network segment.
Broadcast domain -  Network segment where all devices receive a copy of a broadcast sent out by a device within the network.

VLANs create separate broadcast domains.

Coupling - An OOP term that is used to describe the level of an object's dependence on other objects.
Cohesion - An OOP term used to describe the level of an object's independence on other objects.

DRP Methods:

Read-through - DRP documents are disturbed only
Structured walk-through test - Table-top exercise. Gathers around a table to role-play.
Simulation test - Asked to develop a response to a given disaster. Tested against a simulated disaster.
Parallel test - Employees are relocated to the DRP's recovery location. 
Full-interruption test - Employees are relocated and processes fully shutdown.

CC ST - A documentation for a system or product that is to be tested.
EAL are ratings for products that have been tested.

Least privilege - Requires a user have no more access to a resource than what is required to do that user's job.
Compartmentalization - Isolates groups of users from other groups of users based on the information or access required by the groups.
Need to know - A principle that requires that a user have no access to information that is not required by the user.

WS-SecureConversation Web Services are used to create security contexts for faster message exchanges. 

Four security modes for systems that process classified information:
System high mode - Users must have a security clearance and access approval
Dedicated mode - Users must have a security clearance, access approval, and a valid need to know.
Compartmented mode, Users must have a security clearance for all information processed by the system. They also need a need to know.
Multilevel Mode - Secret clearance, access approval, and a valid need to know. 

Prevention obfuscation is used to make programs obscure to computers

DRP - Used to restore specific IT services so that a company can recover from a disaster quickly.
BCP - Procedures that should be performed in the event of a disaster. Establish the order in which procedures should be implemented.
MTD - Used to prioritize the recovery of assets in a BCP or DRP.
BIA - Used to identify the business systems and processes that are critical for a company to continue to operate.

Remote journaling - Sending database transaction logs to a remote 
Database shadowing - Requires two or more databases that are running simultaneously.
Electronic vaulting - Transmitting bulk data to an offsite backup storage facility.
Active-active clustering - Load balancing with multiple systems running in parallel.

Overt channel - Transmission or other communication that is authorized and is performed in compliance with security policies.
Covert timing channel - Sequences off  a specific time for communication.
Covert storage channel - A memory space or storage

Emanation - Access control vulnerabilities that could result in the theft of information by capturing and analyzing the electromagnetic leakage of electronic devices.

KDC - Enables SSO services by acting as a trusted third-party authentication server within a Kerberos Network.

Mutual Assistance Agreement - backup-site agreement or reciprocal agreement. It is a legal arrangement between two organizations in which the parties agree to aid one another by providing space and network resources in the event that a disaster renders one of the parties incapable of functioning.

Noninterference Security Model - Used to avoid covert channel attacks.

Chinese Wall/Brewer-Nash model - Used to mitigate conflicts of interest.
Take-Grant - Uses a directed graph as an access control model. 
Clark-Wilson - Subjects use programs to access objects. Used for integrity breaches and separation of duties.

ARO * SLE = ALE

ESP is used with L2TP to provide confidentiality.

BIA - Identifies business systems and processes that are critical for a company to continue to operate.
BCP development process:
Develop a BCP policy statement
Conduct a BIA
Identify preventive controls
Develop recovery strategies
Develop an IT contingency plan
Perform DRP training and testing
Perform BCP/DRP maintenance

OpenID Connect - Open-standard method for decentralized authentication that is maintained by the OpenID Foundation.  Constructed around Oauth 2.0. 
OpenID - An open-standard method for decentralized authentication.
Oauth 2.0 - Provides third-party application access.

ARP addresses resolve IP addresses to MAC addresses

Defect Density - A metric that determines the average number of defects per LoC.
Risk Density - A metric that ranks security issues in order to quantify risk.
Function point - Metric that estimates the size of an application by the number of LoCs that perform a specific function.
LoC - Metric that estimates the size of an application by the number of executable lines of source code.

License - A contract between a software provider and a consumer.
Trademark - Intellectual property that protects slogans and logos.
Trade secret - Intellectual property that protects confidential information about how a product is created.
Copyright - Intellectual property that protects things like art, music, literature, or source code.

Pharming - DNS cache poisoning attacks that attempt to modify a DNS cache by providing invalid information to a DNS server.
Teardrop - DoS attack that sends several large overlapping IP fragments to a target.

MTD is the maximum tolerable downtime. It is the sum of the RTO and WRT. The maximum amount of time that a business can survive without a particular service.

Due Diligence - Legal liability concept that requires an organization to continually review its practices to ensure that protection requirements are met.
Due Care - Defines the minimum level of information protection that a business must achieve. Means by which an entity can ensure that its business practices are practices are reasonable for individuals. Due Care is the exercising of reasonable security measures to protect assets.

Lipner combines both Bell-LaPadula, confidentiality & Biba, integrity.
Graham-Denning - Uses an access control matrix to map subjects and objects to rules.

TCSEC - Orange book

Fault analysis attack - A side-channel attack that works by denying a smartcard enough power to operate correctly. Passive-attacks.

Multiple processing is when multiple CPUs share the processing load of a single system.




CISSCP Exam Cram

Domain 1:

Due Diligence - Practicing the activities that maintain the due care effort. Includes Research, Planning, and Evaluation Before the decision. Increases understanding and reduces risk. Do Detect.
     Ex: Laws and Regulations, Industry standards, Best practices.
Due Care - Doing what a reasonable person would do in a given situation. It is sometimes called the "prudent man" rule. Includes Implementation, operation, and reasonable measures After the decision. Do Correct
     Ex: Reporting security incidents, Security awareness training, Disabling access in a timely way.
Together, these will reduce senior management's culpability and downstream liability when a loss occurs.

Protect society, Act honorably, provide service, advance and protect the profession.

AUP - Assign roles and responsibilities.
Security Baseline - minimum levels.
Security Guidelines - Offer recommendations.
Procedures - Detailed step-by-step.

Strategic - Long term, stable plan that includes a risk assessment. 5-yr horizon.
Tactical - Midterm plan to provide more details on goals of the strategic plan. 1 year.
Operational - Short-term, highly detailed plan based on the strategic and tactical plans. Monthly, quarterly.

Risk Acceptance - Do nothing and accept the risk and the potential loss.
Risk Avoidance - When costs of mitigating or accepting are higher than the benefits of the service. Removing the technology use.
Risk Mitigation - Implementing countermeasures and accepting residual risks.
Risk Transfer - Assign risk to a 3rd party. Insurance.

RMF NIST 800-37
PCSIAAM
People, Can, See, I, Am, Always, Monitoring
	1. Prepare to execute the RMF
	2. Categorize Information Systems
	3. Select security controls
	4. Implement security controls
	5. Assess security controls
	6. Authorize the system
	7. Monitor security controls

Residual Risk - The risk management has chosen to accept the risk rather than mitigate. AFTER
Inherent Risk - The amount of risk that exists in the absence of controls. BEFORE
Total Risk - The amount of risk an organization would face if no safeguards were implemented. WITHOUT

Risk Formula - Risk = Threat * Vulnerability
Total Risk Formula - Threats * Vulnerabilities * asset value = Total Risk

Risk Analysis Steps 
	1. Inventory assets - Assign a value to an asset. AV
	2. Identify threats - Research each asset and produce a list of all possible threats. Calculate EF and SLE 
	3. Perform a threat analysis - Calculate the likelihood of each threat. ARO
	4. Estimate the potential loss - Calculate the ALE
	5. Research countermeasures to each threat. Calculate changes to the ARO and ALE based on countermeasures.
	6. Perform a cost/benefit analysis for each countermeasure for each threat of an asset.

Delphi Technique - An anonymous feedback-and-response process used to arrive at a consensus. Used for Qualitative assessments.
	
Quantitively formulas and definition:

EF - Percentage of loss that an organization would experience if a specific asset were violated by a realized risk. EF of 30% or .3 per year.
SLE - Represents the cost associated with a single realized risk against a specific asset. AV * EF. $100,000 * .3 = $30,000.0 
ARO - The expected frequency with a specific threat or risk will occur within a single year. 
ALE - The possible yearly cost of all instances of a specific realized threat against a specific asset. (AV * EF = SLE) (SLE * ARO = ALE).
Safeguard evaluation - Used to value how cost effective a safeguard is. Good security controls mitigate risk, are transparent to users, difficult to bypass, and are cost effective. ALE Before safeguard - ALE After safeguard  - Actual Cost = value of safeguard.

Controls Gap - The amount of risk reduced by implementing safeguards. Total risk - controls gap = residual risk.

Threat Modeling - Can be proactive or reactive, but in either case, the goal is to eliminate or reduce threats. Assets, Attackers, & Software.

Stride - Microsoft's Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of privilege. Attackers
PASTA - Focuses on Asset value of Threat Modeling.
VAST - Based on a PM principles - Visual, Agile, Simple, Threat. Integrate threat management into an Agile programming environment. 
DREAD - Damage potential, Reproducibility, Exploitability, Affected users, Discoverability.
TRIKE - Focused on acceptable risk - An open-source threat modeling process that implements a requirements model.
COBIT - Security control framework. IT management and governance framework. Meet stakeholder needs, Cover the enterprise end-to-end, Apply a single, integrated framework, Enable a holistic approach, separate governance from management. 


Security Frameworks

ISO 27001 - Information Security management system governance.
ISO 27002 - Security Controls.
COBIT - Framework for documentation of IT Security. 
ITIL - Servers business functions like service management.

NIST 800-53 - Security controls within the federal government.
NIST 800-57 Risk management framework.

Reduction Analysis - Trust boundaries - Any location where the level of trust or security changes.
Data flow paths, the movement of data between locations.
Input Points - locations where external input is received.
Privileged Operations - Any activity that requires greater privileges than of a standard user account.
Details about Security Stance and Approach - Declaration of security policy, security foundations, and security assumptions.

Security controls
Safeguards are proactive.
Countermeasures are reactive. 

Control Types
Deterrent - Deployed to discourage violation of security policies
Preventative - Deployed to thwart or stop unwanted or unauthorized activity from occurring.
Detective - Deployed to discover or detect unwanted or unauthorized activity.
Compensating - Provides options to other existing controls to aid in enforcement of security policies. Sandboxes
Corrective - Modifies the environment to return systems to normal after an unwanted or unauthorized activity has occurred. Anti-Virus software
Recovery - An extension of corrective controls but have more advanced or complex abilities.
Directive - Direct, confine, or control the actions of subjects to force or encourage compliance with security policies.

Types of law
Criminal - Standard illegal things like murder, assault, robbery, and arson.
Civil Law - Contract disputes, real estate transactions, employment, estate, and probate.
Administrative Law - Government agencies and regulations.

Laws
Computer Fraud and Abuse Act (CFAA) - First major US cybercrime-specific legislation
Federal Sentencing Guidelines - Provided punishment guidelines to help federal judges interpret computer criminal laws.
FISMA - Required a formal infosec operations for the federal government.
DMCA - Covers literary, musical, and dramatic works.

IP and Licensing
Trademarks - Covers words, slogans, and logos used for a company
Patents - Protects intellectual property rights of inventors.
Trade Secrets - Critical intellectual property that pertains to businesses.
Licensing - contractual, shrink-wrap, click-through, and cloud services.

Computer export controls - Can't export to Cuba, Iran, Iraq, North Korea, Sudan, and Syria
Privacy (US) - Fourth Amendment
Privacy (EU) GDPR

HIPPA (Health Information)
HITECH (Health Information Technology for Economic and Clinical Health)
GLBA (Financial institutions)
COPPA (Children's Online Privacy)
ECPA (Electronic Communications)
CALEA (Law Enforcement of communications) 

BCP
BCP - The overall organization plan for "how-to" continue business.
DRP - The plan for recovering from a disaster impacting IT and returning the IT infrastructure to operation.

BCP vs. DRP
BCP - Focuses on the whole business
DRP - Focuses on technical aspects.

COOP - The plan for continuing to do business until the IT infrastructure can be restored.

Review:

NCA - An agreement that binds a current or former employee, contractor or consultant from competing with an employer. Includes details such as: expiration date, geographic restriction, and job descriptions.

Risk Management - Determining the cost-effectiveness of mitigating the potential harm or loss to a company.
Risk Assessment - The risk-evaluation process used to determine the amount of risk a decision involves. Evaluating an asset to ascertain the amount of vulnerability it represents to a company.
Risk = Threat * Vulnerability. A potential harmful incident
Vulnerability - A weakness in a system.
Total Risk = Threat * Vulnerability * AV

Cybersquatting - Attack that focuses on infringement of a trademark. When an entity registers as an Internet domain name that infringes on a different entity's trademark.

AV
SLE = AV * EF
ARO 
ALE = SLE * ARO

Risk Acceptance - Occurs when a company chooses to leave an asset unprotected rather than undergo the time and expense to protect the asset.

EU-U.S. Privacy Shield Framework - Created by the U.S. Department of Commerce and European Commission to enable companies in the United States to process information of individuals in the EU member nations.
OECD - Provides a framework for how information traverses international borders.
U.S. Privacy Act - Used to govern the way federal agencies use and distribute the personal information of U.S. citizens.
PIPEDA - Canadian law used to govern how private organizations can collect, use, and disclose personal information. 

Opt-in agreement - An information sharing agreement that prevents an entity from sharing a user's information by default. Requires an organization to obtain permission to share PII data with third parties.
Opt-out agreement - Information sharing agreement that requires a user to act in order to prevent an entity from sharing that user's information. 
EULA - Software license. Specifies what users are and are not allowed to do with software.

Prudent Man Rule - A business practice that a reasonable individual would consider appropriate.

Mandatory - Polices, procedures, standards

Guidelines and baselines are discretionary.

Compensating access control are used to supplement directive access control such as company policies.

Due Care - Which means when a company did all that it could have reasonable done to try and prevent security breach / compromise / disaster, and took the necessary steps required as countermeasures / controls (safeguards)
Due Diligence - Means that the company properly investigated all its possible weaknesses and vulnerabilities AKA understanding the threats.

Risk Avoidance - Discontinue activity because you don't want to accept the risk.
Risk Transfer - Passing on the risk to another entity.
Risk Mitigation - Elimination or decrease in level of risk.
Risk Acceptance - Live with it and pay the cost.



Domain 2:

Data Life Cycle 
Creation 
Classification 
Storage 
Usage 
Archive 
Destroy 

Government Levels
Unclassified, Confidential, Secret, Top Secret

Non-gov't Levels
Public, Sensitive, Private, Confidential/Proprietary

Data Owner - Usually a member of a senior management. Can delegate some day-to-day duties. Cannot delegate total responsibility. Sets data classification levels.
Data Custodian - Someone in the IT department. Does not decide what controls are needed. Day-to-day duties. Operations.
Data Administrator - Responsible for granting appropriate access to personnel
User - Any person who accesses data via a computing system to accomplish work tasks.
Business/Mission Owners - Can overlap with the responsibilities of the system owner or be the same role.
Asset Owners - Owns asset or system that processes sensitive data associated with security plans.

GDPR
Data Processor - A natural or legal person, public authority, agency, or other body, which processes personal data solely on behalf of the data controller.
Data Controller - The person or entity that controls processing of the data.
Data Transfer - GDPR restricts data transfers to countries outside of the EU.

Anonymization - The process of removing all relevant data so that it is impossible to identify the original subject or person.
Pseudonymization - The process of using pseudonyms (aliases) to represent other data.

Review:

Forced browsing - Attack technique that is used when an attacker is searching for unlinked content on a web server. A brute-force attack and can be used to access content that should not otherwise be available to the attacker. Modifying a URL.
XSS - Involves the execution of malicious web scripting code in a trusted context.
XSRV - Takes advantage of a software vulnerability and involves the redirection of static content within a trusted site. CAPTCHAs prevent CSRF. Revalidating the authenticity

Four common Vs of Big Data
Volume - Scale of Data
Velocity - Analysis of Streaming Data
Variety - Different forms of data
Variability  

Security marking reflects applicable laws, directives, policies, regulations, and standards. They enable organizational process-based enforcement of security policies. It is the human-readable security attributes.
Security labeling - Refers to the use of security attributes for internal data structures within information systems.

Tokenization - Replaces original sensitive data with non-sensitive data in a database.

Information policy - Classifications and defines level of access and method to store and transmit information.
Security policies - authenticates and defines technology used to control information access and distribution.
System security policy - lists hardware / software to be used and steps to undertake to protect infrastructure.

Standards

NIST 800-14 NIST SP - GAPP for securing information technology systems
NIST 800-18 NIST - How to develop security plans.
NIST 800-27 NIST SP - Baseline for achieving security, five lifecycle planning phases: Initiation, Development, Implementation, Operation, Disposal.
NIST 800-88 Guidelines for sanitation and disposition, prevents data remanence.
NIST 800-122 - NIST SP - Defines PII as any information that can be traced back to identify a person.
NIST 800-137 - Build/implement info security continuous monitoring program: define, establish, implement, analyze and report.
NIST 800-145 - Cloud computing

FIPS - Federal Information Processing Standards - Relates to standards and guidelines adopted under FISMA.
FIPS 199 - Standards for categorizing information and information systems.
FIPS 200 - Minimum security requirements for Federal information and information systems.
DOD 8510.01 - Established DIACAP
ISO 15288 - International systems engineering standard covering processes and life cycle stages.



Domain 3:

Secure Defaults - Default configuration reflects a restrictive and conservative enforcement of security policy.
Fail Securely - Indicates that components should fail in a state that denies rather than grants access.
Trust but verify - Depended on an initial authentication process to gain access to the internal "secured" environment then relied on generic access control methods.

Privacy by Design.
Proactive and not a reactive approach.
Privacy as the Default setting.
Privacy must be embedded in the design.
Privacy should be a positive-sum approach and not a zero-sum approach.
End to end full lifecycle data protection.
Visibility and transparency.
Keep privacy user-centric.

Keep it Simple - Complexity is not needed. Best-in-suite over best-in-breed solutions. Allows for organizations to move forward incrementally as well as have easy configuration. 

SOA - A creation of discrete services that may be accessed by users in a black box fashion.
Microservices - Fine-grained services with a discrete function. A modern adaptation of SOA to cloud computing.

Containerization - A lightweight, granular, and portable way to package applications for multiple platforms. Reduces overhead of server virtualization by enabling containerized apps to run on a shared OS kernel.

APIs - A set of exposed interfaces that allow programmatic interaction between services and applications.

REST uses the HTTPS protocol for web communications to offer API end points.

Grid computing - Employs a centralized controller that makes computing assignments to grid members.

Edge Computing - Compute operations that require processing activities to occur locally, far from the cloud. Common in IoT, agricultural, science/space, military
Fog computing - Places gateway devices in the field to collect and correlate data centrally at the edge.

CASB - A security policy enforcement solution that may be installed on-premises or in the cloud.

Algorithms that are quantum resistant is Lattice.

Cryptography

Provides Confidentiality, Integrity, and Nonrepudiation.
Stream - One bit at a time
Block - Groups at a time

Substitution - Replaces each character with a different character.
Transposition - Rearranges the letters.

IV - A random bit string that is Xored with the message, reducing predictability and repeatability.

Zero-knowledge proof - A communication concept. A specific type of information is exchanged, but no real data is transferred. Used with digital signatures and digital certificates. Enables one to prove knowledge of a factor to another person without revealing the fact.

Split knowledge - Means that the information or privilege required to perform an operation is divided among multiple users. Ensures that no single user has sufficient privileges to compromise the security environment.

DES and 3DES Modes

ECB - Simplest & least secure mode. Same encrypted block is produced.
CBC - Each block of text is XORed with the block of ciphertext.
CFB - Streaming version of CBC. Uses memory buffers of the same block size. Uses chaining which generates errors.
OFB - XORs the plain text with a seed value. No chaining function.
CTR - Uses an incrementing counter instead of a seed. 

Asymmetric
Data 
To encrypt a message, use the recipient's public key.
To decrypt a message, use your own private key.

Digital Signature 
To sign a message, use your own private key. (Non-Repudiation)
To validate a signature, use the sender's public key

Meet-in-the-middle attack - Exploits protocols that use two rounds of encryption.
Man-in-the-middle attack - fools both parties into communicating with the attacker instead of directly with each other.

RSA uses prime numbers
El Gamal uses modular arithmetic
EC uses discrete logarithm problems and provides more security.

Security Models

Determines how security will be implemented, what subjects can access the system, and what objects they will have access to.

Has three properties.
Simple Security property for read
Star * for write
Invocation property for calls.

State Machine Model - Describes a system that is always secure no matter what state it is in. Based on FSM. It is a snapshot of a system. If the state transition results in another secure state, it is a secure state machine.
Information Flow Model - Based on how information flows. Biba and Bell-LaPadula are Information flow models.
Non-Interference Model - Concerned with how actions of a subject at a higher security level affect the system state or the actions of a subject at a lower security level.  Makes sure subjects aren't seen by and don't interfere with other objects and subjects on the same system.
Lattice-Based Model - Based on the interaction between any combination of objects (resources, computers, and applications) and subjects (individuals, groups or organizations.)
 
Svannah, Lokesh. Run the readiness check.

Bell-LaPadula - Prevents information flow from a high security level to a low security level.
Biba - Focuses on flow from low to high security level.

Integrity Models
Biba - No read down, no write up
Clark-Wilson - Access control triple. Uses security labels to grant access to objects. Relationship between authenticated principal (user) set of programs (TPs) and data items (UDIs and CDIs)
Goguen-Meseguer - Noninterference model
Sutherland - Prevents interference

Confidentiality Models 
Bell-LaPadula - No read up, no write down. DoD. Uses MAC to enforce security policies. No Read Up, No Write Down. No running Under Nets With Dingos.
Brewer and Nash - Chinese Wall. Prevents conflicts of interest problems.
Take Grant - Directed graph. Take, Grant, Create, and Revoke.

Integrity & Confidentiality
Graham-Denning - Formal set of protection rules for which each object has an owner and a controller. Secure creation and deletion of both subjects and objects
     Has eight rules: Securely create an object, create a subject, delete and object, delete a subject, provide read access rights, grant, delete, and transfer.

Security Modes

Dedicated Mode - Security clearance that permits access to All info processed by system, approval for ALL info processed by system, valid need-to-know for ALL info processed by system.\

Multilevel Mode - Can process information at different levels even when all system users do not have the required security clearance to access all information processed by the system.

System High Mode - Each user must have valid security clearance, access approval for ALL info processed by system, and a valid need-to-know for at least SOME info on the system. Offers the most granular control.

Compartmented Mode - Further than System High Mode. Each user has to have a valid security clearance, access approval for ALL INFO processed by system, but requires valid need-to-know for ALL INFO they have access to on a system.



Trusted Computing Base - A combination of hardware, software and controls that work together to form a "trusted base" to enforce your security policy.

Security perimeter - An imaginary boundary that separates TCB from the rest of the system. Creates secure paths to communicate with the rest of the system.

Reference Monitor - Enforces access control. Logical part of TCB that confirms whether a subject has the right to use a resource prior to granting access.
Security Kernel - Implements access control. Collection of TCB components that implement the functionality of the reference monitor.

Criteria

Common criteria (ISO-IEC 15408) - Enables an objective evaluation to validate that a particular product or system satisfies a defined set of security requirements.
     cPP - Black box
     EAL - White box

Trusted Computer System Evaluation Criteria) - A structured set of criteria for evaluating computer security within products and systems.
ITSEC - Represents and initial attempt to create security evaluation criteria in Europe.

CC Level	Description
EAL0, EAL1	Functionally Tested
EAL2	Structurally Tested
EAL3	Methodically Tested & Checked
EAL4	Methodically Designed, Tested, and Reviewed
EAL5	Semi-Formally Designed and tested
EAL6	Semi-Formally Verified Design and Tested
EAL7	Formally Verified Design and Tested


TCSEC	ITSEC	CC Level	Description
D	F-D+E0	EAL0, EAL1	Minimal/no protection
C1	F-C1+E1	EAL2	Discretionary security mechanisms
C2	F-C2+E2	EAL3	Controlled access protection
B1	F-B1+E3	EAL4	Labeled security protection
B2	F-B2+E4	EAL5	Structured security protection
B3	F-B3+E5	EAL6	Security domains
A1	F-B3+E6	EAL7	Verified security design


Covert Channels - A method that is used to pass information over a path that is not normally used for communication. May not be protected by system's normal security controls.
     Covert timing - Process will relay information by modulating the use of a system resources  based on different timing.
     Covert storage - A process that writes data to a storage location where a process of a lower clearance level is able to read it.

Types of Access Control

MAC - Determined by the system. Relies on classification labels.
DAC - Permits the owner or creator of an object to control and define everything. 
Non-DAC - Enables the enforcement of a system-wide restrictions that override object-specific access control.
Rule-based Access Control - Defines specific functions for access to requested objects. Commonly found in firewall systems.
RBAC - Well-defined collection of named job roles with specific permissions. Groups.

Certification - Technical evaluation of each part of a computer system to assess its concordance with security standards.
Accreditation - The process of formal acceptance of a certified configuration from a designated authority.

Open System - Designed using industry standards and are usually easy to integrate with other open systems.
Closed System - Generally proprietary hardware and/or software. Not normally published and harder to integrate with other systems.

Techniques for ensuring CIA

Confinement - Restricts a process to reading from and writing to certain memory locations.
Bounds - Are limits of memory a process cannot exceed when reading or writing.
Isolation - Is the mode a process runs in when it is confined through the use of memory bounds.

Authentication - The process of proving that you are who you say you are.
Authorization - The act of granting an authenticated party permission to do something. Usually, granting access to resources. 

Multitasking - Simultaneous execution of more than one application on a computer and is managed by the operating system.
Multithreading - Permits multiple concurrent tasks to be performed within a single process.
Multiprocessing - The use of more than one processor to increase computing power.
Multiprogramming - Similar to multitasking but takes place on mainframe systems and requires specific programming.

Memory Types

ROM - Burned in at factory.
RAM - Static RAM uses flip-flops, DRAM uses capacitors
PROM - Programmable ROM.

EPROM - Erasing, Clearing (overwriting w/ unclassified data).
     Ultraviolet EPROM (UVEPROM) - Chips that have a small window, when illuminated with a special ultraviolet light, erases contents.
     Electronically Erasable PROM (EEPROM) - Uses electric voltages deliverable to the pins of the chip to force erasure.

Flash Memory - Derivative concept from EEPROM. Nonvolatile, can be electronically erased and rewritten.

Primary storage - Is the same as memory
Secondary storage - Consists of HDD, SSD, Must be read into primary memory before the CPU can use that data.
Random access storage - Devices can be read at any point.
Sequential access storage - Devices require scanning through all the data physically stored before the desired location.

Firmware - Software stored on a ROM chip, containing basic instructions needed to start a computer. Also used to provide operating instructions in peripheral devices such as printers.

Process isolation - Ensures that individual processes can access only their own data.
Layering - Creates different realms of security within a process and limits communication between them.
Abstraction - Creates black-box interfaces for programmers to use without requiring knowledge of an algorithms or device's inner workings.
Data hiding - Prevents information from being read form a different security level. Hardware segmentation enforces process isolation with physical controls.

Principle of least privilege - Ensures that only a minimum number of processes are authorized to run in supervisory mode.
Separation of privilege/role separation - Increases the granularity of secure operations.

Functional Order of Security Controls - Deterrence, Denial, Detection, Delay, Determine, Decide

Class	Type	Suppression material
A	Common combustibles	Water, Soda acid
B	Liquids	C02, halon, soda acid
C	Electrical	C02, Halon
D	Metal	Dry powder
K	Kitchen	Wet chemicals

Lights need to be 8ft tall. 2 Feet candle 
Fences 8 feet.

Review:


DRAM uses capacitors to store information. Requires constant refreshing to maintain data integrity. Requires more power to function. More slow and cheaper than SRAM
SRAM uses flip-flops. Contains more hardware storage.

ITIL - Operational framework. Uses IT management procedures. Includes best practices. 
SABSA - Security architecture framework that creates a chain of traceability. Works by deriving its ACM from the analysis of the business security requirements.
Zachman Framework - Formal methodology for organizing enterprise architectural information, such as design documents and specifications. Contains Why, How, What, When, Where
TOGAF - A security architecture framework that was developed by the Open Group in 1990s. Four basic architecture domains: Business, Application, Data, and Technology.

Key escrow - To enable a trusted third party to access sensitive data if the need arises. Typically used when a government or other authoritative body needs to access encrypted data for investigative purposes.
Recovery agent - Used to provide a copy of the encryption key in the event that the original is lost.

ITSEC is influenced by the Orange book
Trusted network Interpretation is the red book.

CVSS - Open standard that helps to indicate the severity of vulnerabilities and to prioritize responses to those vulnerabilities. Has Base Metrics, Temporal Metrics, and Environmental Metrics. 
     The base score affects the Temporal score, and the Temporal score affects the Environmental score.
     Base score - Severity of the vulnerability
     Temporal score - Indicate the urgency of the vulnerability.
     Environmental score - Optional and indicates how much an environment or end-user organization is affected by a vulnerability. 

TCB - Describes all the components of a system that are responsible for system security.
TCSEC - Describes the elements of a system that needs TCB. It is a security evaluation method. Orange book. Defines different types of access controls within a computer system.
ITSEC - Segregates a system's functionality. 
International Common Criteria - International standard that is used to test the security of IT products.

To send data to another host, the receiving host's public key is used when encrypting the data. 

TPM  creates an endorsement key. This is a permanent key when created. Storage root key is created when a user takes ownership of the TPM.

Noninterference model - Used to avoid covert channel attacks. 

Clark-Wilson security model requires that subjects use programs to access objects.

Ethernet frame check sequence (FCS) - It contains a 4-byte cyclic redundancy check (CRC) value.

RSA can be attacked from mathematical attacks, Brute-force attacks, and timing attacks.

Linux system file /etc/shadow contains secure user account information and can be read only by root. Contains: login name, encrypted password, etc.
/etc/passwd Contains user account information in older systems. Note secure.

CVSS - Defines the standard scoring system for vulnerability severity.
CVE - Defines the naming system for describing vulnerabilities.
CCE - Defines the naming system for system configuration problems.
XCCDF - SCAP component that provides a language for specifying security checklists.
CPE - Defines an OS, Application, and device naming system.
OVAL - Defines the language format for security testing procedures.

Domain registrar - A company that is authorized by ICANN to register Internet domain names.

     AND
0011
0101
0001

     XOR
0011
0101
0110

     XNOR
0011
0101
1001

     OR
0011
0101
0111

     NOR
0011
0101
1000

TCB is a term that describes all the components of a system that are responsible for system security. Example: OS kernel that supports programs that configure file ownership and permissions.

Fault - A short period of total power loss. Examples: Short circuits, a downed powerline, etc.
Brownout - A long period of low voltage. 
Sag - A short period of low voltage.
Blackout - A long period of power loss.
Spike - A short period of high voltage.
Surge - A long period of high voltage.

GRE - A tunneling protocol that can be used to encapsulate protocols in packets that will be delivered by a different protocol. Commonly used for IPv6 packets to be encapsulated and transported across an IPv4 only network to a separate IPv6 one.


Access control mechanisms - Most likely to involve a reference monitor. 
Reference monitor - An OS kernel function that determines whether a subject with a specific clearance level can access an object of a different classification level.

Abstraction - Involves the process of hiding the operational complexity of a system from the system's user.

CC PP is a set of security requirements and objects for the type of product to be tested.
ToE - The system or product that is to be tested.
ST - The documentation that describes the ToE and any security requirements.
PP - A set of security requirements and objects for the type of product to be tested.
EAL - A rating level that is assigned to the product after the product has been tested.

RollJam can be used against newer garage door openers. It blocks and steals codes by garage door openers.
OpenSesame - Used against older garage door openers. Uses fix codes that can be easily hacked. Brute-force attack.
KeySweeper - Attack that can sniff and decrypt keystrokes sent from Microsoft wireless keyboards.

Middleware - Software that is used in a distrusted computing environment to allow multiple independent processes to communicate with each other and function in a standardized way.
Mainframe - These are thin-client systems in which all the processing takes place on a single large unit.
Distributed System - A type of computing platform that is the most likely to balance the responsibility for security between a server and its clients. Uses a client/server style architecture in which clients that are connected to a server can also function independently. 

Polyalphabetic ciphers: Vigenère, running-key, cipher disk.
Monoalphabetic cipher: Caesar cipher.

Lockdown enclosure - Used to prevent the theft of computer equipment.

ESP is used with L2TP to provide confidentiality.

01010100
01000011
01010100

Out-of-ban method uses symmetric encryption.

3DES is 112 for effective security.

Chinese Wall security model/Brewer-Nash - Avoids conflicts of interest. 

Clark-Wilson - Integrity. Requires subjects to use programs to access objects. Subjects must be authorized to access the programs. Uses separation of duties to ensure that no single user alone can modify sensitive data.

Pipelining - A method by which a CPU can process more than one instruction per clock cycle.

Take-Grant - Enables subjects to assign rights, such as create and remove to other subjects. Uses a directed graph as an access control model.
Information Flow - Describes how information should or should not be passed from subject to subject within a secure environment. 
Noninterference - Multilevel model that can mitigate covert channel attacks.

ECB - Weakest DES mode. Two identical plaintext fragments in a message will yield the same ciphertext.
CBC - Employs an IV and chaining to destroy ciphertext patterns. Works in block mode. Encrypts messages one block at a time.
CTR - Uses a 64-bit counter for feedback. Can perform multiple encryptions in parallel. Does not propagate errors.
CFB - Employs an IV and a method to destroy ciphertext patterns. Works in stream mode. More vulnerable to the propagation of encryption errors.
OFB - Uses the encryption subkey before it is compared to the plaintext by using OR. 

Code words are used to shorten, hide, or clarify a message.

/etc/passwd - It once contained encrypted user passwords, contains the user's primary group ID, and it contains the user's home directory.

Hub-and-spoke topology requires that all communications pass through a central device. Each device connects to a central device.

Linear cryptanalysis - A known plaintext attack. The process of examining an information system in order to break its encryption.

Side-channel attack - Attempts to break an encryption method by monitoring something external to the algorithm.

Red Book/Trusted Network Interpretation - U.S. DoD standard that describes security evaluation criteria for networked systems.
TSEC/Orange Book - Defines different types of access controls within a computer system.
ITSEC - European set of security evaluation that segregates a system's functionality.
International Common Criteria - Used to describe the evaluation criteria for networked systems. Used to test the security of IT products. Identify and remove known vulnerabilities from a product.

P2PE vs. E2EE
P2PE - Prevents merchants from performing key management. E2EE does not. P2PE encrypts cardholder data as soon as it is swiped.

Swapping - A memory protection technique that copies an entire process to a disk.

SSL - Uses a combination of asymmetric and symmetric key encryption to secure communications between a web server and a client.
IPsec - A suite of protocols used with VPN solutions.

RSA is susceptible to chosen ciphertext attacks.

TSEC - A-D

CYOD - Allows employees to use their own devices to connect to the company network.
COPE - Requires employees to use equipment that is purchased for them but they are also allowed to use for personal use.

Ciphertext-only cryptanalysis technique is most likely to include frequency analysis.

Lattice-based model - Uses a hierarchical model that defines layers of privilege.
Matrix-based model - Access is allowed or denied based on the direct relationship of a subject to an object.
State machine model - Uses arithmetical calculations to determine the state of a system at a given time.

Lipner - combines Bell-LaPadula and Biba

Ciphertext-only - Cryptanalysis happens here. Analyzes an encrypted message only. Attempt to decipher an encrypted message. Frequency analysis happens here as well.
Chosen-ciphertext - Capable of choosing portions of a ciphertext to decrypt.

Known-plaintext - Happens when an analyst has a copy of the same message in both its encrypted format and decrypted format.
Chosen-plaintext - Has access to an encryption technology and can also encrypt messages of the analyst's own choosing.

NFPA fire exposure is 60%

Multiprocessing is when multiple CPUs share the same processing load of a single system.
Multitasking - A CPU switches from one process to another to speed up processing time.
Multithreading - Processes can spawn child processes that are known as threads.
Pipelining - Method by which a CPU can process more than one instruction per clock cycle.

Meet-in-the-middle attack is known as a known plaintext attack. It attempts to extract encryption keys when the plaintext and matching ciphertext are known.

Side-channel - Attacker attempts to break an encryption method by monitoring something external to the algorithm.

Overt channel - A transmission or other communication that is authorized and is performed in compliance with security policies.

Zachman Framework for Enterprise Architecture - A matrix-based methodology that enables the viewing of an architecture from six different perspectives.

Graham-Denning Model - Represents a subject with each row. Each column represents either an object or another subject. Has eight actions or rules that a subject needs to perform based on their rights.

Harrison-Ruzzo-Ullman - Includes a rights integrity protection system that prevents a subject or object from being created if that subject or object already exists in the matrix. Does not allow deletion of a subject.

TOGAF - Security architecture framework that exclusively uses business requirements as a central point of comparison for every phase of deployment. Uses an iterative development process.

SABSA - Creates a chain of traceability through six different perspectives.


State Machine Model - Describes a system that is always secure no matter what state it is in. Always boots into a secure state.
Information Flow Model - Focuses on information flow. Bell-LaPadula and Biba.
Noninterference Model - Concerned with how the actions of a subject at a higher security level affect the system state or the actions of a subject at a lower security level.

Matrix - Provides access rights to subjects for objects.

Composition Theories - How inputs and outputs between multiple systems relate to one another.
Cascading - Input for one system comes from the output of another system.
Feedback - One system provides input to another system, which reciprocates by reversing those roles (so that System A first provides input for System B provides input to System A).
Hookup - One system sends input to another system but also sends input to external entities.

Red = trusted network
Orange = TCSEC evaluation
Brown = trusted facilities management
dcsmmmTan = Audit
Aqua = glossary
Green = Password management

ISO 27001 - Security governance
ISO 27002 - Security controls
COBIT - Prescribes the goals and requirements for security controls to meet business objectives.

Register - Limited amount of onboard memory

 that provide it directly with accessible memory locations such as the ALU.
Stack Memory Segment - Used by processors to communicate instructions and data to each other.
Monolithic Operating System Architecture - All of the code working in kernel mode/system mode in an ad hoc and non-modularized OS.

Confusion - Mixing the key values during repeated rounds of encryption, make the relationship between ciphertext and key as complex as possible.
Diffusion - Mix location of plaintext throughout ciphertext, change of a single bit should drastically change the hash.

Split knowledge - Means that the information or privilege required to perform an operation is divided among multiple users

El Gamal - Works with discrete logarithms based on D-H.

Ciphertext Only - Attacker only sees the ciphertext. 
Known Plaintext - Attacker knows both cipher and plaintext
Chosen Plaintext - Offline attack (attacker prepares list of plaintext) lunch box attack
Chosen Ciphertext - Attacker chooses both the plaintext values and the ciphertext values, cherry picking, feed info and based on what you learned get key.

POODLE - (Padding Oracle on Downgraded Legacy Encryption) - Attack helped force the movement from SSL 3.0 to TLS because it allowed attackers to easily access SSl encrypted messages.

Applets - Code objects that are sent from a server to a client to perform some action. Self-contained miniature programs that execute independently of the server that sent them.
Java applets - Short Java programs transmitted over the Internet to perform operations on a remote system.
ActiveX - Controls are Microsoft's answer to Sun's Java applets.

SMSD - Switched Multimegabit Data Service - A connectionless packet-switching technology. Used to connect multiple LANs to form a MAN or WAN. Used to link remote LANS that communicate infrequently






Domain 4:


LiFi - Uses LED to transmit data.

Zigbee - A short-range wireless PAN technology developed to support automation, machine-to-machine communication, remote control and monitoring of IoT devices. Supports centralized and distributed security models.

CDN -A geographically distributed network of proxy servers and their data centers. 

OSI Layer	Protocols	Common Attacks
Application	SHH, HTTP, FTP, LPD, SMTP, Telnet, TFTP, EDI, POP3, IMAP4, SNMP, NNTP, S-RPC, SET	
Presentation	Encryption. ASCII, TIFF, JPEG, MPEG	
Session	SMD, RPC, NFS, and SQL	Session Hijacking, XSS Attacks
Transport	SPX, SSL, TLC, TCP, and UDP	SYN Flood, Fraggle
Network	ICMP, RIP, OSPF, BGP, IGMP, IP, IPSec, IPX, NAT, and SKIP	Man-In-The-Middle (SMURF attack, Teardrop)
Data Link	ARP, SLIP, PPP, L2F, L2TP, PPTP, FDDI, ISDN	Spoofing (MAC Spoofing, MAC Flooding, VLAN Hopping)
Physical	EIA/TIA-232, EIA/TIA-449, X.21, HSSI, SONET, v.24, v.25, Bluetooth, 802.11 - WiFi, and Ethernet	Sniffing


OSI Layer	Definition	Common Means/Devices
Application	Responsible for converting data into a format that is usable by applications	HTML, HTTP, FTP, NGFW
Presentation	Responsible for converting and representing data in different formats.	ASCII, GIF, JPEG, MPEG
Session	Establishes and terminates connections between applications. 	PPTP, ZIP, SCP, SIP.
Transport	Responsible for error detection and correction, flow control, and sequencing.	TCP, UDP
Network	Responsible for logical addressing and routing on a network	Routers, IP, IPv6, IPX, Layer 3 switches, IPSec
Data Link	Defines how devices communicate over a network	MAC, Ethernet, Frame Relay, Token Ring, L2TP, PPP, CDP, 802.11, switches
Physical	Defines how bits are passed over a medium	Coaxial cable, twisted-pair copper cable, fiber-optic cable, hubs

Physical - Contains the device drivers that tell the protocol how to use the hardware for the transmission and reception of BITS.
Data - Formatting the packet from the Network layer into the proper format for transmission. FRAMES
Network - Adding routing and addressing information (source and destination) to the data. PACKETS
Transport - Managing the integrity of a connection and controlling the session. SEGMENTS or DATAGRAMS
Session - Establishing, maintaining, and terminating communication sessions between two computers.
Presentation - Transforming data received from the Application layer into a format that any system following the model can understand.
Application - Interfacing user applications, network services, or the operating system with the protocol stack.

TCP/IP Stack
Application - Application, Presentation, Session
Transport - Transport
Internet - Network
Link - Data Link, Physical

TCP = Segments
UDP = Datagrams

Analog - Communications occur with a continuous signal that varies in frequency, amplitude, phase, voltage, etc.
Digital - Communications occur through the use of a discontinuous electrical signal and a state change or on-off pulses.

Synchronous - Communications rely on a timing or clocking mechanism based on either an independent clock or a time stamp embedded in the data stream. Can support very high rates of data transfer.
Asynchronous - Communications rely on a stop and start delimiter bit to manage the transmission of data. Good for smaller amounts of data.

Baseband - Can only support a single communication channel.
Broadband - Can support multiple simultaneous signals. Uses frequency modulation to support numerous channels. Good for high throughput rates.

CSMA - Developed to decrease the chances of collisions when two or more stations start sending their signals over the datalink layer. Requires that each station first check the state of the medium before sending.
CSMA/CA - Attempts to avoid collisions by granting only a single permission to communicate at any given time. Wireless networks.
CSMA/CD - Responds to collisions by having each member of the collision domain wait for a short but random period of time before starting the process over. Wired networks.

Token passing - Performs communications using a digital token. Once its transmission is complete, it releases the token to the next system.
Polling - Performs communications using a master-slave configuration. The primary system polls each secondary system in turn whether they have a need to transmit data.

Intranet - A private network that is designed to host the same information services found on the Internet.
Extranet - Cross between Internet & intranet. A section of an organization's network that has been sectioned off to act as an intranet for the private network but also servers information to the public Internet.
DMZ - An extranet for public consumption is typically labeled a DMZ or perimeter network.

Bluejacking - Push unsolicited messages to engage or annoy other nearby Bluetooth users.
BlueSnarffing - Wirelessly connects to a device without the owner's knowledge to download and/or alter phonebooks.
Bluebugging - Grants hackers remote control over the feature and functions of a Bluetooth device.

Fibre Channel - A form of network data storage solution. SAN, NAS, etc.
FCoE - used to encapsulate Fibre Channel communications over Ethernet networks.

iSCSI - Networking storage standard based on IP.

EAP - An authentication framework. Allows for new authentication technologies to be compatible with existing wireless or point-to-point connection technologies.
PEAP - Encapsulates EAP methods within a TLS tunnel the provides authentication and potentially encryption.
LEAP - Cisco proprietary alternative to TKIP for WPA. 

Antenna Types

Loop - Reaches multiple frequencies and is more commonly used for TV and RFID systems. Omnidirectional if horizontally mounted.
Monopole - An omnidirectional antenna that can send and receive signals in all directions perpendicular to the line of the antenna itself.
Dipole - An omnidirectional antenna essentially composed of two monopoles. Generate powerful signals in a restricted space.
Panel - A flat device that focuses from only one side of the panel.
Parabolic - Are used to focus signals from very long distances or weak sources.
Yagi - Crafted from a straight bar with cross sections to catch specific radio frequencies in the direction of the main bar.
Cantenna - Constructed from tubes with one sealed end. Focus along the direction of the open end of the tube.

Gateways - Connects networks that are using different network protocols. Also known as protocol translators, can be stand-alone hardware devices or a software service.
Bridges - Used to connect two networks in order to connect network segments that use the same protocol.

Private circuit - Uses dedicated physical circuits. Dedicated or leased lines, PPP, SLIP, ISDN, DSL.
Packet-switching - Uses virtual circuits. Efficient and cost effective. X.25, Frame Relay, ATM, SDLC, HDLC.

Firewalls

Static Packet-Filtering Firewalls - Filters traffic by examining data from a message header.
Application-Level Firewalls - Filters traffic based on a single internet service, protocol, or application.
Circuit-Level Firewalls - Used to establish communication sessions between trusted partners. SOCKS.

Stateful Inspection Firewall - Evaluate the state, session, or the context of network traffic.
Deep Packet Inspection Firewalls - A filtering mechanism that operates typically at the application layer in order to filter the payload contents of a communication rather than only on the header values. Inspects and filters both the header and payload of a packet.

UTM - Composed of several security features in addition to a firewall. IDS, IPS, TLS/SSL Proxy, QoS, etc.

Stateless - Watch network traffic and restrict or block packets based on source and destination addresses or other static values. Not 'aware' of traffic patterns or data flows. Faster and better for heavier traffic loads.
Stateful - Can watch traffic streams from end to end. Are aware of communication paths and can implement various IP security functions such as tunnels and encryption.

NGFW - A deep-packet inspection firewall that moves beyond port/protocol inspection and blocking. Adds application-level inspection, intrusion prevention, and brings intelligence from outside the firewall.

NAT - Allows private subnets to communicate with other cloud services and the Internet but hides the internal network from Internet users.

Inline - NIDS/NIPS placed on or near the firewall as an additional layer of security.
Out-of-band - Traffic does not go through the NIPS/NIDS.

Bastion Host - A computer or appliance that is exposed on the Internet and has been hardened by removing all unnecessary elements, such as services, programs, protocols, and ports.
Screened Host - A firewall-protected system logically positioned just inside a private network. MOST SECURE.
Scteened Subnet - A subnet is placed between two routers or firewalls and the bastion host(s) is located within that subnet.

Network Attacks

Teardrop Attack - A DoS attack that involves sending fragmented packets to a target machine. The packets overlap one another due to receiving such packets. It is used to crash the network device.
Fraggle Attack - a DoS attack that involves sending a large amount of spoofed UDP traffic to a router's broadcast address within a network.
Smurf Attack - Uses spoofed ICMP traffic using a 3rd party network to bring down a device.
Land Attack - Layer 4 DoS attack where the attacker sets the source and destination information of a TCP segment to be the same. Causes a machine to crash or freeze due to the packet being repeatedly processed by the TCP stack.
SYN flood - DoS attacked which an attacker sends a succession of SYN requests to a target's system in an attempt to consume enough server resources to make it unresponsive to legitimate traffic.
Ping of Death - An oversized ping packet.

Review

Extranet - Used to provide customers with access to the company's network. A portion of a company's network that is accessible by people outside the company.
Intranet - Provides a location for sharing information among members of the company. Provides a location for sharing information among members of the company.

MIC - Helps protect against man-in-the-middle attacks. Developed as an improvement to WEP. A new field with a sequence number is added to wireless packets.

D-H - Security algorithm that can be used for secure key exchange over unsecure networks when public key encryption is implemented. Session key is generated with symmetric encryption.

Teardrop - Uses several large overlapping IP fragments. 
LAND - Uses a malformed IP packet in the source and destination address and port are the same.
Fraggle - DoS attack that uses UDP echo and chargen packets.
Smurf - DoS attack that uses ICMP echo requests.

VLANs create separate broadcast domains. Switches with no VLANs configured can be used to increase the number of collision domains. A CD is a network segment where collisions can occur when frames are sent among the devices on that network segment. 
BD - A network segment where all devices receive a copy of a broadcast sent out by a device within the network segment.

Control plane - SDN controllers. Responsible for network decision-making in both a controller-based network and a traditional network. It is also a centralized area.
Data plane - Network infrastructure devices
Management plane - Network management protocols happen here such as Telnet, SSH, SNMP, and syslog. Enables administrators to connect and manage a network device.
Application plane - SDN applications. Written to allow interaction within the centralized controller. Designed to improve network management efficiency through network automation.

Encapsulation - Takes information from a higher layer and adds a header. Example: Segments are encapsulated in packets. Packets into frames, Frames into bits.

RFS 1918 - Defines the address ranges that the company will use. Defines three private IP address ranges that are intended for LAN.
RFC 2660 - Defines S-HTTP encryption of packets.
RFC 2818 - Defines HTTPS

Session layer establishes and terminates connections between applications.

Spoofing and DoS happens at the same time usually.

Decapsulation means going up the OSI layers
Encapsulation means going down the OSI layers.

POP3 & IMAP4 are used by CLIENTS to receive email from servers.

PGP vs. S/MIME
PGP can be used to encrypt disk drives as well as email messages.

PGP can be used to create digital signatures for an email message.

PGP - A software application that you can use to encrypt and digitally sign email messages.
S/MIME is a protocol that provides security for email messages.

HTTPS requires the use of symmetric and asymmetric keys. S-HTTP does not require any of those.
S-HTTP does not encrypt the HTTP header. HTTPS encrypts the entire message.
HTTPS uses TLS to encrypt HTTP requests and responses. HTTPS is far more secure.

MIMO uses multiple antennas in concert to increase transmission speeds.

ARP cache contains a table of IP addresses and their corresponding MAC addresses. 

RCP is used to remotely copy files.
RSH  - Enables users to remotely execute shell commands.
SSH - Used to transfer files over a network. SSH provides secure authentication, confidentially, and integrity by encrypted all data.

DSSS a modulation technique that uses chipping codes to spread data transmissions across an entire frequency spectrum.

Stateful firewalls allow traffic into a network only if a corresponding request was sent from inside the network. Makes filtering decisions based on previous packets that have been sent.

PPP can transmit multiple Network layer protocols on the same link. Supports synchronous links, such as T1 lines as well as asynchronous links like dial-up

Standard	Speed	GHz
a	54 Mbps	5
n	11 Mbps	2.4
ac	20+ Mbps	2.4
b	600 Mbps	2.4
g	6.9 Gbps	5


Explicit vs. implicit
Explicit - Blocks specific traffic
Implicit - Blocks traffic that is not specifically granted access.

Ad hoc mode - Enables two 802.11 wireless clients to communicate directly with one another without an AP.

Modes
Infrastructure Mode - Common 802.11 wireless mode where wireless clients use an AP to communicate with other clients
Ad hoc - Enables two 802.11 wireless clients to communicate directly with each other without an AP.
Client Mode - Used to allow wireless clients to communicate only with the AP. Wireless clients cannot communicate with other clients.
Monitor - Used to sniff WLAN traffic. Read-only mode. Can be received but not sent out.

Dual stack - Enables a host to communicate with both IPv4 and IPv6

TFTP session is established when a client connects to UDP port 69 on a TFTP server. For a server to send a response back to the client, a UDP port number higher than 1023 that is generated by the client is used.

SDN benefit - Improved threat response time and adaptiveness to changing conditions. 

Port 20 is used to transfer data; port 21 is used for control commands with FTP.

IEEE 802.1X Standard defines a method that uses EAP to establish port-based connections.

IPSec is a framework of protocols that can be used to provide security for VPN connections and to provide data confidentiality by encrypting the data before it is sent over the connection. 

Private address range
Class	Start Address	Finish Address
A	10.0.0.0	10.255.255.255
B	172.16.0.0	172.31.255.255
C	192.168.0.0	192.168.255.255


Public address range
Class	Start Address	Finish Address
A	0.0.0.0	126.255.255.255
B	128.0.0.0	191.255.255.255
C	192.0.0.0	223.255.255.255
D	244.0.0.0	239.255.255.255
E	240.0.0.0	254.255.255.255


Synchronous Data Link Control (SDLC) - A synchronous, full-duplex, WAN protocol that operates at the Data Link Layer. Each SDLC node can act as primary node or a secondary node. Secondary nodes must receive permission from a primary node before transmission.

OSPF - Link-state routing protocol that learns the entire network topology for the area. Uses cost instead of hop count.

ARP resolves IP addresses to MAC addresses.
RARP resolves MAC addresses to IP addresses.

RIP - Distance-vector routing protocol

Teardrop - Sends overlapping IP fragments.
Fraggle - Sends UDP echo and chargen packets.
Smurf - Sends ICMP echo request packets.
LAND - Sends an IP packet with the same source and destination address and port.

AH verifies an IP packet's integrity.

SPF - Technology that authenticates messages by validating the sending system against the domain name in the message header.
DNSSEC - Authenticates DNS resource records by using a chain of trust that has been established from public keys. Mitigates pharming attacks.
DKIM - Technology that digitally signs the message body and parts of SMTP header to mitigate forged sender addresses.
DMARC - Specifies a policy for handling both authenticated and unauthenticated email. Uses SPF and DKIM alignment to mitigate email spoofing and related attacks.

Circuit-level proxy firewalls operate at layer 5

Simple Key Management for Internet Protocols (SKIP) - Provides high availability in encrypted sessions to protect against crashes. Exchanges keys on a session by session basis.

BootP, Boostrap Protocol - When wireless workstation is on-lined it sends out a BootP request with its MAC address to get an IP address and the file from which it should boot. Replaced by DHCP.

Security Modes

Dedicated SM - All users can access all data.
Multi-level - All users can access some data based on their need to know, approval and clearance
Controlled - Limited amount of trust is placed in the system's hardware/software along with classification.
Limited access: Minimum user clearance is not cleared and the maximum data classification is unclassified but sensitive.

LDAP - Client/server based directory query protocol loosely based upon X.500, commonly manages user information, for accessing directory services and manage certificates.
SASL - provides secure LDAP
OpenLDAP - Stores PW in cleartext

Multiplexor - A device that enables more than one signal to be send out of one physical circuit.
CSU/DSU - Digital interface device used to terminate the physical interface on a DTE device. Connects to the closest telephone company switch in a central office.
Bridges - Forwards data to all other network segments if it's not on the local segment.
Gateway - Software the acts as access point to another network or device that translates between different protocols.

Collision Domain - Set of systems that could cause a collision if they transmitted at the same time, mor renumber of systems in domain increases the likelihood of network congestion due to more collisions.

iSCI - Converged protocol that allows location-independent file services over traditional network technologies.

MPLS - High performance networking, uses path labels instead of network addresses, wide are networking protocol, label switching, finds final destination and then labels route for others to follow.

Asymmetric multiprocessing - Used in applications that are dedicated, such as embedded systems, when individual processors can be dedicated to specific tasks at design time.
Symmetric multiprocessors - Hardware and software architecture where two or more identical processors are connected to a single, shared main memory.

Packet switching technologies

X25 - Defines point-to-point communication between data terminal equipment and data circuit terminating equipment.
Link Access Procedure-Balanced (LAPB) - Created for use with X25. Defines frame types and is capable of retransmitting, exchanging and acknowledging frames as detecting out of sequence of missing frames.
Frame Relay - High performance WAN protocol designed for use across ISDN interfaces. No error correction. 
Switched Multimegabit DATA Service (SMDS) - High speed communication over public switches networks for exchanging bursts of data between enterprises.
ATM - Very high bandwidth. Uses 53-byte fixed size cells instead of frames like Ethernet. It can allocate bandwidth up on demand making it a solution for applications. Requires fiber optics.
VOIP - Combines many types of data into a single IP packet. Cost, interoperability and performance wise it’s a major benefit.

SDLC - Allows mainframes to connect to their remote offices. Uses a polling media access method.
HDLC - Extension of SDLC for mainframes. Uses data encapsulation on sychronous serial links using frame characters and checksums.
HSSI - Defines electrical and physical interfaces to use for DRE/DCE communications.


CSMA - Sends out a packet if it does not get acknowledged.
CSMA with Collision Detection - Only one host can send at a time.

Internet = global
Intranet = Local for use within companies
Extranet = Can be used by customers and clients but is not public.

PPTP - Data link protocol, only one single ptp connection per session. Used with dial-up networks, doesn't support EAP, sends packets in plaintext
L2F - Mutual authentication tunneling mechanism. Does not offer encryption.
L2TP - Data link protocol, single point to point connection per session. Uses IPSec and port 115.
IPSec - Network layer protocol, enables multiple and simultaneous tunnels. Encrypts and authenticates. Built into IPv6. 
	Authentication Header
	Encapsulated Security Payload
	2 Modes:
Transport - Only datagram encrypted
	Tunnel - Entire data package is encrypted
	
PVC - Dedicated leased line; logical circuit always exists and is waiting for the customer to send data.

FHSS - Frequency Hopping Spread Spectrum, entire range of available frequencies is employed, but only one frequency at a time is used.
DSSS - Direct Sequence Spread Spectrum, employs all the available frequencies simultaneously in parallel. Provides a higher rate of data throughput. Uses a special encoding mechanism known as chipping code to allow a receiver to reconstruct data even if distorted.
OFDM - Orthogonal Frequency-Division Multiplexing - Employs a digital multicarrier modulation scheme that allows for a more tightly compacted transmission. 

T1 1.5 Mbps
T3 44.6 Mbps
E1 2048 Mbps
Serial Line (SLIP) slow interfaces.

PPP - Adds login, password and error by CHAP and PAP.
ISDN - Combination of digital telphony and data transports.
xDSL - Uses telephone to transport high bandwidth data to remote subscribers.

ADSL - 18,000 feet over copper pair
SDL - 10,000 over copper pair
HDSL - High Rate T1 speed and up to 12,000 feet
VDSL - High speed of 13-52MBPs down , 1.5-2.3 Mbps upstream from 1000 to 4500 feet

FCoE - A form of network data storage solution that allows for high-speed file transfers at upward of 16 GBps.
MPLS - High performance network technology that directs data across a network based on short path labels rather than longer network addresses.



Domain 5:

RADIUS (remote access) - Uses UDP and encrypts the password only.
TACACS+ (Admin access to network devices) Commonly used within Cisco. Encrypts the entire session.
Diameter (4G) - Based on RADIUS and improves many of the weaknesses of RADIUS, but Diameter is not compatible with RADIUS.

Kerberos - Primarily purpose is authentication, as it allows users to prove their identity. Provides confidentiality and integrity using symmetric key encryption. Does not include logging capabilities so it does not provide accountability.

Need to Know - Ensures that subjects are granted access only to what they need to know for their work tasks and job functions. Subjects with a clearance to access is only granted if they actually need it to perform a job.
Least Privilege - Ensures that subjects are granted only the privileges they need to perform their work tasks and job functions. DIFFERENCE = least privilege will also include rights to take action on a system.
Separation of Duties and Responsibilities - Ensures that sensitive functions are split into tasks performed by two or more employees. Helps prevent fraud and errors.

Identification + authentication + auditing = accountability 

False acceptance - Occurs when an invalid subject is authenticated. Type 2 error, false positive.
False rejection - Occurs when a valid subject is rejected. Type 1 error, false negative.

SAML - An XML-based open-standard data format for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider. Common in federation scenarios.
OAuth 2.0 - An open standard for authorization, commonly used as a way for Internet users to log into third party websites using their Microsoft, Google, Facebook, Twitter, One Network etc. accounts without exposing their password.
OpenID - An open standard that provides a decentralized authentication, allowing users to log into multiple unrelated websites with one set of credentials maintained by a third-party service referred to as an OpenID provider.

Access Control Models

DAC - Every object has an owner, and the owner can grant or deny access to any other subjects. NFTS
RBAC - Roles or groups are used to assign permissions directly to users. Typically mapped to job roles. System Admin, Help Desk
Rule-based - Applies global rules that apply to all subjects. Rules within this model are sometimes referred to as restrictions or filters. Firewalls.
ABAC - Rules that can include multiple attributes. Allows it to be much more flexible than a rule-based access control model. SDNs.
MAC - Use of labels applied to both subjects and objects. Military levels like Top Secret. Lattice-based model.
NDAC - A central authority determines what subjects have access based on policies.

Access Control Matrix - A table that includes subjects, objects, and assigned privileges. The system checks the ACM to determine if the subject has the appropriate privileges. Object focused and identify access granted to subjects for any specific object.

Capability Tables - Focuses on subjects (such as users, groups, or roles). Subject focused and identify the objects that subjects can access.

Permissions - Refer to the access granted for an object and determine what you can do with it. Ex: Read permissions.
Rights - Refers to the ability to take an action on an object. Ex: Right to modify the system time on a computer.
Privileges - Combination of rights and permissions. Ex: admin for a computer has full privileges, granting the admin full rights and permissions on the computer.

Open - The port is open on the remote system and there is an application that is actively accepting connections on that port.
Closed - The port is only accessible on the remote system, meaning that the firewall is allowing access, but there is no application accepting connections on that port.
Filtered - Unable to determine whether a port is open or closed. Firewall is interfering with the port.


Security Controls

Assets, Administrative, Logical/Technical, Physical
Control	Definition	Examples
Preventative	Deployed to stop unwanted or unauthorized activity from occurring.	Fences, locks, biometrics, mantraps, alarm systems, job rotation, data classification, penetration testing, access control methods.
Detective	Deployed to discover unwanted or unauthorized activity.	Security guards, guard dogs, motion detectors, job rotation, mandatory vacations, audit trails, IDS, violation reports, honey pots, incident investigations.
Corrective	Deployed to restore systems to normal after an unwanted or unauthorized activity has occurred, such as a security incident.	Antivirus, mantraps, alarms, security policies, BCP.
Compensating	Deployed to provide options to other existing controls to aid in the enforcement and support of a security policy.	Disaster recovery plan with different office location, fire suppression.
Directive	Deployed to direct, confine, or control the actions of subject to force or encourage compliance with security policies.	Security guards, guard dogs, security policy, posted notifications, escape route exit signs, monitoring, supervising, work task procedures, awareness training.
Recovery	Deployed to repair or restore resources, functions, and capabilities after a violation of security policies. More advanced or complex capability to respond to access violations than a corrective access control.	Backups and restores, fault tolerant drive systems, server clustering, database shadowing.
Deterrent	Deployed to discourage the violation of security policies. Picks up where prevention leaves off.	Trespass or intrusion alarms, security cameras, locks, fences, security badges, mantraps, auditing, firewalls.

Control	Physical	Technical	Administrative
Preventive	Door locks, mantraps, and badges	Firewalls, antivirus	Polices and training to ensure employees follow security best practices.
Detective	Motion detectors and security cameras	IDS and system log alerts	Audit trails and reviews to view violations of policies.
Corrective	Backup generators	Patch management systems	Incident response teams that manage the aftermath of a breach
Deterrent	Warning signs	Warning banners	Policies listing out consequences of violating security protocols.
Compensating	Security guard when technical control like a card swipe is broken	Stricter password policies and monitoring when MFA is not used	Additional oversight and manual checks when automated controls fail
Recovery	Off-site backups	System imaging for quick restoration	BCP plans.
Directive	Security checkpoints to direct traffic	Network segmentation to control the flow of data	Instructions for mandatory reporting of security incidents

Access aggregation - A type of attack that combines, or aggregates, non-sensitive information to learn sensitive information and is used in reconnaissance attacks.

TEMPEST - Allows the electronic emanations that every monitor produces to be read from a distance. Useful against CRT monitors.
White Noise - Broadcasting false traffic at all times to mask and hide the presence of real emanations.

IP Probes - Often the first type of network reconnaissance carried out against a targeted network. Attempts to ping each address in a range.

Review

Enrollment - The process of collecting the biological information that is required to authenticate a user. One-time process used by a biometric control system. 
Throughput - Process of authenticating to a biometric control system. 

WS-SecureConversation Web Services - Used to create security contexts for faster message exchanges. Establishes a session key that is used for the duration of the connection. 

Kerberos port for authentication is UDP port 88.
IKE is 50 - Protocol that authenticates IPsec VPN peers.
L2TP 1701
Kerberos provides authentication, authorization, & auditing. Based on symmetric key cryptology.
Realm - Indicates an authentication administrative domain. It is intended to establish the boundaries within which an authentication server has the authority to authenticate a user, host or service.

KDC - Grants tickets to clients for specific servers. Knows all the secret keys of all clients and servers from the network., TGS and AS, single point of failure.
AS (Authentication server)
TGS (Ticket granting server.
Process:
User types a username and password into the client
Client encrypts the username with AES for trans. To the KDC.
The KDC verifies the username against a database of known credentials.
KDC generates a symmetric key that will be used by the client and the Kerberos server. Encrypts the key with a hash of the user's password. Generates an encrypted time-stamped TGT.
Transmits the encrypted symmetric key and the encrypted time-stamped TGT to the client.
Client installs the TGT for use until it expires. The client also decrypts the symmetric key using a hash of the user's password.
User can now use the ticket to service as an application service.

Transient authentication is something you have.

Accountability - Task of reviewing server log files for malicious activity. Logging and verifying activity of authorized users on a system.

Synchronous dynamic token is a Type 2 authentication method that generates passwords and requires accurate time. Generates at a specific interval of time.
Asynchronous dynamic token generates passwords by using a counter and an algorithm.

Kerberos stores secret keys in clear text format.
Kerberos - a SSO access control system. Once a client is authenticated by Kerberos, authentication to other devices on the network is a seamless experience for the user.
Kerberos functions by creating a logical network of devices, known as a realm, and by using a system of tickets and sessions to authenticate clients. 

Password minimum age requirements  are used to ensure that users cannot immediately change new passwords back to old passwords.

Replay attack is a Kerberos vulnerability that can be mitigated by enforcing lifetime limits for a session key.

SAML - IDP verifies authentication and authorization information. SAML is an open standard that is used to provide SSO by exchanging authorization credentials within a federation. The SP is the entity that is being asked by the subject to provide a service or resource.


Dedicated mode - Security clearance, access approval, and a valid need to know
System high mode - Security clearance and access approval
Compartmented mode - A security clearance
Multilevel mode - Security clearance, access approval, and a valid need to know that permits only the information they will access.

Side-channel attacks target smartcards by attempting to obtain information.
Fault analysis - works by adjusting the smartcard's operating environment, such as denying power.
Power differential attacks - Works by directly connecting to pins and attempting to translate power fluctuations.

X.400 - Set of directory technology guidelines that have been replaced by SMTP.

FRR is Type 1
FAR is Type 2

XACML - Used by SDN systems. Used to define access control policies. Can be attribute-based or role-based.
SAML - Used by web applications to create a SSO experience. Can be used to exchange authentication and authorization information.
SPML - XML-based standard used for federated identity SSO.

KDC enables SSO services by acting as a third-party authentication server.

Minutiae - Another term for loops, whorls, ridges, and bifurcations found in fingerprints.

X.500 is a protocol suite that was created by ITU-T to standardize how directories are used on computer networks.
Relative distinguished name (RDN)
Distinguished names (DNs)
Organizational units (Ous)

Role-based access control - Model that uses the tasks performed. Has five elements: users, roles, permissions, operations, and objects.

OpenID Connect - Uses RFC 6749 as a framework but is not maintained by the IETF. It is an open-standard method for decentralized authentication.

Nondiscretionary access control - Uses permissions that are primarily determined by the admin, not organizational policy . Enables the assignment permissions, such as read, write, and execute, to regulate access to data objects.

Type 1 - Something you know for authentication.
Type 2 - Something you have for authentication.
Type 3 - Something you are for authentication.

Type 1 Error - FRR
Type 2 Error - FAR

Minutiae - The ridge endings and bifurcations exhibited by the friction ridges.

Retina Scans - Scans the blood-vessel pattern of the retina. MOST ACCURATE.
Iris Scans - Scans the colored portion of the eye that surrounds the pupil.
Facial Scans - Takes attributes and characteristics like bone structures, nose ridges, eye widths, forehead sizes, and chin shapes.
Palm Scans - Records the palm creases, ridges, and grooves.
Hand Geometry - The shape of a person's hand.
Voice print - People's speech sounds and patterns.
Signature Dynamics - Electrical signals of speed and time that can be captured when a person writes a signature.
Keyboard Dynamics - Captures the electrical signals when a person types a certain phrase.
Hand Topology - Looks at the size and width of an individual's hand and fingers.

Windows uses Kerberos. RADIUS used in wireless networks, OAUTH for web applications. TACACS+ for network devices.



Domain 6:

Regression testing - Performed to ensure that a change has not broken existing functionality or introduced new problems. Has a checklist of tests that should be performed.
Combinatorial testing - Type of black-box testing that involves entering every possible variation of input data into the application.
Pairwise testing - Form of combinatorial testing 

Security audit - Assesses the effectiveness of a security policy's implementation.
Targeted testing - Information is provided to both the pen tester and customer's security personnel.

SOC 1 - Assesses controls related to financial reporting.
SOC 2 - Assesses controls related to security, availability, integrity, and confidentiality and produces results intended for internal distribution 
SOC 3 Same as SOC 2 but used for external distribution.

Type 1 reports - Addresses the design and implementation of the controls in place at a specific point of time. Provides only theoretical assessments of the controls and their suitability 
Type 2 reports - Assess organizational controls over a period of time and evaluate their operation and effectiveness.

Control testing - Broad term that encompasses a range of security testing techniques, including the testing of both administrative controls and technical controls.

Footprinting - First step in the Discovery phase. A simple information gathering from sources like a WHOIS database, mailing lists, or Internet groups.

Log reviews - Particularly for administrator activities, ensure that systems are not misused.
Account management reviews - Ensure that only authorized users retain access to information systems.
Backup verification - Ensures that the organization's data protection process is functioning properly.

KRI - Used by organizations to determine how much risk they are exposed to or how risky a particular venture or activity is.
KPI - Help organizations understand how well they are doing in relation to their strategic plans. Helps to understand the risks involved and the likelihood of not delivering good outcomes in the future.

Security audits - Occur when a third party performs an assessment of the security controls protecting an organization's information assets.
Internal audits - Are performed by an organization's internal staff and are intended for management use.



Domain 7:

WAF - Protect web applications by filtering and monitoring HTTP traffic between a web application and the Internet. Protects against XSS, CSRF, and SQL Injections.
NGFW - Deep-packet inspection firewall that moves beyond port/protocol inspection and blocking. Adds application-level inspection, intrusion prevention, and brings intelligence from outside the firewall.

SoD - A basic security principle that ensures that no single person can control all the elements of a critical function or system.

Information Lifecycle - Creation, Classification, Storage, usage, Archive, Destruction.

SLA - Stipulate performance expectations such as maximum downtimes and often include penalties if the vendor doesn't meet expectations.

Secure Provisioning - Ensuring that resources are deployed in a secure manner and maintained in a secure manner throughout their lifecycles. Secure imaging for a PC. 

Patch management program steps:
Evaluate patches, test patches, approve patches, deploy patches, verify patches.

Vulnerability Management - Includes routine vulnerability scans and periodic vulnerability assessments.
Vulnerability Scanners - Can detect known security vulnerabilities and weaknesses, absence of patches or weak passwords. Using different vendors offers the most insight into a security posture.
Vulnerability Assessments - Extends beyond just technical scans and can include reviews and audits to detect vulnerabilities.

DRMRRRL


Phase	Cont.
Detection	Monitoring tools, IPS, firewalls, users, notification to management and/or help desk
Response	Triage (is it really an incident?) Decision to declare. Limiting damage
Mitigation	First containment effort or step, create team. Contain an incident
Reporting	To relevant stakeholders. (customers, vendors, law, stakeholders). Management decisions
Recovery	Return to normal operations. (Backups). Management decisions
Remediation	Root cause is addressed. Root cause analysis
Lessons Learned	Helps prevent recurrence, improve IR process.

DOS attacks
  
DoS	Def
Teardrop	Sends overlapping IP fragments
Fraggle	Sends UDP echo and chargen packets
Smurf	Sends ICMP echo request packets
LAND	Sends an IP packet with the same source and destination address and port.
Ping-of-death	Sends numerous oversized ping packets to the victim.


Espionage - When a competitor tries to steal information, and they may use an internal employee. External
Sabotage - Malicious insiders can perform sabotage against an org if they become disgruntled for some reason. Insider

Log Files
Security logs
System logs
Application logs
Firewall logs
Proxy logs 

Audit Trails - Records created by recording information about events and occurrences into one or more databases or log files. Used to reconstruct an event, to extract information about an incident. Used to prove or disprove culpability.

Sampling - The process of extracting elements from a large body of data to construct a meaningful representation or summary of the whole.
Statistical sampling - Uses precise mathematical functions to extract meaningful information from a large volume of data.
Clipping - A form of nonstatistical sampling that records only events that exceed a threshold.

Auditing - A methodical examination of an environment to ensure compliance with regulations and to detect abnormalities, unauthorized occurrences, or outright crimes. Serves as a primary type of detective control.

Access Review - Ensures that object access and account management practices support the security policy.
User Entitlement Audit - Ensures that the principle of least privilege is followed and often focus on privileged accounts.

6 types of computer crime:
Military and intelligence attacks
Business attacks
Financial attacks
Terrorist attacks
Grudge attacks
Thrill attacks

eDiscovery - Duty to preserve digital evidence. Includes: Information identification and governance, preservation and collection, processing, review, and analysis, production, and presentation.

Evidence Types
Best	Original.
Secondary Evidence	Copy.
Direct	Proves or disproves an act based on the five senses.
Conclusive	Incontrovertible, overrides all other types.
Circumstantial	Inference from other info.
Corroborative	Supporting evidence but cannot stand on its own.
Opinions	Expert and non-expert.
Hearsay	Not based on first-hand knowledge.

Criminal or Civil trial evidences
Real evidence	Consists of actual objects that can be brought into the courtroom
Documentary evidence	Consists of written documents that provide insight into the facts
Testimonial evidence	Consists of verbal or written statements made by witnesses

Evidences must be relevant, complete, sufficient and reliable.

Cold site - Data center space, power, and network connectivity. Recovery
Warm site - Allows you to pre-install your hardware and pre configure your bandwidth needs. Preventative
Hot - Servers and a live backup site up and running. Replicates production environment fast. Proactive

Service Bureau - A company that leases computer time. Service bureaus own large server farms and often fields of workstations. May be onsite or remote
Mobile Site - nonmainstream alternatives to traditional recovery sites. Consist of self-contained trailers or other easily relocated units.
Multiple Sites - May mix-and-match some combination of the aforementioned options.

RPO - The age of files that must be recovered from backup storage for normal operations to resume if a system or network goes down.
RTO - The duration of time and a service level within which a business process must be restored after a disaster in order to avoid unacceptable consequences associated with a break in continuity.

BCP steps
Project scope and planning
Business impact assessment
Continuity planning
Approval and implementation

BCP - The overall organizational plan for "how-to" continue business.
COOP - The plan for continuing to do business until the IT infrastructure can be restored.
DRP - The plan for recovering from an IT disaster an having the IT infrastructure back in operation.
BIA - Used to identify the business systems and processes that are critical for a company to continue to operate.  MTD is signed here. 

BRP - The plan to move from the disaster recovery site back to your business environment or back to normal operations.

MTBF - A time determination for how long a piece of IT infrastructure will continue to work before it fails.
MTTR - A time determination for how long it will take to get a piece of hardware/software repaired and back on-line.
MTD - The amount of time we can be without the asset that is unavailable BEFORE we must declare a disaster and initiate our DRP.

Goals of BCP and DRP - Minimize the effects of a disaster by improving responsiveness by the employees in different situations, easing confusion by providing written procedures and participation in drills, and helping make logical decisions during a crisis.

Type of DRP	Cont.
Read-through or Desk Check	You distribute copies of DRPs to the members of the DR team for review. Talk.
Structured walk-through or table-top exercise	Members of the DR team gather in a large conference room and role-play a disaster scenario. Talk in a big room with a test moderator and the distributed plans.
Simulation test	Similar to structured walk-through, except some of the response measures are then tested (on non-critical functions.) Doing
Parallel test	Involves relocating personnel to the alternate recovery site and implementing site activation procedures. Doing
Full interruption test	Like parallel test but involves actually shutting down operations at the primary site and shifting them to the recovery site. Doing

Recovery Team - Used to get critical business functions running at the alternate site. Recover
Salvage Team - Used to return the primary site to normal processing conditions. Restore

Backup Strategies
Electronic Vaulting - Used to transfer database backups to a remote site as part of a bulk transfer.
Remote Journaling - Transmitting only the journal or transaction logs to the off-site facility and not the actual files.
Remote Mirroring - A live database server is maintained at the backup site. Most expensive and advanced database back solution.

Review:

Syslog message levels.
Everyone, Always, Carries, Estatic, Worrisome, Noisy, Indecisive, Devils
Syslog Level	Cont.
0	Emergency
1	Alert
2	Critical
3	Errors
4	Warnings
5	Notifications
6	Informational
7	Debugging


SoD - Access control principle that requires more than one user to participate in the completion of a critical task.
Least privilege - Access control principle that requires that a user have no more access to a resource than what is required to do that user's job.
Need to know - Access control principle that requires that a user have no access to information that is not required by the user, even If that user has a rank, clearance level, or authorization for greater access.

Compartmentalization - Access control principle that isolates groups of users from other groups of users based on the information or access required by the groups.

Incident Response	Cont.
Detection	Involves the discovery of a security incident by using log reviews, detective access controls, or automated analysis of network traffic.
Response	The process of activating the IR team.
Mitigation	Process of containing the incident and preventing further damage.
Reporting	The process of documenting the security incident so that management and law enforcement can be fully informed.
Remediation	The process of understanding the cause of the security breach and preventing the breach from occurring again.
Lessons Learned	The process of reviewing of the incident to determine whether any improvements in response can be made.

Halon is the safest compared to FE-13, FM-200, and Inergen

	Full Backup Set	Differential Backup Set	Incremental Backup Set
Saturday	Full	Full	Full
Sunday			
Monday	Full	Differential	Incremental
Tuesday	Full	Differential	Incremental
Wednesday	Full	Differential	Incremental
Thursday	Full	Differential	Incremental
Friday	Full	Differential	Incremental
Backups Required to Restore:	1	2	5

Full - All files, archive bit and modify bit are cleared. 
     Advantage: Only previous day needed for full restore. Restore speed fast.
     Disadvantage: Time consuming for backup speeds.

Incremental - Only modified files, archive bit cleared.
     Advantage: Least time and space. Fast backup speed.
     Disadvantage: First restore full then all incremental backups. Less reliable. Slow Restore speed.

Differential - Only modified files, doesn't clear the archive bit.
     Advantage: Full and only last differential needed. Intermediate time needed.

	Full Backup Set	Differential Backup Set	Incremental Backup Set
Backup Speed	Slower	Medium	Faster
Restore Speed	Faster	Medium	Slower


Software analysis - Type of investigation that typically uses decompiling of reverse engineering to detect malicious activity. Digital forensics happens here.
Media analysis - Examining media such as hard drives. Check past checksums. Check hashes.
Network analysis - Examining network traffic. Web server traffic logs.
Hardware/embedded device analysis - Process of examining a computer hardware and software device that has a specific function.

Checksum - The output from a one-way hash function. Used to ensure the integrity of data that is acquired during digital forensics.

Change management stages:
RRATSD
Radical, Reasons, Always, Turns, Serious, Damage

Types of system failure
System reboot - System shuts itself down in a controlled manner after detecting inconsistent data structures or runs out of resources.
Emergency restart - When a system restarts after a failure happens in an uncontrolled manner.
System cold start - When an unexpected kernel or media failure happens and the regular recovery procedure cannot recover the system in a more consistent state.

FE-13 is the safest fire suppressions system in an electrical environment. 

DRP Test	Cont.
Read-through	Involves the distribution of DRP documents.
Structured walk-through	Table-top. Gathers around a table with a moderator
Simulation Test	Asked to develop a response to a given disaster.
Parallel Test	Employees are relocated to the DRP's recovery location.
Full-interruption Test	Employees are relocated and they also bring down primary locations.


CFCE - Certified Forensic Computer Examiner
CFTT - Computer Forensics Tool Testing - Testing and certification of digital forensics equipment created by NIST.
CAWFE - Certified Advanced Windows Forensic Examiner
ICMDE - Certified Mobile Device Examiner

DRP focuses on the restoration of specific IT services so that a company can recovery from a disaster quickly.
BCP - Focuses on maintaining business operations no matter what events a business faces.
BIA - Identifies business systems and processes that are critical for a company to continue to operate.
MTD - Used to prioritize the recovery of assets in a BCP or DRP. Determine whether you should create a cold site, a warm site, or a hot site.

System logs monitor computer system events. Also monitor OS events, such as a service stops or starts.

Security admin - Responsible for user account management and reviews of audit data in a client/server architecture. Oversees system security.
System admin - Typically monitors and maintains the systems and applications in a distributed computed environment.
System operator - Found within mainframe environments. 
Power user - An account that has heightened-privilege account that enables a user to perform some tasks that ordinary users cannot perform.

MTD is the sum of RTO and WRT. Amount of time required to configure and verify a recovered system.

SoD - Access control principle that is designed to create a system of checks and balances on employees who have privileged access. Requires more than one user to participate in the completion of a critical task.
RoD - Access control principle that does not allow one user to perform the same function for more than one consecutive interval of time. Enforces user integrity. 
Compartmentalization - Access control principle that isolates groups of users from other groups of users based on the information or access required by the groups.
Need to know - Access control principle that requires that a user have no access to information that is not required by the user, even if that user has a rank, clearance level, or authorization for greater access.

Evidences - Be authentic, accurate, complete, convincing, admissible

Subscription service - A reliable DR solution when a company purchases a service, it transfers the risk to a third-party provider.

Service Account - Enables an application to perform system-level actions.

Security domain - An access control principle that uses technology to segregate systems and users who have a particular function from other systems and users who are responsible for other functions.



Domain 8:

 CI/CD - Implement Identity and access management, Store secrets securely, no hard-coded secrets, automate vulnerability scanning in the pipeline, release versioning, track issues.

Basic architecture of RDBMS

Table (Relation) - Contains a number of attributes, or fields. Each attribute corresponds to a column in the table.
Row (Records/Tuple) - A data record within a table. Each row, which represents a complete record of specific item data, holds different data within the same structure.
Column (Fields/attributes) - A set of data values of a particular type, one value for each row of the database.

Type of Key	Cont.
Candidate Key	A subset of attributes that can be used to uniquely identify any record in a table. No two records in the same table will ever contain the same values for all attributes composing a candidate key.
Primary Key	Used to uniquely identify records in a table. Has one primary key. Ex: Employee ID
Foreign Key	Used to enforce relationships between two tables. Known as referential integrity. Ensures that if one table contains a foreign key, it corresponds to a still-existing primary key in the other table in the relationship.


Type	Definition	Prevention
Aggregation	The ability to create sensitive information by combining non-sensitive data from separate sources.	Need-to-know, and least privilege
Inference	The ability to deduce or assume sensitive information from observing non-sensitive pieces of information.	Blurring data and database partitioning 


Types of memory
Memory	Cont.	Example
Primary memory	Consists of the main memory resources directly available to a system's CPU. Usually, the most high-performance storage available. 	Volatile RAM.
Secondary storage	Consists of more inexpensive, nonvolatile storage resources available to a system for long-term use. 	Magnetic and optical media, such as tapes, disks, hard drives, flash drives, and compact disc/digital versatile disc (CD/DVD) storage.
Virtual memory	Allows a system to simulate additional primary memory resources through the use of secondary storage.	System low on RAM makes a hard disk available for direct CPU addressing.


Types of storage
Storage		
Virtual	Allows a system to simulate secondary storage resources through the use of primary storage.	RAM disk that presetns itself to the OS as a secondary storage device but is actually implemented in volatile RAM.
Random Access	Allows the OS to request contents from any point within the media.	RAM and hard drives.
Sequential Access	Requires scanning through the entire media from the beginning to reach a specific address.	Magnetic tape.
Volatile 	Loses its contents when power is removed from the resource.	RAM.
Nonvolatile	Does not depend the presence of power to maintain its contents.	Magnetic/optical media and NVRAM.

Expert Systems - Consist of two main components: a knowledge base that contains a series of "if/then " rules and an interface engine that uses that information to draw conclusions about other data.

Machine Learning - Techniques that attempt to algorithmically discover knowledge from datasets.

Neural Networks - Simulate function of the human mind by arranging a series of layered calculations to solve problems . Require extensive training on a particular problem before they can offer solutions.

Agile Model four principles - Individuals and interactions over processes and tools, Working software over comprehensive documentation, Customer collaboration over contract negotiation, Responding to change over following a plan.
Waterfall - System requirements, Software requirements, Preliminary design, detailed design, code and debug, testing, ops & maintenance.

SW-CMM - 5-step model for measuring software development orgs.
L1 - Initial: no plan.
L2 - Repeatable: Basic lifecycle management.
L3 - Defined: Formal, documented SW development processes.
L4 - Managed: Quantitative measures to gain detailed understanding.
L5 - Optimized: Continuous development process, w/ feedback loops.

IDEAL Model - Model for software development which implements many of the SW-CMM attributes.
Initiating: Business reasons outline, support & infrastructure for initiative put in place.
Diagnosing: Engineers analyze current state of org & make recommendations for change.
Establishing: Org takes recommendations & develops plan to achieve those changes.
Acting: Plan put into action. Org develops solutions, tests, refines & implements.
Learning: Org continuously analyzes efforts and results, proposes new actions to drive better results.

XSS - Occur when web apps contain 'reflected input'. A type of injection, in which malicious scripts are injected into otherwise benign and trusted websites. Occur when an attacker uses a web application to send malicious code to a different end user.
XSRF - Attacks exploit the trust that sites have in a user's browser by attempting to force the submission of authenticated request to third-part sites.

IP Probes - Automated tools simply attempt to ping each address in a range. Systems that respond to the ping request are logged for further analysis.
Port Scans - Scans a system for open/listening ports. Often, web servers, file servers, and other servers supporting critical operations are prime targets.

SDL
Real, Developers, Ideas, Take, Effort
Requirements analysis
Design
Implementation
Testing
Evolution

Concentric Circle Security . Defense in-depth - Several mutually independent security applications, processes, or services that operate toward a single common goal.

Software Security Attacks
Type	Cont.	example
OS Attack	Attackers always try to search for OS vulnerabilities	Buffer overflow, OS bugs, unpatched OS
Application-Level Attacks	Attacks Apps	Overflow, active content, XSS, DoS, SQL injection, Session hijacking, phishing
Shrink Wrap Code Attacks	Act of exploiting holes in unpatched or poorly configured software you can buy and install	Unpatched software that contains sample scripts/code
Misconfiguration Attacks	Target poorly configured service or device, or one left in default configuration.	WiFi default settings with WEP or 'admin' as a password

Review:

Accreditation phase - The software is accepted by the data owner, even if it has not been certified.

Type-safe - A language that prevents a variable from containing information that is different from the variable's declaration.

SDLC Phases: Initiation and planning, functional requirements definition, System design specification, development and implementation, documentation and common program controls, acceptance, testing and evaluation controls, certification, accreditation, implementation.

Sandbox - a mobile control mechanism that limits the amount of system resources a program can use.

ASLR - A buffer overflow protection mechanism that places executables into random memory addresses at boot time.

Heap metadata protection is used to force an application to fail immediately if a pointer is freed.

Java applet is a client-based technology that uses a sandbox as a security control.
ActiveX uses a client-based technology that uses digital certificates. Browser applications that support only Microsoft Windows OS.

Live workloads are used to test software applications. It simulates how the application behaves when accessed by a large number of users or processes, thereby providing the most accurate stress testing for the application.

Lexical obfuscation - Deals with renaming classes, fields, and methods, replacing them with new identifiers that lack intuitive meaning.
Data obfuscation - Deals with modifying data and data structures in order to hide what the data is used for.
Control flow obfuscation - Deals with making an application harder to understand or decompile
Prevention obfuscation - Includes inserting junk bytes, converting branches to jsr instructions, and combining try blocks with catch blocks. Used to make a program obscure to computers.

Microsoft's SDL

Training - Conducting core security training for software development members.
Requirements - Establish security requirements, create quality gates and bug bars, perform security and privacy risk assessments.
Design - Establish design requirements, perform attack surface analysis and reduction, use threat modeling.
Implementation - Create the software based on the blueprint they created. Includes use approved tools, deprecate unsafe functions, and static analysis
Verification - Ensures that code meets the security standards they established in the Requirements phase. Performs dynamic analysis, fuzz testing, and attack surface review.
Release - Prepare the software for release. Create incident response plans, final security reviews, and certify the release and archive the project materials.
Response - Occurs after everything after the software has been released.

Object reuse - The process of using authentication credentials that an application or process has shared in memory to authenticate a user or another application or process.

Garbage collection - The process of cleaning up and controlling what is left in memory by an application.

Negative testing - Software testing technique that issues invalid information to an application to ensure that the application appropriately handles the input.

Pointer Encoding - The buffer overflow protection mechanism that Microsoft recommends but does not require for ISVs who are implementing the SSDL. Applies an exclusive OR (XOR) random value with pointers, encoding the pointer value.

Normalization - Processes that are typically used to organize data in a relational database so that is logical, concise, and consistent.
1NF - Data that is logically divided.
2NF - Process of moving data that partly depends on primary keys into a different table.
3NF - Used to remove data that has no relevance to a table's primary key. Data is placed into different table that might or might not contain a primary key.

Gantt Chart - A type of bar chart that shows the interrelationships over time between projects and schedules.
PERT - Project scheduling tool used to judge the size of a software product in development.

DDL - Defines structure and schema
DML - View, manipulate and use the database via VIEW, ADD, MODIFY, SORT, and DELETE commands.
DDE - Enables applications to work in a client/server model by providing the inter-process communications mechanism.

Polyinstantiation - Occurs when two or more rows in the same relational database table appear to have identical primary key elements but contain different data for use at differing classification levels. Used against inference attacks.

Expert Systems - Seeks to embody the accumulated knowledge of experts on a particular subject and apply it in a consistent fashion to future decisions.
Knowledge base - If-then statements 
Interference system - Decision program.

1GL - All machine languages.
2GL - All assembly languages.
3GL - All compiled languages.
4GL - Approximates natural languages and includes SQL for databases.
5GL - Allow programmers to create code using visual interfaces.

Compiler - Translates higher level program into an executable file.
Interpreter - Reads higher level code, one line at a time to produce machine instructions.
Assembler - converts machine-code into binary machine instructions. Translates assembly into machine language.

Encapsulation (Data Hiding) - Only data it needs, no accidental access to data.
Delegation - Forwarding a request to another object.

Poly-instantiation - Occurs when two or more rows in the same relational database table appear to have identical primary key elements but contain different data for sue at differing classification levels. 

COBRA - Broker architecture enables programs written in different languages and using different platforms and OS's through IDL.

Cohesion - Ability to perform without use of other programs, strength of the relationship between the purposes of methods within the same class.
High cohesion - Without use of other modules.
Low cohesion - Must interact with other modules

Coupling - Effect on other modules. Level of interaction between objects
High coupling - Module largely affects many more modules.
Low coupling - It doesn’t affect many other modules.

Abstraction - Object-oriented programming "black-box" doctrine that says that users of an object don't necessarily need to know the details of how the object works.

Storage covert channel - Processes communicate via storage space on the system.
Covert timing channel - One process relays to another by modulating its use of system resources. 

Mobile code
Java - Sandboxes, no warnings, programs are compiled to bytecode. Uses a sandbox as a security control.
ActiveX - Authenticode, relies on digital signatures.

Covert Channel - A way to receive information in an unauthorized manner.
Covert Storage Channel - Writing to storage by one process and reading by another of lower security level.
Covert Timing Channel - One process relays to another by modulating its use of system resources.

LOKI - A tool used for cover channel that writes data directly after the ICMP header.

Review - CCCUre

Key clustering
Key Collision

Tort law

NDAC
RBAC

Multipart virus - Infects both the boot sector and executable files. Resides in memory and then infects the boot sector and then the entire system.

Three Parts of the Relational Model

Structural - Defines the core of the data and the relationships involved. Described in terms of relations, tuples, and attributes and domains.
Manipulative - Defines how the data in the model will be accessed and manipulated. Used to provide answers to some question posed by a user of the data. Achieved through relational algebra or relational calculus.
Constraints - Defines limits on the model. The constraints determine valid ranges and values of data to be included in the model.

A database can be defined as a persistent collection of interrelated data items.

DDL - The description of the database is called a scheme. The schema is defined by the DDL. Used for defining data structures and schemas.
DML - Used to retrieve, insert and modify database information. 
DCL - allows admins to configure security access to relational databases.

Foreign key - Defined as an attribute in one relation that has values matching the primary key in another relation.

Bind variables - Placeholders for literal values in a SQL query being sent to the database on a server.

OLTP - All transactions are recorded as they occur. The transactions should be written to a report and reviewed.

Concurrency controls - Ensure that two users cannot simultaneously change the same data, or that one user cannot make changes before another user is finished with it.
Atomicity - Ensures that all of the steps inv9olved in the transaction complete successfully. If one step should fail, then the other steps should not be able to complete.

Smartcards are tamper resistant, mobile storage and application of private keys of the users.

NDAC - Rules that are not established at the discretion of the user. Rule-based access control is a type of NDAC due to being determined by rules.
DAC - Identity based access control system. The owner of an object is defined as the person who created the object. The owner has the discretion to grant access to other users on the network.

Lattice-based access control - Used to represent the relationships between different levels of access permissions.

Differences between MAC and RBAC - MAC uses LABELS.

NIST-7316

Object - An entity that contains or receives information.
Subject - An active entity, generally a person, that causes information to flow among objects.

SOD - The principle that not user should be given enough privileges to misuse the system. Ex: Person authorizing a paycheck should not also be the one who can prepare it.

DAC - Leaves a certain amount of access control to the discretion of the object's owner or anyone else who is authorized to control the object's access. 
NDAC - Policies in this category have rules that are not established at the discretion of the user. Cannot be changed by users, but only through administrative actions.
MAC - A policy access control that are made by a central authority. Used within military security. The system enforces the protection decisions.
RBAC - Access decisions are based on the roles that individual users have as part of an organization. Assigned roles.

Brewer Nash / Chinese Wall - Addresses conflict-of-interest issues. Confidentiality policy.

DCOM - Defines how distributed components interact and provides an architecture for interposes communication.

Digital signature is used to achieve integrity, authenticity, and non-repudiation. Sender's private key is used to encrypt a message digest of the message and the receiver needs to validate the same using the sender's public key.

Baseline - Provides the minimum level of security necessary throughout the organization. 
Standards specify how hardware and software products should be used throughout the organization.
Procedures - Detailed step-by-step instruction on how to achieve certain tasks.
Guidelines - Recommendation actions and operational guides to personnel when a specific standard does not apply.

Packet filtering firewalls can also enable access only authorized application port or service numbers.

RAID 1 - An exact copy or mirror of a set data on two disks.
RIAD 2 - Stripes data at the bit.
RAID 4 - Uses block-level striping with a dedicated parity disk.

Advisory policies are not mandated. Security policies that are not to be followed but are strongly suggested.

Type 1 error - False rejection
Type 2 error - False Acceptance

Authentication Factors:
Type 1 - Something you know
Type 2 - Something you have
Type 3 - Something you are

Digital Signature Standards provide Authentication, Integrity, and Digital Signatures.

TCB - The total combination of protection mechanisms within a computer system. Includes the hardware, software, and firmware.
Security kernel - Implements and enforces the reference monitor concept.

Ciphertext-Only - Type of attack where an attacker has the ciphertext of several messages. Goal is to discover the key.
Known-Plaintext - Attacker has the plaintext and corresponding ciphertext of one or more messages. Goal is to discover the key.

Chosen-Plaintext Attack - The attacker has the plaintext and ciphertext, but can choose the plaintext that gets encrypted to see the corresponding ciphertext.
Chosen-Ciphertext - Attacker can choose the ciphertext to be decrypted and has access to the resulting decrypted plaintext.

Preliminary steps to security planning include: Establish objectives, List planning assumptions, and determine alternate courses of action.

Key Escrow Algorithms - A feature implemented with some CA and crypto system to all for key recovery in case of damage or loss of the key.

The process of encrypting bulk data using symmetric key cryptography and encrypting the session key with a public key algorithm. 

Directory Service - Type of network service that stores information about the various resources in a central database on a network and help network devices locate services.

Network Management - Refers to the activities, methods, procedures, and tools that pertain to the operation, administration, maintenance, and provisioning of network systems.

DCE - A service provider device that does the actual data transmission and switching in the frame relay cloud.

PPP - A protocol for communication between two computers using a serial interface. A full duplex protocol that can be used on various physical media. 
X.25 - An ITU-T standard protocol suite for packet switched wide area network communication.

Frame Relay - has DTE, and DCE. 
DTE - Usually a customer owned device that provides a connectivity between company's own network and the frame relay's network.
DCE - Service provider device that does the actual data transmission and switching in the frame relay cloud.

Frame relay cloud - A collection of DCE that provides switching and data communication functionality. 

ATM - Uses cell switching. Used within high speed network technologies. Connection orientated technology that uses fixed channels.

MPLS - Used to speed up network traffic flow and making it easier to manage. Sets up specific paths for a given sequence of packets, identified by a label put in each packet. Works with IP, ATM, and frame relay network protocols. Allows most packets to be forwarded at the L2 level rather than L3. 

TCP/IP Model

Application Layer - Top most layer. Defines application protocols and how host programs interface with Transport layer services to use the network.
Transport Layer - Used to permit devices on the source and destination hosts to carry on a conversation. Defines the level of service and status of the connection used when transporting data.
Internet Layer - Pack data into data packets known as IP datagrams. Contains source and destination addresses. Packet switching happens here.
Network Access - Defines details of how data is physically sent through the network, including how bits are electrically or optically signaled by hardware devices that interface directly with a network medium.

Clipping level - The point at which a system decides to take some sort of action when an action repeats ap reset number of times. The action bay be to log the activity, lock a user account, temporarily close a port, etc.

OEP - Provides the response procedures for occupants of a facility in the event of a situation posing a potential threat to the health and safety of personnel, the environment, or property. 
BCP - Addresses business processes and provides procedures for sustaining essential business operations while recovering from a significant disruption.
DRP - Applies to major, usually catastrophic events that deny access to the normal facility for an extended period.

Industry Vertical - Specific Control Frameworks apply to different industries. COBIT 5, HIPPA, PCI-DSS, etc.

Passphrases - Fact or opinion-based information used to verify an individual's identity.

IKE - Protocol performs peer authentication at Phase 1. IKE is a protocol used to configure a security association in the IPsec Protocol suite. Uses X.509 certificates for authentication.

Lattice model - Users are assigned security clearances and the data is classified. Access decisions are made based on the clearance of the user and the classification of the object.

PBX -  A sophisticated computer based switch that can be thought of as essentially a small in-house phone company for the organization that operates it.

Kerberos is a trusted, credential-based, third-party authentication protocol that uses symmetric key cryptography to authenticate clients to other entities on a network for access to services.

Trusted system - One that meets its intended security requirements. Has (1) policy, (2) mechanism, and (3) assurance. A trusted system is one in which all protection mechanisms work together to process sensitive data for many types of users.

Bell-LaPadula model - A confidentiality model for information security based on the military classification of data.

Types of attacks

Military and Intelligence Attacks - Perpetrated by criminals, traitors, or foreign intelligence agents seeking classified law enforcement or military information.
Financial Attacks - Banks, large corporations, and e-commerce sites are the targets of financial attacks. Embezzle funds, online financial information, etc.
Business Attacks - Competitive intelligence gathering, DoS, etc.
Grudge Attacks - Targeted at individuals or businesses and are motivated by a desire to take revenge against a person or org.

Digital Envelope - A message encrypted with a secret key attached with the message. The secret key is encrypted with the public key of the receiver.

Acronyms

Accountability - Ensures that account management has assurance that only authorized users are accessing the system and using it properly.
ActiveX Data Objects (ADO) - A Microsoft high-level interface for all kinds of data.
ARP - Used at the MAC Layer to provide for direct communication between two devices within the same LAN segment.

ABAC - Access control paradigm whereby access rights are granted to users with policies that combine attributes together.
Authorization - The process of defining the specific resources a user needs and determining the type of access to those resources the user may have.
IEEE 802.15 - Bluetooth wireless technology.

Bridges - Layer 2 devices that filter traffic between segments based on MAC addresses.

Business Continuity (BC) - Actions, processes, and tools for ensuring an org can continue critical operations during contingency.
BIA - A list of the organization's assets, annotated to reflect the criticality of each asset to the organization.

SMM or SW-CMM - Maturity model focused on quality management processes and has five maturity levels that contain several key practices within each maturity level.
CA - An entity trusted by one or more users as an authority that issues, revokes, and manages digital certificates to bind individuals and entities to their public keys.

CDMA - Every call's data is encoded with a unique key, then the calls are all transmitted at once.
Common Object Request Broker Architecture (CORBA) - A set of standards that addresses the need for interoperability between hardware and software products.

Concentrators - Multiplex connected devices into one signal to be transmitted on a network.
Condition coverage - This criterion requires sufficient test cases for each condition in a program to take on all possible outcomes at least once. It differs from branch coverage only when multiple conditions must be evaluated to reach a decision.

Confusion - Provided by mixing (changing) the key values used during the repeated rounds of encryption. Where the key is modified for each round, it provides added complexity that the attacker would encounter.
Covert Channel - An information flow that is not controlled by a security control and has the opportunity of disclosing confidential information. 

Cryptanalysis - The study of techniques for attempting to defeat cryptographic techniques and, more generally, information security services provided through cryptography.
Cryptography - Secret writing. Provides confidentiality, integrity, authenticity, non-repudiation, and access control. 

DBMS - A suite of application programs that typically manages large, structured sets of persistent data.
DevOps - An approach based on lean and agile principles in which business owners and the development, operations, and quality assurance departments collaborate. 

Diffusion - Provided by mixing up the location of the plaintext throughout the ciphertext. The strongest algorithms exhibit a high degree of confusion and diffusion. 
Digital certificate - An electronic document that contains the name of an organization or individual, the business address, the digital signature of the certificate authority issuing the certificate, the certificate holder's public key, a serial number, and the exp date. Binds things to their public keys.

DRM - A broad range of technologies that grant control and protection to content providers over their own digital media.
Digital signatures - Provides authentication of a sender and integrity of a sender's message and non-repudiation services.

DR - Those tasks and activities required to bring an organization back from contingency operations and reinstate regular operations. 

Due Care - A legal concept pertaining to the duty owned by a provider to a customer.
Due Diligence - Actions taken by a vendor to demonstrate/provide due care.

Encoding - The action of changing a message into another format through the use of a code.
Encryption - The process of converting the message from its plaintext to ciphertext.

FCoE - A lightweight encapsulation protocol, and it lacks the reliable data transport of the TCP layer.

Guidelines - Suggested practices and expectations of activity to best accomplish tasks and attain goals.

Hash function - Accepts an input message of any length and generates, through a one-way operation, a fixed-length output called a message digest or hash.

IV - A non-secret binary vector used as the initializing input algorithm, or a random starting point, for the encryption of a plaintext block sequence to increase security by introducing additional cryptographic variance and to synchronize cryptographic equipment. 

IGMP - Used to manage multicasting groups that are a set of hosts anywhere on a network that are listening for a transmission. 

Job rotation - The practice of having personnel become familiar with multiple positions within the organization as a means to reduce single points of failure and to better detect insider threats.
Last privilege - The practice of only granting a user the minimal permissions necessary to perform their explicit job function.

Loop coverage - The criterion requires sufficient test cases for all program loops to be executed for zero, one, two, and many iterations covering initialization, typical running, and termination (boundary) conditions.

MAD - The measure of how long an organization can survive an interruption of critical functions.
Message authentication code (MAC) - A small block of data that is generated using a secret key and then appended to the message, used to address integrity.

Need-to-know - Primarily associated with organizations that assign clearance levels to all users and classification levels to all assets; restricts users with the same clearance level from sharing information unless they are working on the same effort. Entails compartmentalization. 
Null cipher - Hiding plaintext within other plaintext. A form of steganography.

OAuth - Framework enables a third-party application to obtain limited access to an HTTP service, either on behalf of a resource owner by orchestrating an approval interaction between the resource owner and the HTTP service, or by allowing the  application to obtain access on its own.
OSPF - An interior gateway routing protocol developed for IP networks based on the shortest path first or link-state algorithm.

Overt security testing - Overt testing can be used with both internal and external testing. Internal perspective, the bad actor simulated is an employee. The Org's IT staff is made aware of the testing and assess the impact of the test by providing specific guidelines for the test scope.

PPP - provides a standard method for transporting multiprotocol datagrams over point-to-point links.

Policy - Documents published and promulgated by senior management dictating and describing the organization's strategic goals. High level statement.
Procedures - Explicit, repeatable activities to accomplish a specific task. Procedures can address one-time or infrequent actions or common, regular occurrences.

Real user monitoring (RUM) - An approach to web monitoring that aims to capture and analyze ever transaction of every user of a website of application.

Risk - The possibility of damage or harm and the likelihood that damage or harm will be realized.
Risk acceptance - Determining the potential benefits of a business function outweigh the possible risk impact/likelihood and performing that business function with no other action. 
Risk avoidance - Determining the impact and/or likelihood of a specific risk is too great to be offset by the potential benefits and not performing a certain business function because of that determination. 
Risk mitigation - Putting security controls in place to attenuate the possible impact and/or likelihood of a specific risk.
Risk transference - Paying an external party to accept the financial impact of a given risk.

SAML - A version of the SAML standard for exchanging authentication and authorization data between security domains.

Separation of duties - The practice of ensuring that no organizational process can be completed by a single person; forces collusion as a means to reduce insider threats. 
SIP - Designed to manage multimedia connections.

Smurf - ICMP Echo Request sent to the network broadcast address of a spoofed victim causing all nodes to respond to the victim with an Echo Reply.

SNDs - Separates network systems into three components: raw data, how the data is sent, and what purpose the data servers. This involves a focus on data, control, and application (management) functions or "planes".
SD-WAN - An extension of the SDN practices to connect to entities spread across the internet to support WAN architecture especially related to cloud migration.

Standards - Specific mandates explicitly stating expectations or performance or conformance. 

Substitution - The process of exchanging on letter or bit for another.

Teardrop Attack - Exploits the reassembly of fragmented IP packets in the fragment offset field that indicates the starting position, or offset, of the data contained in a fragmented packet relative to the data of the original unfragmented packet.

Time multiplexing - Allows the OS to provide well-defined and structured access to processes that need to use resources according toa controlled and tightly managed scheduled. 

Transposition - The process of reordering the plaintext to hide the message by using the same letters or bits.

TCB - The collection of all of the hardware, software, and firmware within a computer system that contains all elements of the system responsible for supporting the security policy and the isolation of objects.
TPM - A secure crypto processor and storage module.

WiFi (Wireless LAN IEEE 802.11X) - Primarily associated with computer networking, Wi-Fi uses the IEEE 802.11x specification to create wireless local-area network either public or private.
WiMAX (Broadband Wireless Access IEE 802.16) - One well-known example of wireless broadband is WiMAX. Can deliver data rates of more than 30 megabits per second.

TSEC is based on government requirements.  
ITSEC is based on international input. Integrity is the fundamental change over TCSEC.

Identification is the function of the username.
Password is the function of authentication.

Clipping level establishes a normal error rate that can be ignored for violation analysis purposes.

TCSEC - Largely based on Bell-LaPadula. Concerned with confidentiality. Focuses on measuring security products. D1 which means no security to A1 which means very robust and mathematically verified security. Most common at C2 or B1. Not good for networked environments.
ITSEC -  Works well In a network environment. Used to measure integrity with function and assurances. E0 to E6.
Common Criteria - Compromises multiple components that work together. Uses EAL levels.
     PP - Lists the security capabilities that a type of category of security product should possess. Ex: VPN capabilities, firewall, 2FA, IDS, etc.
     TOE - A vendor's product that is being rated and being assessed.
     ST - Describes from the vendor's perspective of capabilities outline in the PP. Measured against functional and assurance security capabilities. 
EAL7	Formally verified, designed, and tested
EAL6	Semi-formally verified, designed, and tested
EAL5	Semi-formally designed and tested
EAL4	Methodically designed, tested, and reviewed
EAL3	Methodically tested and checked
EAL2	Structurally tested
EAL1	Functionally tested
Most orgs will not purchase a product that is rated above EAL4. EAL7 is more vulnerable to compromise, due to being more complex and harder to maintain.

Key Clustering - Where two different keys will produce the same cipher text from the same plaintext.
Key Escrow - Where a decryption key is placed in escrow with one or more agents so it can be obtained by law enforcement with court approval.

BCP - A series of procedures and plans that help an organization maintain operations in a long-term disaster. BCP is focused on a business as a whole. High level
DRP - Focused on critical IT infrastructure and processes.

Try…catch - Example of error handling. Doesn't execute the code in error in an attempt to still manage it properly.

SOW - Outlines the tasks and deliverables the assessment supplier will provide.
Work commencement - Authorization to commence work
Noncompete agreement - Restricts the security assessor from disclosure.
NDA - Reinforces trust between people.

ARP = MAC to IP
RARP = IP to MAC

Reference Model - Enforces access control between subjects and objects. Validates access to every resource before granting access request.
TCB - Security controls that would be implemented to protect an architecture. Refers to all protection mechanisms within an architecture. 

Subjects - A subject is an active entity that is seeking rights to a resource or object. Can be a person, program, or process.
Object - Passive entity, such as a file or storage resource. 

State Machine Model - Refers to a system that is always in secure mode regardless of the operational state it is in. A state is a snapshot of a system at a specific time.

Bell-LaPadula Model - Confidentiality. Used within DoD. Based on State machine model. Implements mandatory access controls and the lattice model. 
     SS property - States that a subject at a specific classification level cannot read data with a higher classification level.
     Security property - States that a subject at a specific classification level cannot write data to a lower classification level. 
Doesn't allow for subjects at a higher security clearance to write to objects accessible at a lower security clearance.
Main focus is to prevent accidental leakage of sensitive information.
No read up, no write down.

Biba - Integrity. State machine model based on classification lattice with mandatory access.
     The prevention of object modification by unauthorized subjects.
     The prevention of unauthorized object modification by authorized subjects.
     The protection of internal and external object consistency.

     SI Axiom, subject at a classification level cannot read data with a lower class level.
     Integrity Axiom, subject at a specific classification level cannot write data to a higher classification level.
     Subject at one level of integrity cannot invoke a subject at a higher level of integrity.
Main focus is safeguarding objects from outside threats and internal threats. 

Clark-Wilson - Integrity. Implements a subject-program-object. Subjects have accessibility to objects exclusively through programs. No direct access.
     Well-formed transactions - Subjects are able to access objects. Each program has restrictions.
     SoD - Divides critical functions into two or more parts.

Brewer and Nash Model / Chinese Wall - Confidentiality. Allows access controls to change dynamically based on the user's past activity. Creates security domains that are sensitive to the notion of COI

Take-Grant - Confidentiality-based model that uses a directed graph to specify the rights that can be passed from one subject to another. Gives permissions to subjects to take rights from other subjects.

Information Flow Model - Based on a state machine model, used to block unauthorized, insecure, or restricted information flow between subjects and objects. Bell-LaPadula and Biba.

Noninterference Model - Addresses how the actions of a higher security level subject impacts the system state or actions of a subject at a lower security level. Actions at a higher security level subject should have influence on the actions of a subject at a lower subject level. The higher security subject should go unnoticed at the lower level.

Access Control Matrix - A table that states a subject's access rights on an object.
       Capability list - Connected to the subject and outlines the actions that a specific subject is allowed to perform on each object. Allows discretionary access control.

PLC - A controller that can have multiple inputs and outputs.
SCADA - Large industrial control systems that can span large geographic areas. Control and supervise operations using inputs from PLCs
DCS - A network of PLCs, sensors, and supervisory computers.

Reduction analysis - Supports threat modeling by identifying elements common to underlying threats.

Access control triple - Ensuring that subjects can only access objects through the use of an application.

Output encoding - The conversion of certain characters within website form inputs into HTML character entity reference equivalents prior. Application security technique used to ensure that certain characters within form inputs are processed as data and not programming syntax.
Input validation - Used to ensure that actual input is aligned to the input expected for a particular field, before it is processed.

SAML is a SSO technology based on XML. Has the Principal, IDP, and SP. Popular SSO solution that exchanges authentication 

Low humidity leads to an increase in static electricity.
High humidity leads to corrosion.

Entitlement - Refers to the level of privileges granted to a user. If a user has been granted access to an object, they are entitled to it.

Anonymization - The process of removing data to the point that it is impossible to identify the subject(s). Cannot be reversed.
Pseudonymization - Provides false names for subjects.
Tokenization - Involves replacing sensitive data with a token that has no actual relation to the data it is replacing.

Due Care - Best defined as taking and making decisions that a reasonable and competent person would make. Helps shields and organization from liability should a breach happen.

Elasticity - The ability to automatically expand or contract resources according to demand. Used within virtual and cloud environments to support the peaks and valleys of service demands by allocation resources when they are needed.

Tape jukebox - Tape library, a device that can load and unload tape backups automatically.

Risk is viewed as the possibility that something could happen to damage, destroy, or disclose data or other resources.

Integrated development environment - A pre-created environment, composed of useful programs for the task at hand. Kali Linux that has red and blue teaming tools.
Dynamic link library - Functions meant to be used with a specific coding language for a specific purpose. Ex. Libraries for creating machine learning AI in Python.

ABAC - Most detailed form of AC and can take location, network, time of day, device, and even more.  More difficult to implement.

Compensating controls - Put in place to counter a weakness or vulnerability in a network. Used to "make up for" the lack of something else.

MITRE ATT&CK Matrix - Provides a step-by-step guide on how attackers exploit vulnerabilities and can be easily compared with the company's vulnerabilities.

DREAD - Rating system designed to provide a flexible rating solution that is based on the answers to five main questions about each threat:
Damage potential
Reproducibility
Exploitability
Affected users
Discoverability

BIA - Identify critical systems and prioritize assets that are most critical to the business. Includes qualitative and quantitative evaluations. 

802.1AE - MACsec that provides confidentiality and integrity at the data link layer.

Parallel test - Production processing is not interrupted or moved from the primary site.

Known-plaintext attack - Model for cryptanalysis where the attacker has samples of both the plaintext and its encrypted version. 

Buffer overflow attack - Occurs when an application buffer is populated with data that exceeds the capacity allocated to it, causing excess data to overflow into adjacent memory.
Memory leak - Describes the waste condition that results from an application that fails to release memory it has allocated but no longer needs.

SOC engagement reports increase in level. The greater involvement of people, the higher the level.

iSCSI - Used to transmit SCSI commands through TCP packets. Frequently found in SANs and allows a server to attach storage through Ethernet.

ATM - Cell-switching technology that is used for WAN connections. It fragments communications into fixed-length 53-byte cells. Allows ATMs to be efficient and offers efficient bandwidth.

Delphi - Brings focus groups into a room where they can anonymously provide feedback. Each group compiles its feedback on a piece of paper and submits it. The feedback is then presented to the groups and repeated until a consensus has been reached.

RAID-0 - Stripes data across multiple disks. Increases the change of failure, but increases the write and read speed.
RAID-1 - Mirrors data across multiple disks. Decreases the usable drive space by 50% and does not provide any write speed benefits.
RAID-5 - Stripes & adds a parity bit. Provides fault tolerance, but decreases write speeds.
     Parity means calculating the data in two drives and storing the results on a third one. Computed by XOR'ing a bit from drive 1 with a bit from drive 2 and stores it on drive 3.
RAID-10 - Stripes & Mirrors two sets. Provides fault tolerance, but decreases usable drive space by 50%.

RSA - Asymmetric algorithm that uses public and private keys.

802.15 Bluetooth
802.11n Wireless
802.3 ethernet for DSSS

Private networks:
10.0.0.0/8 = 10.0.0.0 - 10.255.255.255
172.16.0.0/12 = 172.16.0.0 - 172.32.255.255
192.168.0.0/16 = 192.168.0.0 - 192.168.255.255
.
KPI - Class of metric used to measure activity success. Enable performance to be tracked, trended, monitored, and prioritized or targeted for improvement. Ex: 'percent of system uptime'
KRI - class of metric used to measure exposure to potential harm. Ex: 'number of unplanned outages'.

Hardware segmentation - Higher trust levels often require hardware segmentation of memory. The memory becomes physically separated, not just logically separated.

Digital certificates contain public keys of a public-key infrastructure. PKIs use Cas to distribute digital certificates. 

Capacitance - Changes in the electromagnetic field around the sensor. Motion detection.

Scoping - Reviewing security controls and weeding out ones that are not applicable.
Tailoring - Changing the list of previously selected security controls.

Generation one - Machine Language
Generation two - Assembly Language
Generation three - High-level languages, such as C
Generation four - JavaScript and Python 

Misuse case testing - Used to help identify potential security flaws in a software's design.

Accountability - Ensures that the changes made to the system are logged and audited to ensure the integrity of the system.
Authorization - List of roles and permissions for a user.
Authentication - Ensures that a user has access to an object.

Direct evidence - May come from witnesses who give oral testimony based on their observations
Conclusive evidence - Irrefutable and cannot be contradicted.
Circumstantial evidence - Prove an intermediate fact used to assume another fact.
Corroborative evidence - Used to prove an idea or point that cannot stand on its own.

Clipping level - A threshold for the number of error occurrences before it's considered suspicious or sets off an alarm.

Synthetic transactions - Ensures that whatever text is expected comes out when requested. Good for testing code and validating input.

HSM - Dynamically manages data across different storage media to optimize for access speed or media cost. 

Forwarding table (CAM) overflow attack - When sending frames out interfaces. If the switch does not know what interface the destination MAC address is connected to, it will send the frame out of all interfaces except the source interface. Attackers can create thousands of MAC addresses that overflow the forwarding table.

Least privilege - Based upon limiting access and ability as determined by a subject's security clearance or permission group.
Need-to-know - More selective and determined by a task needed to be completed by a specific subject, even within a security clearance level.

SAML - XML-based language that is used to exchange authentication and authorization information between federated organizations. Used to provide SOO for browser access.

Fail-secure - Means of failing, but in a way to protect assets. Ex. Firewall failing and not allowing access to assets by default.
Fail-soft - Refers to something still allowing for operation in a reduced capacity. Ex. Door that opens based on a sensor and makes a noise upon entry.
Fail-closed - Closing all access. Ex. Bank vault automatically locking if a bank loses power. 

Breach and attack simulation (BAS) - System simulates and attack, exploiting and highlighting vulnerabilities to be remediated.

Responsible disclosure - The act of disclosing a vulnerability in a timely manner to the vendor.

M of N control is a multi-person and split knowledge control that requires a minimum number of individuals to provide credentials before action can occur.

Cryptology is the study of encrypting messages
Cryptanalysis is the method of breaking encryption.

Lattice-based - Model protects illegal information flow among entities. Subjects can only access objects as long as they are in the range of their lattice position. The object's classification and labels determine lattice positions.

White noise - A false traffic used to mask or hide the presence of real traffic. Includes a real signal mixed in with false information. 

Digital signature - A hash of the message that is encrypted with the sender's private key. Digital signatures assure the recipient that the message has not been tampered with during transmission by comparing the decrypted hash with the hash generated by the receiver.

IV is a random value used with a key to encrypt or decrypt data. Reduces the likelihood of the same plaintext patters being found in the ciphertext.

802.1X EAP-PEAP - Allows an admin to require endpoints to authenticate before network access is granted. EAP-PEAP uses a trusted certificate or requires valid credentials.

Multithreading - Type of processing allows multiple instruction sets to run in parallel under a single process.

Security Onion - A SIEM that logs network traffic and analyzes it in various ways.

Frame relay resides in data link layer and uses packet-switching technology to connect different WAN connections. Frame relay uses virtual circuits and data link connection identifiers to address to connect routers.

PGP is a hybrid cryptosystem that uses IDEA to encrypt the data. PGP then uses a web of trust instead of traditional PKI.

FIM - Management of a form of SSO that provides a solution for users accessing resources over the internet.

Weakest to strongest
ECB
CBC
CFB
OFB
CTR

Trust but verify - A secure design principle that challenge assumptions of trust derived from certain criteria without trust being explicitly verified.

Fagan inspection
Planning
Overview
Preparation
Inspection
Rework
Follow-up

Register - A temporary storage location located on the CPU. It is used to store instruction sets. When a CPU executes an instruction set, it loads it from the register.

CDN - A collection of different content that a website may display, distributed across geographical regions. Allows website creators to improve performance by providing a website's content in a geographical region closest to the client.

Fagan inspection - A formal step-by-step process of code review. It is considered the most-in-depth code review in the industry.

Diameter was developed after and inspired by RADIUS to overcome the limitations associated with compatibility among other authentication mechanisms. 

ISO 15408 = Common Criteria for Information Technology Security.

Surge - Prolonged increase in voltage.
Spike - Sudden but short increase in voltage.

CISSP Mindset
	1. Your role is Risk Advisor--DO NOT FIX PROBLEMS.
	2. Who is responsible for security? Senior management.
	3. How much security is enough? Depends on how valuable the asset is.
	4. All decisions start with risk management, which starts with Evaluating your assets. Includes things like data labeling and data classification. Quantitative and qualitative evaluation.
	5. Think "End Game" What ends up fixing things in the long term? Always think of policies.
	6. "Security Transcends Technology" No configuration, Don't look for purely technical solutions, think broad.
	7. Physical safety is always the first choice. Good for BCP, DRP, etc.
	8. Technical people-Stay out of the weeds. This is not a technical exam, this is a managerial exam. Think broad. Think what answer encompasses the entire question.
	9. Incorporate security into the design, as opposed to adding it on later. Know the software security steps. Always have security implemented.
	10. Layered Defense


Kerberos - A network authentication protocol designed from MITs project Athena. Tries to ensure authentication security in an insecure environment. Allows SSO. Uses Symmetric encryption.
     Authentication is the process to obtain ID verification of the user or service requesting access.
Components:
AS - Allows authentication of the user and issues a TGT. Often is a single point of failure.
TGS - After receiving the TGT from the user, the TGS issues a ticket for a particular user to access a particular service.
KDC - Runs the TGS and AS together.
Tickets: Means of distributing the session key.
Principles - users, applications, and services.
Main goal: user needs to authenticate himself/herself without sending passwords across the network --needs to prove he/she knows the password without actually sending it across the wire.

OpenID - A standard that allows an organization to leverage a third-party IDP to manage user identification and authentication.

Real-time Transport Protocol (RTP) - Media sharing protocol used to send and receive voice or video communications over an IP-based network.

Data Owner / Controller - Accountable for protection of data, holds legal rights and defines policies.
Data Processor - Responsible for processing data on behalf of the owner / controller (Processor is typically the Cloud Provider.)
Data Custodian - Technical responsibility for data (e.g. data security, availability, capacity, continuity, backup and restore, etc.)
Data Steward - Business responsibility for data (e.g. metadata definition, data quality, governance, compliance, etc.)
Data Subject - Individual to whom personal data relates.

Bell-LaPadula Model - Confidentiality
Simple Security Property - Allows you to read down but not up. NO READ UP 
Star Property *- - Allows you to write up but not down. NO WRITE DOWN
Strong Star Property - Allows you to Read & Write ONLY at your level.

Biba - Integrity
Simple Integrity property - Prohibits people from reading information below their clearance level. NO READ DOWN 
*-Integrity Property - Prohibits people from writing information above their clearance level. NO WRITE UP

Clark-Wilson - Integrity: Relies on the separation of duties and separation of subjects from objects.
Has three goals:
	1. Prevent unauthorized subjects from making any changes. (Same as Biba)
	2. Prevent authorized subjects from making bad changes.
	3. Maintain consistency of the system
Access triple - Which means subjects access and modify objects is indirectly done from an interface or program.

Brewer-Nash / Chinese Wall: Confidentiality: Prevents conflicts of interests.

Graham-Denning model - Rule-based model that specifies rules allowing a subject to access an object.

Harrison-Ruzzo-Ullman Model - Integrity. Focuses on the integrity of access rights via a finite set of rules available to edit the access rights of a subject.

Non-interference model - Prevents processes operating in different domains from affecting each other. Focuses on preventin higher-level security processes from negatively8 affecting the process of lower-level security. Used to address covert channels.

ISO 27001 - Information security management systems: International model for development and implementation of policies, procedures, and standards for ISMS appliances.
ISO 27002 - Information security controls: Describe specific controls to achieve control objectives.
ISO 27017 - Cloud security controls: Standards for cloud services, cloud customer information and privacy.
ISO 27037 - Digital forensics: Guide for collecting, identifying, and preserving electronic evidence. 
ISO 27050 - eDiscovery: Process of identifying and obtaining electronic evidence for prosecution. 
ISO 27701 - Privacy controls: Guide for managing privacy.
ISO 31000 - Risk management.

Due Care - Action taken during an instance: Takes the actions that a reasonable person would in the same situation. Actions we take in the moment. Incident response plan, modifying firewalls during intrusion.
Due Diligence - Prior planning: Puts governance structures in place to protect the organization's interests. Actions we take in before. Policies, procedures, standards, guidelines, etc.

BIA - Includes the most critical/essential business functions, processes, and systems. Includes potential impacts of an interruption as a result of a disaster. Has RPO, RTO, WRT, MTD.
Three steps:
Determine mission/business processes and recovery criticality
Identify resource requirements
Identify recovery priorities for system resources.

DRP - Focuses on the recovery of vital technology infrastructure and systems; tactical.
BCP - Focuses on survival of the business and the capability for an effective response; strategic.

BCP is all about being able to continue performing work and delivering services at an acceptable level - tied with SLAs. After an impacting incident takes place
DRP is all about documenting a specific set of activities that will need to take place so an organization is able to recover from an incident and resume normal operations. Return to normal state.

Read-through test - Author reviews DR plan against standard checklist for missing components/completeness.

Walkthrough test - Relevant stakeholders walk through the plan and provide their input based on their expertise.

Simulation Test - Follow a plan based on simulated disaster scenario.

Parallel test - Test DR plan at recovery site/on parallel systems. Includes performing all steps of a real recovery, except that you keep the live production systems running in the original location during the test..

Full-interruption - Cause an actual disaster and follow DR plan to restores systems and data.

SCA - Goals are to verify security, assess the effectiveness of security, and identify the strengths and weaknesses of security.

VAST - Visual, agile, and simple threat for agile programming concepts to conduct threat modeling.

International Traffic in Arms Regulation (ITAR) - U.S. regulation that restricts and controls the export of defense and military technologies to foreigners.

Class A - Wood or paper
Class B - Liquids like fuels and oils
Class C - Electrical
Class D - Metal 

EDR - A protection solution commonly deployed on endpoints to detect APTs. 

ISAE 3402 - Covers security audits on an international scale outside the U.S.: Creates SOC audits between organizations.

Real user monitoring (RUM) - Analyzes the traffic or status of transactions for real user traffic. Provides real time updates on the status of user interactions for a given service.
Synthetic monitoring - Completes transactions against a website to track website performance, such as refreshing a page to count response time or inputting various user input to tally outputs.

COBIT - A framework for governance. Best set of best IT security practices. Based on meeting stakeholder needs, covering enterprise end-to-end, apply an integrated framework, enables holistic approach, separates governance from management.
Meeting stakeholder needs
Covering the enterprise end to end
Applying a single integrated framework
Enabling a holistic approach
Separating governance from management

Zero-knowledge proof - Allows one party to demonstrate knowledge of a secret without actually disclosing that secret to the other party. Common in cryptography to validate passwords and keys.

Abuse case testing - A test to determine if a website, its hardware, software, and their interactions with one another have security vulnerabilities which could be used by attackers
Stress testing - Focus is putting a piece of hardware or software under stress to ensure it meets the acceptable standards and demands of customers.
Misuse case testing - Used to test common user misuse testing.

Software assurance maturity model - Includes Governance, design, and verification. 

Policy - Defines the scope and enforcement of security within an organization
Standards - Mandatory rules for a given subset of technology.
Guidelines - Recommended steps for a given subset of technology
Procedures - Step by step tasks that should be performed for a given subset of technology.

Capability Maturity Model - Offers a structured approach that allows and organization to measure processes and understand where strengths and room for improvement exist. 
Initial - marked by new or unrefined processes
Repeatable - the ability to repeat processes
Defined - Well-documented processes
Managed - Metrics
Optimized - Processes are continually improved using tools
 
Accountability - Where the buck stops. Have ultimate ownership, answerability, blameworthiness, and liability
Responsibility - The doer. In charge of task or event. Multiple entities can be responsible. Develops plans, make things happen.

Responsibility 

LDAP - Open and cross platform protocol used to authenticate to directory services, such as AD and query them. Used to manage and access information stored in a directory. 

BCP - Allows for businesses to continue due to prior planning. 
DRP - No disaster. 

Physical order:
Deterrence
Preventive
Detective
Compensating 

Skipjack - Symmetric with a Clipper chip. Part of an escrowed FIPS publication. Divides a secret key into two parts and places them into a key escrow.

Permanent virtual circuits - Can always exists and can be used at any time by the customer.
Switched virtual circuits - Dial-up connection and is temporary.

The act of bypassing the native security restrictions is rooting.

ACL - Table that includes subjects and assigned privileges. Bound to a specific object.
ACM - A table that shows which subjects are granted to which resources. Shows multiple levels of access for each subject.

KISS principle - Keep it simple stupid, used to keep universal truth of vulnerabilities. Keep it simple.

Unit Testing - Examines and tests individual components of an application.
Interface testing - Standardized, defined ways that units connect and communicate with each other. Verifies components that connect.
Integration testing - Focuses on testing component groups (groups of software units) together.
System testing - tests the whole system.

Positive Testing - Focuses on the response of a system, based upon normal usage and expectations. Ex: correct username and password.
Negative Testing - Focuses on the response of the system when normal errors are introduced. Ex: incorrect username and password.
Misuse Testing - Outside perspective trying to break or attack the system. Break into or abuse.

Equivalence partitioning - Inputs are divided (partitioned) into groups that exhibit the same behavior with test cases covering each partition.
Boundary value analysis - Focus on testing data at the boundaries. Extreme ends of the input values.

Decision Table Analysis - Different input combinations and their corresponding system behavior/output are captured in a table.
State-Based Analysis - A set of abstract states that a unit of software can take are defined, and then tests compare its actual state to the expected state. Useful for testing GUIs and communication protocols.

Vulnerability assessment 
Reconnaissance - Gather public information
Enumeration - Actively enumerate the target - IP addresses and ports. Network discovery.
Vulnerability Analysis - Identify potential weaknesses to be exploited.
Execution - Attempt to exploit weaknesses.
Document findings - Identify the severity of findings and report them to the appropriate audience.

Banner grabbing helps identify software and versions.
Fingerprinting looks at how the packet is formed.

CVE - List of security flaws and vulnerabilities that are publicly disclosed for awareness and risk mitigation
CVSS - Framework that uses common vulnerability metrics and characteristics to score.

Operational testing 
Real User Monitoring - A passive monitoring technique that monitors user interactions and activity with a website or application.
Synthetic Performance Monitoring - Used to test functionality and performance under load. Runs scripted transactions to monitor functionally, availability, and response times.

KRI - Forward-looking indicators and risk-related decision-making.
KPI - Backward-looking indicators and looks at historical data for evaluating the performance.
SMART, Specific, Measurable, Achievable, Relevant, Timely

ISAE 2402 - International standard in assurance engagements and is quite similar to SSAE 16/18.

Grid Computing - Distributed across hundreds and thousands of nodes across the internet. Nodes check-in when they have available system resources. Used for things like bitcoin mining, rainbow tables, and predicting weather patterns.

Remote journaling - A type of backup system where the transfer of data happens closer to real-time. Only transmits file deltas to keep systems synchronized.

VLAN hopping - Occurs when an attacker manipulates a frame, so the switch moves it to a different VLAN. This happens when spoofing a switch, setting up a dynamic trunk or tagged interface, or creating a double-encapsulated 802.1Q tag. 
     Mitigation - Disable dynamic trunk or tagged interfaces and use separate VLANs for access interfaces.

A thread is an individual instruction set that must be worked on by the CPU.

Threat - Something that can take advantage of the vulnerability, such as a thief.
Vulnerability - Latent weakness in a system that can be exposed by a threat.
Impact - Monetary effect that will occur, or it can be expressed as the impact to human health.

BIA - Tools used to help understand the criticality of assets within an organization.

Management Controls - Polices, Standards, Processes, Procedures, & Guidelines
Operational Controls - Execution of Policies, Standards & Process, Education & Awareness

Multitasking - Execute more than one task at the same time.
Multiprocessing - More than one CPU is involved.
Multi-threading - Execute different parts of a program simultaneously. 

Security Kernel - Made up of software, hardware, and firmware

Presentation  layer deals with transforming data into structures that other systems can understand. Ex: JPEG, MPGEG, ASCII, and GIF.

Abstraction - A principle that is commonly applied to simplify security-related management activities, such as permissions assignment. Simplifies complex sets through the grouping of similar, fundamental elements.

Covert Channel - Disclosure of information in an unauthorized manner.
Storage - Exchanges information by writing data to a common storage medium that another process can read.
Timing - Exchanges information through the use of timing. Shared resource that is used or not used.

Third-party audit - Relates to an audit conducted on behalf of another firm.

Domain controller - What a user must authenticate with in Microsoft AD. Checks the credentials entered by the user to ensure they match what is stored within the directory.

Nmap 
Open - Port is open accepting connections.
Closed - Port is accessible but not accepting connections.
Filtered - Unable to determine if the port is open or closed due to a firewall.

NDAC is centrally administered. Admins can make changes that affect the entire environment.

Frame relay uses the data link layer and uses packet-switching technology to connect different WAN connections.

Heartbeat sensor - A communication pathway that tests a target's signal periodically.

Trademarks protect brand identity, including slogans, logos, phrases, or combinations representing the company or brand identity.

Tokenization - The technique of mapping sensitive data elements to, and replacing them with, an identifying token that is not itself sensitive if revealed.
Anonymization - The technique of removing the fields in a data set which associate that data with a particular person so that the balance of data in that set can be analyzed and shared without any risk to the privacy of those from whom the data was collected.

Runtime - Having all the hardware and software needed to properly run an application in an environment.

Type 1 - Something you know
Type 2 - Something you have
Type 3 - Something you are

Provisioning - Process of user account creation and permissions assignment.
Onboarding - Refers to a collection of activities performed by new hires to meet legal or policy compliance, and orient the employees to the policies and processes of the organization.

BCP NIST
Develop a contingency planning policy statement - A formal policy provides authority and guidance necessary to develop an effective contingency plan.
Conduct a BIA - Prioritize information systems and components critical to supporting the orgs mission/business functions. 
Identify preventive controls - Measures take to reduce the effects of system disruptions to increase system availability and reduce contingency life cycle costs.
Create contingency strategies - Through recovery strategies ensure that the system may be recovered quickly and effectively.
Develop an information system contingency plan - Contain detailed guidance and procedures for restoring a damaged system.
Ensure plan testing, training, and exercise - Testing that validates recovery capabilities.
Ensure plan maintenance - Living document that is regularly updated with current system enhancements and organizational changes.

Strategic plans - Long-term plans. Ex. Create disaster recovery location within five years.
Tactical plans - Cover shorter amount of time. Ex. Install servers in the third quarter and set up backups in the fourth quarter.
Operational plans - Short, detailed plans. Ex. Use NFS with a storage are network to attach storage to the servers next week.

MTTF - Devices or components that fall into this use MTTF. 

COBIT - Manages control variables within IT and how they align with business practices.

Database - A collection of information or data for search and retrieval purposes.
Schema - Data from where formal definitions of every object are created.

Software capability maturity model - based on the principle that a mature software development process will produce quality software.

IKE - Used to negotiate parameters and ultimately established security associations for IPsec.

Runtime application self-protection (RASP) - Security application that ensures all software runs as it should and does not execute behavior that may be malicious. Digs into the code associated with the program, views what is set to occur at runtime, and determines if it's malicious.

Privacy Act of 1974 - Restricts the way the government can use private information. Defines exceptions such as the census, law enforcement, and health and safety.

SOD - Allows for two or more people to play separate roles in the completion of a critical process.
Dual Control - involves two or more people serving one specific function.

EOS - Term used to describe a product or solution that is no longer actively supported by its manufacturer.
EOL - Term used to describe a product or solution that is no longer actively sold by its manufacturer.

Security incident - Any event that negatively impacts an organization's security posture or may lead to the eventual disclosure of sensitive information. 
Data breach - Event that results in the disclosure of sensitive information.

Ring architecture model:
Applications (3)
Hardware Drivers (2)
Operating System (1)
Kernel (0)

Threat modeling - The security process wherein potential threats to assets are identified and analyzed.

Hierarchical model is one-to-many data model which forms a logical trees structure.
Relational model is one-to-one data model.

ABAC - A system that uses attributes of the subject, object, or action to define access. More specific than RBAC. Attributes can include location, time of day, security clearance, etc.

SCRM (Supply Chain Risk Management) - A structured approach to managing resiliency in the sourcing of components and materials.

RFC 1087 - Statement of policy published by the IAB which promotes responsible use of the internet and characterizes five categorizes of activity as unethical.

Anonymization - Technique of removing the fields in a data set which associate that data with a particular reason.

DCS - A network of PLCs. Process-specific.
SCADA - System that controls multiple processes and can span large geographical areas.

Failover - Refers to any scenario in which standby equipment automatically takes over when the primary system fails.

Capacitance motion detector - Contains an electromagnetic field surrounding the device.

PCI has 12 main requirements.

Multiprocessing - The parallel execution of instructions.
Multithreading - Sharing of a single CPU between multiple tasks.
Multiprogramming - The execution of two or more programs by a single computer.
Multitasking - Processing of more than one task at a time. 

LDAP - A directory service is a centralized database that includes information about subjects and objects. AD is used commonly here.

Access control matrix - A table that contains a list of subjects, objects, and permissible actions.
Access control list - The columns.

Reasonableness check - Ensures that data outputted from software fails within the specified boundaries.

FISMA - Requires that federal agencies implement an information security program that covers their operations. Requires that government agencies include the activities of their contractors in the security management programs.

WEP uses TKIP
WPA uses RC4
WPA2 uses AES

EAP - A framework for authentication rather than a standalone authentication protocol. Used to negotiate the best authentication protocol. 

BCP - Seeks to allow a business to continue.
DRP - A plan involving a backup site. Business has ceased and the main job is to bring the business back up as soon as possible.

Formula for residual risk - Threat x vulnerability x asset value - control gap

e-Discovery - A term used to describe the process of identifying and producing electronically stored information requested by a court subpoena.

Geofencing - Used to restrict access based on location. 
Geotagging - The ability of a mobile device to incorporate time, date, and location data into the metadata of media.

SSH provides end-to-end encryption and exchange keys using Diffie-Hellman.

Smurf attack - Spoofs the source IP address with the victim's address and floods the broadcast address with ICMP requests.

A nonce is a random number or value generated by the authentication server. It is a challenge. Nonces are used to add replay resistance.

ALU - A series of physical circuits that perform bitwise operations on binary numbers. They are used to make calculations using logic gates.

The Open Group Architecture Framework (TOGAF) - A standard that helps organizations design, plan, implement, and govern information technology architecture.

M of N control - Requires that a minimum number of authorized users (M) be present out of all authorized users (N) before performing a function. 

Tailoring - Modifying standards in place to meet the needs of the current business.

Software escrow - Process when a third party maintains the source code in the event that a customer needs it when a vendor or company that initially developed the code no longer exists.
Code repository - Concerned with holding code in an air-gapped network for the purposes of protection.

Deluge fire suppression - Water suppression system.

Criminal - Deals with crimes and includes legal punishment.
Civil - Disputes between individuals or organizations.
Regulatory - Violations of regulated activities.
Administrative - Focus on internal violations of organizational policies.

Interface - The logical or physical point where two systems or a user interact with each other.

DRP should be initiated when IT is no longer able to support a mission-critical process.

Type 1 - A valid user is falsely rejected by the system
Type 2 - An invalid subject is authenticated.

PASTA - Process for Attack Simulation and Threat Analysis. Focuses on countermeasures based on asset values.

Compensating - Used to provide alternatives to aid in security enforcement. They are used in addition to main security controls. Used to reduce risk to an acceptable level when the main control is too expensive or restrictive. 

Due Care - Proactive. What actions should I take in the moment
Due Diligence - Before. What documentation is there?

Credential management systems - Provides a secure location where uses can store their usernames and passwords for resources such as websites, network files, and software.

Least privilege - Used to ensure that subjects are granted only the privileges they need to perform their work tasks and job functions.

BCP is focused on keeping business operations going even if an incident occurs.
DRP is focused on the recovery of systems after a disaster has occurred. 

POP3 - Used to pull email messages from an email server to an email client's inbox.
SMTP - Primarily used to transfer email between servers.

Homomorphic encryption - A unique type of encryption which supports the ability to perform computations on its encrypted data fields.

Computer Fraud and Abuse Act - Implemented penalties against those who perpetrate and spread viruses, worms, and other malicious software intended to harm computing systems.

DSSS - Modulation technology that increases bandwidth and adds redundancy by adding sub-bits to messages.

AH - Provides integrity of the packet and adds an AH header.
ESP - Provides confidentiality of the packet and adds an ESP header.

IKE has two modes:

Main mode - uses a six-way handshake where parameters are exchanged in multiple rounds with encrypted key exchange.
Aggressive Mode - Uses a three-way handshake where the hashed PSK is sent unencrypted. 

SSAE 18 and ISAE 3402 is used for External and third-party audits of companies.

Access control matrix - A table that lists objects, subjects, and their privileges.
Access Control List - Focuses on objects and which subjects can access them.
Capability table - Lists subjects and what objects they can access.

Fagan inspection - Highly formalized review and testing process that uses planning, overview, preparation, inspection, rework, and follow-up steps.

Data controller - Create and manage sensitive data within an organization. Ex. HR employees create and manage data such as salary and benefit data, reports, etc.
Data processors - Manage data on behalf of data controllers. Ex. A third party manages the payroll data on behalf of the data controller.

Certification - Means a system has been certified to meet the security requirements of the data owner.
Accreditation - The data owner's acceptance of the certification and of the residual risk, which is required before the system is put into production.

ISO 17799 - Broad-based approach for the information security code of practice by the ISO
COBIT - Control framework for employing information security governance best practice within an organization.
ITIL - Framework for providing best services in IT Service Management.

Scoping - The process of determining which portions of a standard will be employed by an organization. Ex. An org that does not employ wireless equipment may declare the wireless provisions of a standard are out of scope and therefore do not apply.
Tailoring - The process of customizing a standard for an organization. It begins with controls section, continues with scoping, and finishes with the application of compensating controls.

Clark-Wilson - Integrity. Requires subjects to access objects via programs. Has well-formed transactions and separation of duties.
Brewer Nash / Chinese Wall - Designed to avoid conflicts of interest.

Security domain - The list of objects a subject is allowed to access.
Domains - Group of subjects and objects with similar security requirements.

CPU ring model
Ring 0: Kernel
Ring 1: Other OS components that do not fit into Ring 0
Ring 2: Device drivers
Ring 3: User applications

Open systems - Uses open hardware and standards from different vendors.
Closed system - Proprietary hardware or software.

ALU - Performs mathematical calculations; fed instructions by the control unit.

Pipelining - Combines multiple CPU steps into one process, allowing simultaneous FDX and write steps for different instructions.
Interrupt - Indicates that an synchronous event has occurred.

Process - an executable program that is associated data loaded and running in memory.
Thread - A lightweight process  that are able to share memory.

Multitasking - Allows multiple tasks to run simultaneously on one CPU.
Multiprocessing - Runs multiple processes on MULTIPLE CPUs.

CISC (Complex instruction set computer) Uses a large set of complex machine language instructions
RISC (reduced instruction set computer) Uses a reduced set of simpler instructions.

Swapping - Uses virtual memory to copy contents of primary memory (RAM) to or from secondary memory (not directly addressable by the CPU, on disk).

Kernel - Provides the interface between hardware and the rest of the operating system, including applications.

Reference monitor - Mediates all access between subjects and objects. Enforces the system's security policy. Ex. Preventing a normal user from writing to a restricted file.

IaaS - Provides an entire virtualized operating system, which the customer configures from the OS on up.
PaaS - Provides a preconfigured operating system and the customer configures the applications.
SaaS - Completely configured, from the operating system to applications, and the customer simply uses the application.

Grid computing - Represents a distributed computing approach that attempts to achieve high computational performance by nontraditional needs.

P2P - Any system can act as a client, a server, or both, depending on the data needs.

Packers - Provide runtime compression of executables.

Applets - Small pieces of mobile code that are embedded in other software such as web browsers.

XML - Markup language designed as a standard way to encode documents and data. Can be used to store application configuration and output from auditing tools.
EXML - Allows users to define their own data formats.

SOA - Attempts to reduce application architecture down to a functional unit of a service. Intended to allow multiple heterogeneous applications to be consumers of services.

Polyinstantiation - Allows two different objects to have the same name. Two rows may have the same primary key, but different data.

Aggregation - Collection of public information or less sensitive data. Accumulation of data.
Inference - Interpretation of data using deduction.

Diffusion - Means the order of the plaintext should be dispersed in the ciphertext.
Confusion - Means that the relationship between the plaintext and ciphertext should be as confused or random as possible.

Substitution - Replaces on character for another. Ex. C becomes %. Confusion involves substitution
Transposition or Permutation provides diffusion by rearranging the characters of plaintext. Ex. 'ATTACKATDAWN' 'CAAKDTANTATW'.

XOR - Combines the key with a plaintext via XOR to create ciphertext.

Digital signatures - Provides authentication and integrity, but not confidentiality.

Known Plaintext - Relies on recovering and analyzing a matching plaintext and ciphertext pair. Goal is to derive the key that was used.
Chosen Plaintext - Attacker chooses the plaintext to be encrypted in a chosen plaintext attack. 
Chosen Ciphertext - Attacker chooses the ciphertext to be decrypted. Usually used against asymmetric cryptosystems, where the attacker may choose public documents to decrypt that are signed with the users private key.

Differential cryptanalysis - Seeks to find the difference between related plaintext that are encrypted.
Linear cryptanalysis - Known plaintext attack where the cryptanalysis finds large amounts of plaintext/ciphertext pairs created with the same key.

Side-channel attacks - Uses physical data to break a cryptosystem, such as monitoring CPU cycles or power consumption used while encrypting or decrypting.

Digital certificate - A public key signed with a digital signature. Provides mutual authentication and encryption. Standard is X.509.

AH - Provides authentication and integrity for each packet of network data. Protects against replay attacks.
ESP - Provides confidentiality by encrypting packet data. Also may provide authentication and integrity.
IKE - Negotiates the algorithm selection process.

PGP - Provides the modern suite of cryptography. Used to encrypt emails, documents, or an entire disk drive. Uses a web of trust model to authenticate digital certificates. 

Blackout - Prolonged loss of power
Brownout - Prolonged low voltage
Fault - Short loss of power
Surge Prolonged high voltage
Spike - temporary high voltage
Sag - Temporary low voltage

Humidity = 40 to 60 percent'
High humidity allows the water in the air to condense onto and into equipment, which may lead to corrosion
Low humidity allows static.
Temperature - 68-77F

Ionization - contain a small radioactive source that creates a small electric charge.
Photoelectric - Contain LED and generates a small charge while receiving light.

DNP3 (Distributed network protocol) - Provides an open standard used primarily within the energy sector for interoperability between various vendors.

Frequency-hopping spread spectrum (FHSS)  -  Uses a number of small frequency channels throughout the band and "hops" through them in pseudorandom order.
Direct-sequence spread spectrum (DSSS) - Uses the entire band at once, "spreading" the signal throughout the band.

Asynchronous - Type of token-based authentication system that uses a challenge/response process in which the challenge has to be entered on the token.

Software escrow agreement - Place a copy of the source code for a software package in the hands on an independent third party who will turn the code over to the customer if the vendor ceases business operations.

False rejection - Occurs when an authorized subject is rejected by the biometric system as unauthorized. Type 1.
False accept rate - When an unauthorized subject is accepted as valid. Type 2.

Authentication - Proving an identity claim.
Authorization - Actions-authenticated subjects are allowed to perform on a system.
Accountability - The ability to audit a system and demonstrate the actions of subjects.

FIdM - Applies SSO on a wider scale.

SAML - XML-based framework for exchanging security information, including authentication data.

Penetration Tester methodology
Planning
Reconnaissance
Scanning 
Vulnerability assessment
Exploitation
Reporting

Identification - The process of a subject claiming, or professing, an identity. A subject must provide an identity to a system to start the authentication, authorization, and accountability processes.

Atomicity - Ensures that if any part of a database transaction fails, the entire transition must be rolled back as if it never occurred
Isolation - Requires that transactions operate separately from each other.
Consistency - Ensures that all transactions are consistent with the logical rules of the database.
Durability - Requires that once a transaction nis committed to the database it must be preserved.

CDN - Designed to provide reliable, low-latency, geographically distributed content distribution.

Release control - The process of ensuring that the processes includes acceptance testing and confirms that any alterations to end-user work tasks are understood and functional prior to code release.

PGP - Provide strong encryption of files, which can then be sent via email.

Traceability matrix - Used to map customers' requirements to the software testing plan. Traces the requirements and ensures that they are being met.

Synthetic transactions / monitoring - Involves building scripts or tools that simulate activities normally performed in an application. Used to establish expected norms for the performance of transactions.

Unit testing - Low-level tests of software components, such as functions, procedures, or objects.
Installation testing - Testing software as it is installed and first operated.
Integration testing - Testing multiple software components as they are combined into a working system. 
Regression testing - Testing software after updates, modifications, or patches.
Acceptance testing - testing to ensure that the software meets the customer's operational requirements.

Combinatorial software testing - Black-box testing method that seeks to identify and test all unique combinations of software inputs.
Misuse case testing - Leverages use cases for applications, which spell out how various functionalities will be leveraged within an application.

Interface testing - Primarily concerned with appropriate functionality being exposed across all the ways users can interact with the application.

Breach and attack simulation (BAS) - Useful for preparing for a security audit. The system simulates an attack, exploiting and highlighting vulnerabilities to be remediated prior to an official audit.

MITRE ATT&CK Matrix - Provides a step-by-step guide on how attackers exploit vulnerabilities and can be easily compared with the company's vulnerabilities.

RUM - An approach to web monitoring that aims to capture and analyze every transaction of every user of a website application. 
Synthetic performance monitoring - Involves having external agents run scripted transactions against a web application.

ISAE 3402 covers security audits on an international scale outside of the U.S.

Microsoft SQL Servers use TCP ports 1433 and 1434

Third-party audit is conducted by someone outside the target organization that can be fair, impartial, and transparent in the process.

Least privilege - Dictates that persons have no more than the access that is strictly required for the performance of their duties.
Need-to-know - Primarily associated with organizations that assign clearance levels to all users and classification levels to all assets; restricts users with the same clearance level from sharing information unless they are working on the same effort. Entails compartmentalization. 
Separation of duties - The practice of ensuring that no organizational process can be completed by a single person; forces collusion as a means to reduce insider threats.
Rotation of duties - Provides an organization with a means to help mitigate the risk associated with any one individual having too many privileges.

Allocated space - Portions of a disk partition that are marked as actively containing data.
Unallocated space - Portions of a disk partition that do not contain active data. This is where 'file deletion' happens.
Slack space - Data that is stored in specific-sized chunks known as clusters. This is the leftover space
'bad' Blocks/cluster/sectors - Sectors that cannot be read due to some physical defect.

eDiscovery - Pertains to legal counsel gaining access to pertinent electronic information during the pretrial discovery phase of civil legal proceedings.

PDRMRRRL
Preparation -  Steps taken before an incident occurs. Includes training, writing incident response policies and procedures, and providing tool such as laptops with sniffing software, crossover cables, original OS media, removable drives, etc.
Detection - Phase in which events are analyzed in order to determine whether the events might compromise a security incident.
Response - Incident response team begins interacting with affected systems and attempts to keep further damage from occurring. Ex. Taking a system off the network, isolating traffic, powering off the system. Forensic copy is made.
Mitigation - The process of understanding the cause of the incident so that the system can be reliably cleaned and ultimately restored to operational status later in the recovery phase.
Reporting - Begins immediately upon detection of malicious activity. Includes both technical and nontechnical reporting.
Recovery - Cautiously restore the system and continue to closely monitor it in production.
Remediation - Vulnerabilities are remediated.
Lessons learned - Provide a final report of the incident, which will be delivered to management.

Root-cause analysis - Attempts to determine the underlying weakness or vulnerability that allowed the incident to be realized.

Change management process:
Identifying a change
Proposing a change
Assessing the risk associated with the change
Testing the change
Scheduling the change
Notifying impacted parties of the change
Implementing the change
Reporting results of the change implementation


SLA - Stipulates all expectations regarding the behavior of the department or organization that is responsible for providing services and the quality of those services. Ex. Bandwidth, time to delivery, response time, etc.

RAID review:
Mirroring - Achieves full data redundancy by writing the same data to multiple hard disks.
Striping - Focuses on increasing read and write performance by spreading data across multiple hard disks.
Parity - Achieves data redundancy without incurring the same degree of cost as that of mirroring in terms of disk usage and write performance.

RAID 0 Striped set
Employs striping to increase the performance of read and writes. Offers 0 data redundancy.

RAID 1 Mirrored set
Creates/writes and exact duplicate of all data to an additional disk.

RAID 5 Striped set with distributed parity
Distributes the parity information across multiple disks. Good for disk cost and redundancy.

RAID 6 Striped set with dual-distributed parity
Can allow for the failure of two drives and still function.

RAID 1 + 0 Stripped and Mirrored set

Active-active HA cluster - Actively processes data in advance of a failure. Used commonly for load balancing.
Active-passive - Or hot standby configuration. Backup systems only begin processing when a failure is detected.

BCP Goal - Focus is on the business as a whole, ensuring that critical services or functions the business provides or performs can still be carried out in the wake of a disruption and after a disruption. Strategic
DRP Goal - Short-term plan for dealing with specific IT-orientated disruptions. Tactical

Hot site has all of the necessary hardware and critical applications data mirrored in real time. Recovery in a few hours.
Warm site - Has readily accessible hardware and connectivity, but relies upon backup data in order to reconstitute a system after a disruption.

BCP - Provide procedures for sustaining essential business operations while recovering from a significant disruption. 
DRP - Provide detailed procedures to facilitate recovery of capabilities at an alternative site. 
BRP - Provide procedures for recovering business operations immediately following a disaster.
COOP - Provide procedures and capabilities to sustain an organization's essential, strategic functions at an alternate site for up to 30 days.

Incremental backups - Archive data that have changed since the last full or incremental backup.
Differential backups - Archive data that have changed since the last full backup

FIFO (First In, First Out) Only maintains 14 days of data. You use each tape in order and cycle back to the first tape.
GFS- A son tape graduates to father then a father graduates to a grandfather after a set time. Creates data from the past 7 days, weekly tapes for the past 4 weeks, and monthly tapes for the past 12 months.

Electronic vaulting - The batch process of electronically transmitting data that is to be backed up on a routine, regularly scheduled time interval. Used to transfer bulk information to an offsite facility. 
Remote journaling - A database journal that contains a log of all database transactions. Saves the database checkpoints and database journal to a remote site.

Sashimi Model - Has highly overlapping steps; successor to the waterfall model. Based on the hardware design model. Like waterfall but includes explicit overlapping.

Spiral model - Software development model designed to control risk. Repeats steps of a project, starting with modest goals, and expanding outwards in ever-wider spirals called rounds. Risk analysis is performed each round.

Software escrow - Describes the process of having a third-party store an archive of computer software. Often negotiated as part of a contract with a proprietary software vendor. 

API - Allows an application to communicate with another application or an operating system, database, network, etc. 

Configuration management tracks changes to a specific piece of software.

DevOps - The practice of operations and development engineers participating together in the entire service lifecycle, from design through the development process to production support.

Database - A structured collection of related data. Allows searches, updates, deletions, and more.

Relational database - Contain two dimensional tables, or relations, of related data.

Referential integrity - Every foreign key in a secondary table matches a primary key in the parent table.
Semantic integrity - Each attribute value is consistent with the attribute data type.
Entity integrity - Means each row has a unique primary key that is not null.

Database normalization - Seeks to make the data in a database table logically concise, organized, and consistent. Removes redundant data and improves the integrity and availability of the database.

DDL - Used to create, modify, and delete tables.
DML - Used to query and update data stored in the tables.

Oop - Combines data with functions in an object-oriented framework. Used to manipulate the objects and their data.

Database replication - Mirrors a live database, allowing simultaneous reads and writes to multiple replicated databases by clients.
Shadow database - Mirrors all changes made to a primary database, but clients do not access the shadow. It is one way with shadow databases.

Polymorphism - Can change behavior based on the context of the input, overloading the + to perform addition or concatenation, depending on the context.
Polyinstantiation - Two objects with different data.

Software Capability Maturity Model (CMM) - A maturity framework for evaluating and improving the software development process. Main goal is to develop a methodical framework for creating quality software that allows measurable and repeatable results.
Initial - First stage. Few processes are defined
Repeatable - Project management processes are established to track cost, schedule, and functionality.
Defined - Software process for both management and engineering activities is documented, standardized, and integrated into a software process.
Managed - Measures how the software process and product quality are collected, analyzed, and used to control the process.
Optimizing - Continual process improvement with quantitative feedback from the process and from piloting innovative ideas.

Acceptance testing - Examines whether software meets various end-state requirements. A formal testing with respect to user needs, requirements, and business processes.

CSRF - Allows a third party to redirect static content within the security context of a trusted site.
XSS - A third-party execution of web scripting languages, such as JavaScript, within the security context of a trusted site.

Data processor - A third-party legal entity or agency that handles the data given to them by a data controller.

Difference between hacking and penetration testing: Permission.

Policy is a high-level document with high-level language written by senior management. Mandatory
Standards - Presents a uniformed and efficient managed enterprise. Ex: Windows 
Guidelines - Not enforced. Suggestions.
Procedures - Detailed step-by-step instructions.

If you need to know why you have to do something within a company, look at policies. If you need to know what configurations are mandatory, check standard. If you need to know how to do something, check procedures. For all other helpful suggestions and best practices, check guidelines.

CISSP exam wants a manger to think at a high level to make sure the proper processes are in place before any action or procurements are started.

SYN flood - Uses TCP SYN/ACKS to flood CPU memory
Smurf Attack - Uses ICMP replies. Echo Request ICMP floods the victim.
Fraggle Attack - Uses UDP
Ping Flood - Echo Request packets 

Tokenization - Meaningless data that represents meaningful data. It's a way to use random string of characters to represent actual private data.
Anonymization - The process of removing all relevant data so that it is impossible to identify the original subject or person.
Pseudonymization - The process of using pseudonyms (aliases) to represent other data.
Obfuscation - Re-arranging the letters of a word or converting from ASCII to ANSI format.

Digital signatures do not provide confidentiality.

Due diligence - Actions such as disablign personal USB drives, conducting background checks, having security guards, etc. All of it is prior to something happening. It is a methodical approach to choosing and customizing appropriate risk-based due care security controls.

Pocket Prep:
Security Assessment and Testing - 76/115 66%
Identity and Access Management (IAM) - 89/124 72%
Security Architecture and Engineering - 120/166 72%
Communication and Network Security - 91/125 73%
Asset Security - 69/94 73%
Security Operations - 93/125 74%
Software Development Security - 79/104 76%
Security and Risk Management - 118/147 80%
