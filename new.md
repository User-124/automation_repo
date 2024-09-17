 
COIT20246 PROJECT
Project specification
 
 
Table of Contents
1	Introduction	2
2	Task: Network design	2
2.1	Assumptions and requirements	2
2.2	Network Topology:	4
3	Cloud services	7
3.1	Pricing for cloud services	7
3.2	Comparison of Backup Strategies	10
4	Security	12
4.1	Conduct cyber security risk assessment	12
4.2	Recommend security controls	16
5	Project management	18
5.1	Project plan	18
6	Project reflection	19
7	References	22

List of figures
Figure 1 Network diagram	5
Figure 2 AWS pricing	9
Figure 3Azure pricing	9
Figure 4 TVA matrix	16
Figure 5 Vulnerabilities	16

 
1	Introduction 
In the realm of networking and cybersecurity, the task of designing a robust infrastructure for a small manufacturing company is both a challenge and an opportunity. This project delves into the intricacies of creating a network that harmoniously integrates factory machinery, office operations, and security systems while harnessing the potential of cloud services. The scenario unfolds in a single location comprising a small factory with network-controlled machinery, an office building housing sales and administration, and the imperative need to safeguard intellectual property. This study aims to analyze several intricate elements of risk assessment, strategic security measures, and meticulous design in order to propose a comprehensive framework for a network architecture that ensures both security and efficiency.
2	Task: Network design 
2.1	Assumptions and requirements
Assumptions:
1.	Network Traffic: The network will need to handle a variety of traffic types, including data transfer for engineering designs, financial data, internet access for office staff, and real-time monitoring and control of machinery in the factory.
2.	Cloud Services: The company will continue to use cloud services for functions like hosting their website and email services.
3.	Security: The company is concerned about security and plans to use IP-based security cameras for monitoring. They want the video streams stored locally for security purposes.
4.	Subnetting: The company has requested at least three different IP subnets, one for the factory, one for the office, and one for the security cameras, all using /24 or /16 network masks.
5.	Mixed Growth: The network should be scalable to accommodate potential future growth in terms of devices and network services.
6.	Data Privacy: Protecting the intellectual property, especially engineering designs and financial data, is crucial for the company.
Requirements:
1.	IP Subnets: At least three separate IP subnets, as requested by the company: one for the factory, one for the office, and one for the security cameras. Additional subnets may be used if justified.
2.	Network Topology: Create a network topology that efficiently connects the factory, office, and security cameras while ensuring reliability and scalability.
3.	Cloud Integration: Evaluate and recommend the use of cloud services for functions like website hosting and email services, considering the company's specific needs.
4.	Security Controls: Conduct a comprehensive cybersecurity risk assessment and recommend appropriate security controls to safeguard the network and sensitive data.
5.	Bandwidth Requirements: Determine the bandwidth requirements for different network segments, taking into account the data transfer needs of each department (Cains, et al., 2022).
6.	Monitoring and Maintenance: A plan for network monitoring and maintenance to ensure optimal performance and security.
7.	Backup and Disaster Recovery: A strategy for data backup and disaster recovery to prevent data loss and ensure business continuity.
8.	IP Camera Integration: Integration of the IP-based security cameras into the network and ensure secure storage and monitoring of video feeds.
9.	Scalability: Design the network with scalability in mind to accommodate future growth in terms of devices and services.
These assumptions and requirements will serve as the foundation for the network design, cloud service integration, and cybersecurity risk assessment for the small manufacturing company. 
The network design for the small manufacturing company will be developed in accordance with the previously stated criteria and assumptions. Below are the key elements of the design:
2.2	Network Topology: 
A hierarchical network design is proposed with the objective of maximizing the interconnectivity among the factory, office, and security cameras. This design ensures scalability, reliability, and ease of management.
1.	Core Layer: The network infrastructure is centered around a high-performance Layer 3 switch that serves as the core router, facilitating inter-subnet routing. This switch is responsible for routing traffic between the factory, office, and security camera subnets.
2.	Distribution Layer: In the distribution layer, there are Layer 2 switches allocated for each subnet, namely the factory, office, and security cameras. These switches are responsible for VLAN segmentation and ensuring efficient traffic flow within each subnet (Ghelani, 2022).
3.	Access Layer: In the distribution layer, there are Layer 2 switches allocated for each subnet, namely the factory, office, and security cameras. Each access switch connects to its respective distribution layer switch.
 
