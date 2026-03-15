# Trojan Email Attachment Investigation

**Platform:** LetsDefend  
**Type:** Email / Malware / Trojan  
**Date:** 2026-02-24  
**Author:** Aeron Lugtu  

---

## 1. Alert Summary
A suspicious email attachment was flagged as potentially malicious. Initial analysis suggested it might be a Trojan. The goal of this investigation was to confirm the threat and prevent any further risk to internal devices.

---

## 2. Investigation Steps

### Step 1: Threat Intelligence
- Submitted the suspicious file to VirusTotal for analysis.  
- Identified associated malicious IP addresses and other threat indicators.

### Step 2: Network Log Analysis
- Correlated malicious IP addresses identified on VirusTotal with internal network logs.
- Checked if any internal devices had communicated with attacker infrastructure.
- Found that an internal device with an IP 172.16.17.45 had an outbound connection to 5.135.143.133

### Step 3: Containment & Remediation
- Identified affected device(s).  
- Isolated compromised systems to prevent lateral movement.  
- Removed the malicious email from all relevant mailboxes to stop further exposure.

---

## 3. Findings
- The attachment was confirmed as a Trojan.  
- Network logs revealed which internal devices had interacted with malicious IPs.  
- Containment prevented further compromise.

---

## 4. Key Takeaways
- ✅ Threat intelligence tools like VirusTotal enable rapid incident detection.  
- ✅ Correlating malicious IPs with internal logs is crucial for identifying compromised devices.  
- ✅ Quick containment and remediation are essential to protect organizational assets.

---

## 5. Conclusion
This hands-on lab reinforced the importance of **structured SOC workflows** and **proactive monitoring**. Following a consistent process ensures timely detection, analysis, and mitigation of malware threats.

**Investigation Workflow:**  
**Alert → Threat Intelligence → Network Analysis → Containment → Conclusion**

---

## 6. Skills Practiced
- Malware detection & analysis  
- Threat intelligence (VirusTotal)  
- Network log correlation  
- Incident containment and remediation  
- SOC workflow adherence  

---

## 7. References / Notes
- Platform: LetsDefend  
- Related MITRE ATT&CK Technique: [T1566 – Phishing](https://attack.mitre.org/techniques/T1566/)

<h2>Screenshots Walk Through</h2>

<p align="center">
Alert: SOC114 <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45a.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
File Attachment <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45b.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
VirusTotal Verification:  <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45c.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Malicious IP Addresses identified on VirusTotal: <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45e.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Identified the internal device that interacted with the malicious IP <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45f.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Evidence of communication with Malicious IP  <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45g.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45h.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Containment of the Internal device <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/45i.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
