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

Analysis:

Double-extension files are often associated with phishing or malware delivery. However, context is critical. Upon reviewing the available details, there was no supporting evidence of execution, user interaction, or follow-on malicious behavior related to this file.

Verdict:
False Positive

Reasoning:

While the filename pattern is suspicious, there was insufficient evidence to confirm malicious intent or impact. No additional indicators of compromise were observed.