Figure 1 Network diagram
IP Addressing: The IP address ranges that will be utilized are those that satisfy the criteria outlined in the given case:
•	For the factory subnet: 27.43.0.0/16 
•	For the office subnet: 27.19.0.0/24 
•	For the security camera subnet: 26.100.24.0/24 
Hardware Recommendations: For optimal network performance, the following minimum hardware specifications are recommended:
•	Core Layer Switch/Router: Cisco Catalyst 9300 Series
•	Distribution Layer Switches: Cisco Catalyst 3650 Series
•	Access Layer Switches: Cisco Catalyst 2960 Series
•	Wireless Access Points: Cisco Aironet 3800 Series for high-density areas
•	IP Cameras: Axis Communications network cameras for security surveillance
•	Servers: Dell PowerEdge series for hosting local services
Explanation of Key Design Decisions:
•	Hierarchical Design: A hierarchical design was selected in order to enhance the management, scalability, and network efficiency. This design separates core routing functions from distribution and access layer switches, reducing broadcast domains and improving security.
•	VLAN Segmentation: Each subnet (factory, office, security cameras) is associated with a separate VLAN to isolate traffic and enhance security. VLANs provide flexibility in network management.
•	IP Addressing: The /24 and /16 both subnet masks were employed in accordance with the stipulated requirements, and IP address ranges were chosen to correspond with the final two digits of the student IDs of the group members, thus fulfilling the specified criteria.
•	Recommended Hardware: The choice of Cisco network equipment ensures reliability, scalability, and compatibility with enterprise-level networking needs.
This network design provides the small manufacturing company with a robust and secure network infrastructure. It supports their current requirements and allows for future expansion while integrating cloud services and implementing necessary security controls.
3	Cloud services
3.1	Pricing for cloud services
In order to ascertain the expenses associated with hosting a web server and a backup server in separate cloud providers, namely AWS and Azure, for a small manufacturing company, it is imperative to guarantee that the specs of both servers are comparable to provide an equitable comparison. Here are the details and justifications for each service for the given case scenario:
Web Server:
•	Operating System: Linux (Ubuntu)
•	Region: Australia (Sydney)
•	Virtual Machine (VM) Type: Standard B2s (2 vCPUs, 4 GB RAM)
•	Storage: 50 GB SSD
•	Data Transfer: 100 GB per month
Backup Server:
•	Operating System: CentOS (a common choice for backup servers)
•	Region: Australia (Sydney)
•	Virtual Machine (VM) Type: Standard B2s (2 vCPUs, 4 GB RAM)
•	Storage: 500 GB SSD (encrypted storage)
•	Data Transfer: 100 GB per month
Justifications:
•	Operating System: Linux, specifically the Ubuntu distribution, is a highly economical and dependable option for the purpose of hosting a web server. CentOS is a highly appropriate selection for a backup server because to its exceptional reliability and robust security attributes.
•	Region: Selecting the Australia (Sydney) area is vital in order to minimize latency for users situated in the company's vicinity. This is particularly crucial for facilitating web hosting and data backup operations.
•	VM Type: The Standard B2s option presents a well-balanced solution for server configurations, providing a satisfactory allocation of both central processing unit (CPU) and random-access memory (RAM) resources, while maintaining a cost-effective approach (Mughal, 2020).
•	Storage: A total of 50 gigabytes (GB) of solid-state drive (SSD) storage was assigned to the web server for the purpose of hosting the website and its associated material. A storage capacity of 500 GB on an encrypted SSD is deemed adequate for safely storing critical files on the backup server.
•	Data Transfer: A data transfer allowance of 100 GB per month is suitable for the expected traffic and backup needs of the company.
Now, the annual costs for each server in AWS and Azure are estimated below:
AWS Pricing (per year):
•	Web Server: 313.36 USD (2 vCPUs, 4 GB RAM, 50 GB SSD, 100 GB data transfer)
•	Backup Server: 862.96 USD (2 vCPUs, 4 GB RAM, 500 GB SSD, 100 GB data transfer)
 
