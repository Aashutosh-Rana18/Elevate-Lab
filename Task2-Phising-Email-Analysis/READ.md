Phishing Email Analysis Report: Phishing-Email-Sample.eml
Project Overview
This project entails a thorough investigation of a phishing email sample (Phishing-Email-Sample.eml) to uncover indicators of compromise, malicious attachments, and hidden threats. The goal is to build hands-on expertise in phishing detection, email forensics, and network reconnaissance, thereby strengthening cybersecurity practices against social engineering attacks.
Sample Source
The suspicious email file "Phishing-Email-Sample.eml" was obtained from a controlled analysis environment, simulating a real-world phishing incident. It includes encoded attachments and was analyzed in an isolated virtual machine to prevent any potential malware execution.
Key Analysis Steps
Sender Email Verification

Reviewed the sender's email address for signs of spoofing, such as mismatched domain names or unusual characters.
Compared the displayed sender name with the actual "From" field in the headers to detect impersonation of trusted entities.

Email Header Analysis

Utilized header inspection tools to trace the email's path, including "Received" fields and originating IP addresses.
Examined for routing anomalies, such as unexpected relays or geographic inconsistencies.

Authentication Protocol Checks

Verified the three core email authentication protocols: SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail), and DMARC (Domain-based Message Authentication, Reporting, and Conformance).
Noted failures in these protocols, which are common in spoofed phishing emails.

Content and Language Review

Analyzed the email body for urgent language, fear-inducing phrases, or calls to action (e.g., "Immediate action required").
Identified generic greetings (e.g., "Dear User") and linguistic errors like poor grammar or spelling, hallmarks of non-native or automated phishing campaigns.

Attachment and File Analysis

Decoded Base64-encoded PDF attachments to hexadecimal format using CyberChef and compared hex values for integrity.
Created and extracted a ZIP file ("attach.zip") from the decoded output.
Verified extracted files (DaughtersCrown, GoodJobMajor, Money.xlsx) using GHex for hex matching; noted mismatch in Money.xlsx.
Opened the mismatched spreadsheet in Google Sheets via a disposable account and discovered a hidden Base64-encoded message in Sheet 3.
Decoded the hidden message with CyberChef, revealing an IP address (93.99.104.210) or location data.

Network Investigations

Performed traceroute on the decoded IP (93.99.104.210) to map the network path and identify suspicious hops.
Conducted an Nmap stealth SYN scan (-sS) on the IP to detect open ports, services, and potential vulnerabilities, ensuring compliance with legal guidelines.

Phishing Indicators Found in Phishing-Email-Sample.eml

Spoofed sender address with mismatched domain.
Failures in SPF, DKIM, and DMARC authentication, indicating email spoofing.
Suspicious IP paths in headers suggesting forged relays.
Urgent or manipulative language to prompt user interaction.
Encoded attachments with hex mismatches, pointing to tampering or malware.
Hidden Base64 message in spreadsheet leading to a potentially malicious IP.
Generic salutations and grammatical inconsistencies.
Potential for malware delivery via attachments, aligned with MalSpam techniques.

Tools Used

CyberChef for Base64 decoding, hex conversion, and data transformation.
GHex for hexadecimal file viewing and verification.
ExifTool for bulk metadata scanning of extracted files.
Google Sheets (with disposable Gmail) for safe spreadsheet analysis.
Traceroute and Nmap for IP tracing and port scanning.
Text editors and email clients for manual header and content review.

Learning Outcomes

Acquired advanced skills in email header dissection, attachment forensics, and hidden content extraction.
Enhanced understanding of phishing variants (e.g., spear phishing, MalSpam) and social engineering tactics.
Gained proficiency in using open-source tools for threat hunting and network analysis.
Improved awareness of email delivery protocols (SMTP, POP3, IMAP) and authentication mechanisms to prevent future incidents.
