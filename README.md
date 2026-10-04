# NIST CSF Security Incident Report

1. [Introduction](#introduction)  
2. [Scenario](#scenario)  
3. [Objective](#objective)  
4. [Incident Report Analysis](#incident-report-analysis)  
5. [Notes](#notes)  
6. [Reflections](#reflections)  

# Introduction

This security incident report was completed as part of my cybersecurity documentation portfolio and the [Google Cybersecurity Professional Certificate](https://www.coursera.org/google-certificates/cybersecurity-certificate), specifically the *Connect and Protect: Networks and Network Security* course.

The purpose of this exercise was to improve my understanding of network-based security incidents, identify network vulnerabilities, and learn how the NIST Cybersecurity Framework can be used to strengthen an organization’s overall security posture.

# Scenario

I am acting as a cybersecurity analyst for a multimedia company that provides web design, graphic design, and social media marketing services to small businesses.

The organization recently experienced a Distributed Denial-of-Service (DDoS) attack that disrupted the internal network for approximately two hours.

During the attack, network services suddenly became unavailable because the network received a large volume of ICMP packets. The excessive traffic prevented legitimate internal users and devices from accessing network resources.

The incident response team reacted by blocking incoming ICMP traffic, taking non-critical services offline, and prioritizing the restoration of critical network services.

Further investigation revealed that an attacker had flooded the network with ICMP ping requests through an improperly configured firewall. Because appropriate filtering and rate-limiting rules were not configured, the attacker was able to overwhelm network resources.

Following the incident, the security team implemented several improvements:

- A firewall rule to rate-limit incoming ICMP packets.
- Source IP address verification to help identify spoofed ICMP traffic.
- Network monitoring software to detect unusual traffic patterns.
- An IDS/IPS solution to identify and filter suspicious ICMP traffic.

# Objective

The objective of this exercise is to analyze the incident and develop a plan for improving the organization’s network security using the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF).

The incident is analyzed using the five core functions of the NIST CSF:

- **Identify** — Understand cybersecurity risks by regularly reviewing networks, systems, devices, configurations, and access privileges.

- **Protect** — Apply policies, procedures, security controls, training, and technical safeguards to reduce the likelihood and impact of cyber threats.

- **Detect** — Monitor systems and network activity so suspicious behavior and potential incidents can be identified quickly.

- **Respond** — Contain, investigate, communicate, and mitigate cybersecurity incidents while improving response procedures.

- **Recover** — Restore affected systems and services and return business operations to normal after an incident.

# Incident Report Analysis

## Summary

The organization experienced a DDoS attack that caused its internal network and critical services to become unavailable.

The attacker generated a large volume of ICMP traffic and sent it toward the organization’s network. Because the firewall was not correctly configured to restrict this traffic, the network became overwhelmed and legitimate users were unable to access internal resources.

| Phase | Description |
| --- | --- |
| **Identify** | The cybersecurity team investigated the incident and determined that a malicious actor had flooded the network with ICMP ping requests. The traffic was able to enter through an improperly configured firewall that lacked appropriate controls for limiting ICMP traffic. The firewall configuration was identified as the primary security weakness that allowed the DDoS attack to affect the network. |
| **Protect** | To reduce the likelihood of similar attacks, the network security team implemented firewall rate-limiting rules for ICMP traffic. An IDS/IPS solution was also introduced to identify and filter suspicious traffic before it could significantly affect internal systems. Firewall configurations should also be reviewed regularly to ensure security rules remain effective. |
| **Detect** | Network monitoring software should be used to establish normal traffic patterns and detect unusual increases in ICMP or other network traffic. Source IP verification can also help detect spoofed IP addresses commonly used during certain denial-of-service attacks. IDS/IPS alerts should be monitored and reviewed by the security team. |
| **Respond** | During the attack, the incident response team blocked incoming ICMP traffic, disabled non-critical services, and prioritized the restoration of essential services. After containment, the team investigated the cause of the incident. Incident response procedures and playbooks should be updated based on lessons learned from the event. Security staff should also receive appropriate training on the monitoring and security tools being used. If required by applicable laws or regulations, the organization should also report the incident to relevant authorities. |
| **Recover** | The network was unavailable for approximately two hours before services were fully restored. IT and security teams worked together to bring critical systems back online and eventually restore normal business operations. After recovery, the organization should conduct a lessons-learned review to understand the cause of the incident and identify areas for improvement. Recovery procedures should also be tested so future incidents can be resolved more quickly. The organization may also evaluate cyber insurance and other business continuity options to reduce the financial impact of future attacks. |

# Notes

One useful improvement would be to schedule regular penetration testing and security assessments to verify that newly implemented safeguards are functioning correctly.

Firewall rules, IDS/IPS configurations, monitoring systems, and incident response procedures should be tested periodically rather than assuming they will work during a real attack.

Additional resources that helped support this analysis include:

[CISA — Understanding and Responding to Distributed Denial-of-Service Attacks](https://www.cisa.gov/sites/default/files/publications/understanding-and-responding-to-ddos-attacks_508c.pdf)

[NIST — How to Recover from a Cyber Attack](https://www.nist.gov/blogs/manufacturing-innovation-blog/how-recover-cyber-attack)

# Reflections

This exercise helped me understand how a single network security misconfiguration can result in a significant service disruption.

The most challenging part was deciding how much detail to include while keeping the incident report clear and easy to follow. I initially included more information than necessary, but reviewing the NIST CSF helped me organize the incident into the five core functions.

The exercise also reinforced the importance of properly configuring firewalls, continuously monitoring network traffic, and having a documented incident response process before an attack occurs.

Overall, this activity improved my understanding of how the NIST Cybersecurity Framework can be applied to a real-world network security incident and how organizations can use lessons learned from an attack to improve their future security posture.