Figure 2 AWS pricing
Azure Pricing (per year):
•	Web Server: $476.88 (2 vCPUs, 4 GB RAM, 50 GB SSD, 100 GB data transfer)
•	Backup Server: $836.88 (2 vCPUs, 4 GB RAM, 500 GB SSD, 100 GB data transfer)
 
Figure 3Azure pricing
Recommendation: Considering the cost and specifications, both AWS and Azure offer competitive pricing for hosting the web and backup servers. However, based on slightly lower pricing, Azure is recommended. Additionally, Azure provides excellent integration with Microsoft products and services, which may be beneficial for the company's future needs.
3.2	Comparison of Backup Strategies
The company is considering three different backup approaches i.e., local backup only, backup to the cloud if data is encrypted before sending to the cloud, and backup to the cloud without encryption. Each approach has its own advantages and disadvantages for the company:
Local Backup Only: 
Advantages:
•	Control: The company has full control over the backup process and can manage it internally.
•	Data Privacy: Sensitive data remains entirely within the company's premises, minimizing exposure to external threats.
•	Speed: Backup and restore operations tend to be faster when performed locally.
Disadvantages:
•	Limited Offsite Protection: Data is not stored offsite, which means it could be lost in case of disasters affecting the company's physical location.
•	Scalability: Local storage capacity may be limited, making it challenging to scale backup solutions as data volumes grow.
Backup to the Cloud with Encryption: 
Advantages:
•	Offsite Backup: Data is securely stored offsite, providing protection against on-premises disasters.
•	Data Security: Encryption ensures that even if the data is intercepted during transfer or stored in the cloud, it remains confidential.
•	Scalability: Cloud services can easily scale to accommodate growing data storage needs.
Disadvantages:
•	Cost: Cloud storage costs can add up, especially for large volumes of data.
•	Dependency: Relying on a cloud provider means the company must trust the provider's security measures and policies.
•	Encryption Management: Proper encryption key management is crucial to prevent data loss. If keys are lost, data may become inaccessible.
Backup to the Cloud Without Encryption:
Advantages:
•	Offsite Backup: Data is securely stored offsite, providing protection against on-premises disasters.
•	Cost-Efficiency: Storing unencrypted data in the cloud can be cost-effective compared to encrypted storage.
Disadvantages:
•	Security Risk: Storing unencrypted data in the cloud exposes it to potential security breaches or unauthorized access.
•	Compliance Issues: Depending on the nature of the data, regulatory requirements for data protection may not be met.
•	Data Privacy Concerns: The company may have concerns about data privacy if it is not encrypted, even in a cloud environment (Gupta, et al., 2020).
A combination of local and cloud-based backup strategies was used which were as follows:
•	Local External Drives: Backups of important assignments and documents on external hard drives or USB flash drives were also created. This provides a physical backup that is not dependent on the internet.
•	Cloud Storage Services: A significant number of individuals use cloud storage services such as Google Drive, Dropbox, or OneDrive for the purpose of storing and synchronizing documents. These services automatically backup files to the cloud, providing easy access and recovery options.
•	Version Control Systems: For code-related work, version control systems like Git and platforms like GitHub are used. These systems not only keep track of changes but also serve as offsite backups.
4	Security
4.1	Conduct cyber security risk assessment 
Asset identification 
There are following assets in this work. The assets are identified based on the 6 key asset types:
•	Customer information (Data)
•	Network servers (hardware)
•	Network configuration process (process)
•	Corporate network infrastructure (network)
•	ERP software (software)
•	Network administrators (Personnel) 
Threats:
1.	Customer Information (Data): 
a. Information Extortion: Malicious actors may attempt to steal customer data for ransom. 
b. Software Attacks: Vulnerabilities in data management software could be exploited to compromise customer information.
 c. Espionage and Trespass: Competitors or external entities may attempt to gain unauthorized access to sensitive customer data. 
