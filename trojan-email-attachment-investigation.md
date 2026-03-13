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
- Correlated malicious IPs against internal network logs.  
- Checked if any internal devices had communicated with attacker infrastructure.

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
