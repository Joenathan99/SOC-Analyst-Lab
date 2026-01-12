📌 Room: Phishing Analysis

Platform: TryHackMe

Difficulty: Beginner

Focus: Email phishing investigation, proxy logs, firewall logs, SIEM analysis



🧠 Objective

The objective of this lab was to investigate a suspected phishing email and determine whether the user interacted with the malicious content by analyzing logs within a SIEM environment.


🛠 Tools & Data Sources

- SIEM (log search & correlation)

- Email headers

- Proxy logs

- Firewall logs


🔍 Investigation Summary
1. Phishing Email Analysis

The investigation began by reviewing the phishing email to identify potential Indicators of Compromise (IOCs), including:

- Malicious URL

- Sender details

- Timestamp of delivery

These IOCs were used as pivot points for further analysis in the SIEM.

2. Proxy Log Analysis

Proxy logs were queried to determine whether the user accessed the malicious URL.

Findings:

- Proxy logs confirmed that the user attempted to access the suspicious domain contained in the phishing email.

- The logs provided visibility into the requested URL, timestamp, and action taken (allowed/blocked).

This confirmed user interaction with the phishing email.

3. Firewall Log Analysis

Firewall logs were analyzed to identify any outbound network connections related to the phishing activity.

Findings:

- Outbound traffic from the user’s internal IP to an external IP address associated with the phishing infrastructure was observed.

- Network traffic details such as destination IP and port were reviewed to validate the connection.

This confirmed external communication following the phishing click.

4. Correlation & Conclusion

By correlating email data, proxy logs, and firewall logs, it was determined that:

- The phishing email was delivered successfully

- The user interacted with the malicious link

- Outbound communication to a suspicious external IP occurred

This indicates a successful phishing interaction, warranting further endpoint investigation and remediation.

🚨 Recommendations

- Reset affected user credentials

- Block malicious domains and IPs

- Conduct endpoint malware scanning

- Provide phishing awareness training


🧩 Skills Demonstrated

- Phishing email analysis

- SIEM log searching and filtering

- Proxy and firewall log analysis

- IOC identification and correlation

  Attached below are images that show the tasks i carried out;

<img width="1855" height="844" alt="Screenshot 2026-01-11 161942" src="https://github.com/user-attachments/assets/b46f1975-cdb4-410c-87a2-743c035ea468" />

<img width="1398" height="796" alt="Screenshot 2026-01-11 174153" src="https://github.com/user-attachments/assets/8dc544a9-c39a-40a9-b344-021eecac4397" />

<img width="1487" height="616" alt="Screenshot 2026-01-11 174222" src="https://github.com/user-attachments/assets/7200be6b-b1cd-4d74-83a5-faf7ab4608c3" />

<img width="1394" height="738" alt="Screenshot 2026-01-11 174253" src="https://github.com/user-attachments/assets/e4b93a13-49d4-4a53-b610-e49e821716df" />

<img width="1490" height="609" alt="Screenshot 2026-01-11 174315" src="https://github.com/user-attachments/assets/1745c440-42b6-4496-ab29-23a61069b0d9" />

<img width="1378" height="734" alt="Screenshot 2026-01-11 174328" src="https://github.com/user-attachments/assets/5ba7d101-489d-4cbd-a92b-2c874f3eb2bd" />

<img width="1479" height="624" alt="Screenshot 2026-01-11 174345" src="https://github.com/user-attachments/assets/5ca2b0a6-13c4-4798-b5b8-5eac078a4dc1" />

<img width="1412" height="781" alt="Screenshot 2026-01-11 181216" src="https://github.com/user-attachments/assets/e94b5d91-def3-41ca-90b5-fbccc599b70a" />




<img width="1487" height="593" alt="Screenshot 2026-01-11 174133" src="https://github.com/user-attachments/assets/d42ef3ae-6203-49c0-85b9-77e60cd8124c" />


📎 Notes

This lab simulates real-world phishing alerts and investigation workflows commonly performed in security operations centers.