d. Theft: Employees with access to customer data may misuse it intentionally or inadvertently.
Security controls:
•	Implement strong encryption for customer data.
•	Regularly update and patch software to mitigate vulnerabilities.
•	Enforce strict access controls and monitor user activities.
•	Provide cybersecurity training to employees to recognize and report threats.
2.	Network Servers (Hardware): 
a. Technical Hardware Failures or Errors: Hardware components of servers may fail, leading to service disruptions.
 b. Theft: Physical theft of server hardware can result in data loss and service unavailability. 
c. Forces of Nature: Natural disasters like floods or earthquakes can damage server hardware.
 d. Sabotage and Vandalism: Deliberate physical damage or sabotage of servers can disrupt operations.
Security control
•	Implement redundancy and failover mechanisms to mitigate hardware failures.
•	Secure servers in locked rooms with access controls.
•	Employ disaster recovery and backup strategies.
•	Monitor server locations for unauthorized access or tampering.
3.	Network Configuration Process (Process): 
a. People Errors: Human errors during configuration changes can lead to network vulnerabilities.
b. Technical Software Failures or Errors: Configuration errors in network software can cause network disruptions. 
c. Changing Quality of Services: Changes in service providers or network configurations may impact network performance. 
d. IP Compromises: IP addresses may be spoofed or compromised, leading to unauthorized access.
Security Control 
•	Implement a change management process with approval and testing steps.
•	Regularly audit network configurations for vulnerabilities.
•	Maintain a network performance monitoring system.
•	Use intrusion detection systems to identify IP compromises.
4.	Corporate Network Infrastructure (Network): 
a. Theft: Theft of networking equipment can disrupt communication and data transfer. 
b. Technical Hardware Failures or Errors: Network hardware failures can lead to network outages.
c. Technological Obsolescence: Aging network infrastructure may become vulnerable to new threats. 
d. Software Attacks: Vulnerabilities in network software can be exploited for unauthorized access.
Security Control
•	Secure networking equipment in restricted areas.
•	Implement hardware redundancy and regular maintenance.
•	Plan for network infrastructure upgrades and replacements.
•	Keep network software up to date with patches and updates.
5.	ERP Software (Software): 
a. Software Attacks: Vulnerabilities in the ERP software can be exploited to gain unauthorized access. 
b. People errors: Employees with access to the ERP system may misuse or steal sensitive data.
c. Technical Software Failures or Errors: Software errors can disrupt business operations. 
d. Changing Quality of Services: Disruptions in ERP services may impact business processes.
Security Control:
•	Regularly update and patch ERP software to address security vulnerabilities.
•	Implement access controls and monitoring for ERP users.
•	Establish data backup and recovery procedures.
•	Have contingency plans for ERP service disruptions.
6.	Network Administrators (Personnel): 
a. People errors: Malicious actions or negligence by network administrators could pose risks. 
b. Espionage and Trespass: External entities may attempt to recruit or compromise network administrators. 
c. Information Extortion: Administrators may be targeted for access to sensitive data. 
d. Technical Hardware Failures or Errors: Errors in hardware configuration by administrators may lead to issues.
Security Control:
•	Conduct background checks and regular security training for administrators.
•	Implement least privilege access controls for administrators.
•	Monitor administrator activities and access.
•	Ensure that hardware configurations are reviewed and tested before implementation.
This mini cyber security risk assessment identifies potential threats to various assets and provides sample responses to mitigate those threats. A comprehensive risk assessment would involve further analysis, likelihood and impact assessments, and the development of a risk management plan.
 
Figure 4 TVA matrix
 
