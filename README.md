# Security Operations Center

In this project, I designed and implemented a comprehensive Security Operations Center (SOC) as part of my coursework in Cybersecurity. The SOC is designed to detect, analyze, and respond to various security incidents using a variety of tools and techniques. The core objective of this project was to create a robust system capable of monitoring and defending an internal network against potential cyber threats.

**Report:** [SOC Documentation](../soc_documentatie.pdf)

**Video:** [YouTube](https://youtu.be/N6xHx_H27Vk)

**Completed:** January 2023

## Security Operations Center

The SOC I developed was built on a foundation of reliable and secure technologies. The production environment was centered around Ubuntu Server 22.04, chosen for its robustness and the specific security challenges it presents. This operating system was complemented by pfSense, which managed the network traffic with its powerful firewall and routing capabilities, ensuring that the internal network remained secure from external threats.

For threat detection and prevention, I implemented Suricata, an open-source intrusion detection and prevention system. Suricata was strategically deployed on the pfSense firewall to monitor all network traffic. It played a crucial role in identifying potential threats by analyzing the traffic and generating alerts when suspicious activities were detected. These alerts were then forwarded to the central monitoring system for further analysis.

To centralize and streamline log management and threat detection, I used Wazuh as the primary SIEM solution. Wazuh aggregated logs from various endpoints, including the Ubuntu server and pfSense, and provided a powerful alerting mechanism. This system allowed me to detect and respond to a wide range of security issues, from known vulnerabilities to brute-force attacks, file tampering, and even rootkit installations. Moreover, Wazuh was integrated with VirusTotal, which added an extra layer of security by automatically scanning suspicious files and triggering remediation actions if malware was detected.

Incident response was further enhanced through the integration of Shuffle I.O, a SOAR (Security Orchestration, Automation, and Response) solution. Shuffle I.O allowed me to automate the handling of security alerts, reducing the time it took to respond to potential threats. Critical alerts were automatically forwarded to TheHive, an incident response platform, and notifications were sent to a dedicated Discord channel, ensuring that the team could take immediate action when necessary.

Finally, TheHive served as the incident management platform, providing a centralized system for tracking and responding to security events. With TheHive, I was able to ensure that all incidents were managed systematically and efficiently, from detection through to resolution.

![SOC Scheme](../img/SOC-3.png)
