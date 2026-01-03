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



Alert 2: Potential Data Exfiltration

Severity: Critical

Alert Description: 

This alert was generated due to a large or unusual outbound data transfer, which could indicate possible data exfiltration.

Evidence Reviewed

- Network traffic volume

- Destination address

- Timing of the data transfer



<img width="1837" height="407" alt="Screenshot 2026-01-02 220643" src="https://github.com/user-attachments/assets/d8a53010-e48c-491f-ad69-394efd11aa24" />

Analysis:

The data transfer exceeded normal thresholds and was flagged as critical. However, the destination and behavior aligned with expected system or user activity, and no sensitive data indicators were identified. Hence my verdict of FALSE POSITIVE. 


<img width="1819" height="459" alt="Screenshot 2026-01-02 221739" src="https://github.com/user-attachments/assets/b11f4a6a-3e54-4704-a43e-28067740b5ed" />


Reasoning:

Although the alert severity was high, the activity could be reasonably explained as legitimate data movement. There was no real evidence of malicious data exchange, which generated the right flag for the challenge.



Alert 3: Download from GitHub Repository

Severity: Low
Status: Awaiting Action

Alert Description:

This alert indicated a file download originating from a GitHub repository.

Evidence Reviewed:

- Source domain (GitHub)

- File type

- User activity context

<img width="1815" height="377" alt="Screenshot 2026-01-03 003046" src="https://github.com/user-attachments/assets/a0fa6cbe-2a5a-4ed3-b8fd-45710a1b743e" />

Analysis:

GitHub is commonly used for legitimate software downloads and development activity. No malicious indicators or suspicious behavior were associated with the download. Hence, my verdict of FALSE POSITIVE

<img width="1819" height="351" alt="Screenshot 2026-01-03 003323" src="https://github.com/user-attachments/assets/8fc4e435-ff49-4baa-bd1f-5141ccd4a867" />

Reasoning:

The download originated from a trusted platform and matched normal user behavior. No further investigation was required. This in turn generated the flag to solve the challenge.