Figure 5 Vulnerabilities
4.2	Recommend security controls
Based on the identified threats and assets in the mini cyber security risk assessment, as well as industry best practices, I recommend the following security controls for the network of the small manufacturing company:
1. Encryption for Customer Information:
•	Asset Protected: Customer Information (Data)
•	Threat Mitigated: Information Extortion, Espionage, Insider Threats
•	Explanation: Implement end-to-end encryption for customer data both in transit and at rest. Use strong encryption protocols such as TLS for data in transit and AES for data at rest. This control ensures that even if data is intercepted, it remains confidential and secure.
2. Intrusion Detection and Prevention System (IDPS):
•	Asset Protected: Network Servers (Hardware), Network Configuration Process (Process)
•	Threat Mitigated: Software Attacks, IP Compromises, Technical Software Failures
•	Explanation: Deploy an IDPS to monitor network traffic and detect abnormal behavior or intrusion attempts. It can identify and block malicious activities, protecting network servers and configurations.
3. Regular Software Patching and Updates:
•	Asset Protected: Corporate Network Infrastructure (Network), ERP Software (Software)
•	Threat Mitigated: Software Attacks, Technological Obsolescence
•	Explanation: Establish a process for timely software patching and updates, especially for network infrastructure and ERP software. This control addresses vulnerabilities that could be exploited by attackers.
4. Data Backup and Disaster Recovery Plan:
•	Asset Protected: Customer Information (Data), Network Servers (Hardware), Corporate Network Infrastructure (Network), ERP Software (Software)
•	Threat Mitigated: Theft, Technical Hardware Failures, Software Attacks, Changing Quality of Services
•	Explanation: Develop a comprehensive data backup and disaster recovery plan. Regularly back up critical data and systems to secure locations, both onsite and offsite. This control ensures data availability in case of hardware failures or disasters.
5. Access Controls and Least Privilege:
•	Asset Protected: Network Administrators (Personnel), ERP Software (Software)
•	Threat Mitigated: Insider Threats, Espionage
•	Explanation: Implement strict access controls and least privilege principles for network administrators and ERP users. This ensures that individuals have access only to the resources necessary for their roles, reducing the risk of insider threats.
6. Security Awareness Training:
•	Asset Protected: Network Administrators (Personnel), All Assets
•	Threat Mitigated: People Errors, Insider Threats
•	Explanation: Conduct regular security awareness training for network administrators and all employees. Training should include recognizing phishing attempts, safe data handling practices, and incident reporting procedures. An educated workforce is less likely to fall victim to social engineering attacks.
7. Physical Security Measures:
•	Asset Protected: Network Servers (Hardware)
•	Threat Mitigated: Theft, Sabotage and Vandalism
•	Explanation: Enhance physical security by placing network servers in locked and access-controlled rooms. Implement security cameras and alarms to deter theft and sabotage.
These security controls are specific to the scenario and aim to address the identified threats to the company's assets. By incorporating these controls into the network design and operations, the company can enhance its cybersecurity posture and protect its sensitive data and infrastructure. These recommendations align with industry best practices, such as the NIST Cybersecurity Framework and ACSC Essential Eight, to mitigate known risks effectively.
5	 Project management 
5.1	Project plan 
Communication Frequency	Communication Methods	Task Name
As Needed	GitHub Repository	Form Project Group and Setup Repository
Every Saturday	Zoom Meetings	Agree on Communication Plan and Schedule
Weekly	Zoom Meetings	 Network Design
Every Thursday	Slack (for quick updates)	Cloud Services Estimation
Weekly	Zoom Meetings	Backup Strategies Analysis
Weekly	Slack and Email (for asynchronous)	Cybersecurity Risk Assessment
Daily 	Zoom Meetings	Security Controls Recommendation
Weekly	GitHub Repository	Finalize Project Report and Documentation
As Needed	Zoom Meetings and Email (as needed)	Review and Finalize GitHub Repository
Currently, the integration of Slack and email has been implemented to facilitate expeditious updates, asynchronous communication, and deliberations that do not necessitate instant in-person engagement. Zoom meetings are still scheduled weekly to ensure regular progress updates and discussions. GitHub remains the central repository for project-related documentation.
6	Project reflection 
During the project, our group of two members collaborated effectively to complete the tasks. Here is a reflection on how we worked in the group, what worked well, and the issues we encountered, along with recommended techniques for future group projects:
Work Distribution:
•	What Worked Well: We divided tasks based on our strengths and interests. One team member took the lead on network design and cloud services estimation, while the other focused on backup strategies, cybersecurity risk assessment, and security controls.
•	Challenges Encountered: While task distribution was generally efficient, we occasionally faced challenges when a task required input from both team members, leading to coordination issues.
Effective Communication:
•	What Worked Well: We established regular Zoom meetings to discuss progress, clarify doubts, and make joint decisions. Using Slack for quick updates and asynchronous communication was effective.
•	Challenges Encountered: Scheduling Zoom meetings to accommodate both team members' availability was occasionally challenging due to time zone differences.
Documentation and Version Control:
•	What Worked Well: We maintained a well-organized GitHub repository, which served as a central hub for project documents, code, and discussions.
•	Challenges Encountered: At times, we faced merge conflicts in the GitHub repository when multiple team members were working on the same document simultaneously.
Future Techniques for Successful Teamwork:
1.	Task Breakdown and Allocation: Clearly define project tasks and allocate them based on team members' skills and preferences. Ensure that tasks are independent wherever possible to minimize dependencies.
2.	Regular Check-Ins: Establish a regular meeting schedule to discuss progress, address concerns, and make decisions collaboratively. Use a shared calendar to facilitate scheduling.
3.	Effective Use of Collaboration Tools: Utilize collaboration tools like Slack, Microsoft Teams, or similar platforms for quick updates, file sharing, and asynchronous communication. Ensure that everyone is familiar with these tools.
4.	Time Zone Considerations: If team members are in different time zones, use scheduling tools that consider time zone differences to find suitable meeting times. Also, be flexible and accommodating when scheduling meetings (Rahouti, Xiong, and Lin, 2021).
5.	Version Control Training: Ensure that all team members are proficient in using version control systems like Git and GitHub to avoid merge conflicts and document versioning issues.
6.	Conflict Resolution Plan: Develop a conflict resolution plan or process to address disagreements or disputes within the team. Establish guidelines for escalating issues if they cannot be resolved internally.
7.	Regular Repository Maintenance: Assign a team member to be responsible for maintaining the GitHub repository, ensuring that documents are organized, labeled, and up to date.
8.	Feedback and Evaluation: Conduct periodic evaluations of team performance and communication. Use feedback to identify areas for improvement and make necessary adjustments.
These techniques aim to address common issues in group projects, such as task allocation, communication, and coordination. They facilitate smoother collaboration, reduce misunderstandings, and enhance overall project efficiency.
 
7	References
Balzacq, T. and Cavelty, M.D., 2016. A theory of actor-network for cyber-security. European Journal of International Security, 1(2), pp.176-198.
Cains, M.G., Flora, L., Taber, D., King, Z. and Henshel, D.S., 2022. Defining cyber security and cyber security risk within a multidisciplinary context using expert elicitation. Risk Analysis, 42(8), pp.1643-1669.
Ghelani, D., 2022. Cyber Security in Smart Grids, Threats, and Possible Solutions. Authorea Preprints.
Gupta, B.B., Perez, G.M., Agrawal, D.P. and Gupta, D., 2020. Handbook of computer networks and cyber security. Springer, 10, pp.978-3.
Mughal, A.A., 2020. Cyber Attacks on OSI Layers: Understanding the Threat Landscape. Journal of Humanities and Applied Science Research, 3(1), pp.1-18.
Rahouti, M., Xiong, K. and Lin, J., 2021. Leveraging a cloud‐based testbed and software‐defined networking for cybersecurity and networking education. Engineering Reports, 3(10), p.e12395.
Syafrizal, M., Selamat, S.R. and Zakaria, N.A., 2020. Analysis of cybersecurity standard and framework components. International Journal of Communication Networks and Information Security, 12(3), pp.417-432.






