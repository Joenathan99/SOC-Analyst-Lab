SOC Level 1 Alert Triage – TryHackMe

Overview:

This lab simulates a Security Operations Center (SOC) Level 1 analyst workflow, where multiple security alerts are generated and require triage. The objective is to review each alert, analyze the available evidence, and determine if the alert is a true positive or a false positive.

The focus is on alert context, log review, and analyst reasoning, rather than automated responses.

Environment & Tools

- Simulated SIEM dashboard

- Alert metadata (severity, timestamp, status)

- Log and event details associated with alerts

- Analyst decision-making (verdict assignment)

Alert Summary: The following alerts were reviewed during this investigation:

- Double-Extension File Creation (High)

- Potential Data Exfiltration (Critical)

- Download from GitHub Repository (Low)

Alert 1: Double-Extension File Creation

Severity: High
Status: Awaiting Action

Alert Description:

This alert was triggered due to the creation of a file with a double extension (e.g. filename.pdf.exe), a common technique used to disguise malicious executables as legitimate documents.

Evidence Reviewed:

- File name and extension pattern

- File creation activity on the host

- User context associated with the action

<img width="1802" height="520" alt="Double-Extension File Creation" src="https://github.com/user-attachments/assets/bd427e0e-60f6-43ae-b9e4-649f106e0d2b" />



Analysis:

Double-extension files are often associated with phishing or malware deliverym, this was enough to draw conclusion on my verdict of TRUE POSITIVE


<img width="1769" height="404" alt="Screenshot 2026-01-02 195152" src="https://github.com/user-attachments/assets/874b7356-9459-4ce4-933b-8cf95ad86232" />



Reasoning:

The filename pattern is suspicious, that gave enough reason to flag it. No additional indicators of compromise were observed. This would result in generating the flag for the challenge.

