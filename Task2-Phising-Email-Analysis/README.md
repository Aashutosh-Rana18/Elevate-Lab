# 📧 Phishing Email Analysis Report: Phishing-Email-Sample.eml

## 📝 Project Overview
This project entails a thorough investigation of a phishing email sample **(Phishing-Email-Sample.eml)** to uncover **indicators of compromise (IoCs)**, malicious attachments, and hidden threats.  
The goal is to build **hands-on expertise** in:  
* 🕵️ Phishing detection  
* 🧪 Email forensics  
* 🌐 Network reconnaissance  

… thereby strengthening cybersecurity practices against **social engineering attacks**.

## 📂 Sample Source
* 📥 The suspicious email file **"Phishing-Email-Sample.eml"** was obtained from a **controlled analysis environment**, simulating a real-world phishing incident.  
* 🔒 It included **encoded attachments** and was analyzed in an **isolated virtual machine** to prevent malware execution.

## 🔍 Key Analysis Steps

### 1️⃣ Sender Email Verification
* 🔎 Reviewed sender’s email address for signs of **spoofing** (mismatched domains, unusual characters).  
* 🆚 Compared displayed sender name vs. actual **From** field to detect **impersonation**.

### 2️⃣ Email Header Analysis
* 📬 Used header inspection tools to analyze **Received** fields & originating IP addresses.  
* 🌎 Checked for **routing anomalies**, unexpected relays, and suspicious geolocations.

### 3️⃣ Authentication Protocol Checks
* ✅ Verified **SPF, DKIM, and DMARC** authentication results.  
* ❌ Found **failures**, confirming spoofed sender and unauthorized email relay.

### 4️⃣ Content and Language Review
* ⚠️ Identified **urgent and fear-inducing** language (e.g., “Immediate action required”).  
* 🖊️ Detected **generic greetings** (“Dear User”) and **grammar/spelling errors** common in phishing campaigns.

### 5️⃣ Attachment and File Analysis
* 🧩 Decoded **Base64-encoded PDF** using CyberChef and converted to hex.  
* 📦 Extracted files from a ZIP (**DaughtersCrown, GoodJobMajor, Money.xlsx**).  
* 🔍 Detected **hex mismatch** in Money.xlsx → investigated further.  
* 🧑‍💻 Opened spreadsheet in **Google Sheets** (disposable account).  
* 🗝️ Found **hidden Base64 message** in Sheet 3 → decoded → revealed IP address `93.99.104.210`.

### 6️⃣ Network Investigations
* 🌐 Ran **traceroute** on `93.99.104.210` to analyze network hops.  
* 🛠️ Conducted **Nmap stealth SYN scan (-sS)** to find open ports, services, and vulnerabilities (within legal limits).

### 7️⃣ Phishing Characteristics Summary
* Compiled technical + linguistic indicators into a final **phishing profile report**.

## 🚨 Phishing Indicators Found in Phishing-Email-Sample.eml
* 🕵️ Spoofed sender address with mismatched domain  
* ❌ **SPF, DKIM, DMARC authentication failures**  
* 🌎 Suspicious IP paths & forged relays  
* ⚡ Urgent call-to-action messages to pressure recipients  
* 🗂️ Encoded attachments with **hex mismatches** (possible tampering)  
* 🧑‍💻 Hidden Base64 message → malicious IP address  
* 👤 Generic greetings + grammatical inconsistencies  
* 💻 Attachments potentially delivering malware (**MalSpam technique**)

## 🛠️ Tools Used
* 🔑 **CyberChef** – Base64 decoding, hex conversion, data extraction  
* 🔢 **GHex** – Hexadecimal file viewing & verification  
* 🏷️ **ExifTool** – Metadata analysis of extracted files  
* 📊 **Google Sheets (disposable account)** – Safe spreadsheet inspection  
* 🌐 **Traceroute & Nmap** – Network path tracing and port scanning  
* 🖊️ **Text Editors & Email Clients** – Manual review of headers and content

## 🎯 Learning Outcomes
* ✅ Mastered **email header dissection** and spotting spoofed senders  
* 🧩 Learned **attachment forensics** and detecting hidden payloads  
* 🌍 Enhanced skills in **network reconnaissance** & IP investigation  
* 🛡️ Gained awareness of **phishing attack vectors** and **social engineering techniques**  
* 📧 Improved understanding of **SMTP, POP3, IMAP protocols** and **email authentication mechanisms** to prevent future incidents

---

📌 *This report was created as part of a practical cybersecurity exercise to enhance phishing detection, forensics, and network investigation skills.*
