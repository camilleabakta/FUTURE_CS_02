# Future Interns - Cyber Security Task 2
## SOC Incident Investigation Report & SIEM Monitoring

### Project Overview
This repository contains my submission for **Task 2** of the Future Interns Cyber Security Internship. The goal of this task was to simulate the role of a **SOC (Security Operations Center) Analyst** by using a **SIEM (Security Information and Event Management)** tool to monitor security logs, identify threats, and document an incident response.

### Tools & Environment
*   **Operating System:** Kali Linux
*   **SIEM Platform:** Splunk Enterprise 10.0.2
*   **Log Source:** `SOC_Task2_Sample_Logs.txt`
*   **Language:** SPL (Splunk Processing Language)

### Task Objectives
1.  **Data Ingestion:** Import raw security logs into Splunk.
2.  **Threat Hunting:** Analyze logs to identify suspicious patterns (Malware, Brute Force, etc.).
3.  **Visualization:** Create dashboards to represent the threat landscape.
4.  **Reporting:** Draft a professional Incident Investigation Report with remediation steps.

### Key Findings
During the investigation, several high-severity security incidents were identified:
*   **Critical:** Ransomware behavior detected on user **Bob's** workstation (`172.16.0.3`).
*   **High:** Persistent **Rootkits** detected on **Alice** and **Eve's** systems.
*   **Threat Actor:** External IP `203.0.113.77` identified as a primary source of infection (Worm/Trojan).

### Repository Structure
*   `SOC_Incident_Report.pdf`: The full detailed investigation report.
*   `Screenshots/`: Folder containing Splunk dashboards and investigation tables.
*   `README.md`: Project documentation.

### How to Replicate
1.  Install **Splunk Enterprise** on Kali Linux.
2.  Upload the provided log file via the "Add Data" interface.
3.  Use the following SPL query to find threats:
    ```spl
    index="main" action="malware detected" | table _time, user, ip, threat | sort - _time
    ```
4.  Navigate to the **Visualization** tab to generate the Threat Distribution Pie Chart.

### 👤 Author
**ABAKTA Haana Camille**  
Cyber Security Intern at Future Interns  
Date: January 09, 2026
