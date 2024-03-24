# Security Onion Senior Project Evaluation

## Improvements

### 1. Configure Cuckoo Malware Sandbox

One significant improvement for the Security Onion senior project would be to configure the Cuckoo malware sandbox on its own virtual machine. Unfortunately, due to immense troubleshooting challenges and time constraints, this aspect of the project was not completed as initially planned. Implementing Cuckoo in a separate virtual machine would enhance the overall effectiveness of the malware analysis capabilities.

### 2. Threat Actor Emulation

Demonstrating purple team exercises with threat actor emulation would be useful for students and self-development. Identifying and replicating a particular set of TTP (tactics, techniques, and procedures) of a particular actor would appeal to students more interested in offensive security.

### 3. Endpoint Detection

Security Onion provides, through Wazuh, endpoint monitoring through agents installed on machines. This was tested on a Windows host in the lab but would require much more maintenance and excessive installation to configure endpoint monitoring on all machines.

### 4. Retroactive Threat Hunting

Historical searches for indicators of compromise (IOCs) would be useful to integrate into any SIEM environment. Testing the IDS with testmynids.org, sample packet captures, or threat actor emulation would provide the opportunity for threat hunting to practice the tasks needed to identify attack chains and user behavior. 

## Limitations

### 1. Latency Issues

A primary limitation encountered during the project was latency, primarily stemming from the older CPU's clock speed. The outdated hardware posed challenges in terms of processing speed, affecting the overall performance of the Security Onion setup. To mitigate this limitation, it is imperative to explore strategies for compensating for the slow clock speed, whether through hardware upgrades or optimization techniques.

### 2. Networking Challenges with Hyper-V

Another limitation was the decision to use Hyper-V as the virtualization platform, which introduced unexpected networking problems. Dealing with these issues consumed a considerable amount of time, diverting attention from other critical project aspects. In future iterations, considering alternative virtualization solutions or addressing Hyper-V's networking challenges upfront could streamline the project timeline.
- **Virtualization Platform Consideration:**
  - Evaluate alternative virtualization platforms that may better suit the project requirements and minimize networking challenges.
  - Conduct thorough testing with the chosen platform to ensure compatibility and mitigate potential issues before full-scale implementation.

By addressing these improvements and limitations, Security Onion can achieve enhanced functionality and efficiency in threat detection and analysis.

