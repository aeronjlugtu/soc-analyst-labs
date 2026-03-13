# SQL Injection Alert Investigation

**Platform:** LetsDefend  
**Type:** Web Application / SQL Injection  
**Date:** 2026-02-27  
**Author:** Aeron Lugtu  

---

## 1. Alert Summary
A suspicious web request was flagged as a potential SQL injection attack. The alert originated from `[167.99.169.17]` targeting `[172.16.17.18]`. 

---

## 2. Investigation Steps

### Step 1: Log Review
- Reviewed web server logs to identify source and target IPs.  
- Observed multiple HTTP requests from the same external IP with suspicious URL patterns.
- Used VirusTotal to verify that the Source IP is malicious.

### Step 2: Payload Analysis
- Decoded URL-encoded payloads to inspect request parameters.  
- Confirmed the presence of SQL injection patterns.

### Step 3: Response Validation
- Examined HTTP response codes and server behavior.  
- Observed a 302 redirect with no database errors or abnormal behavior → attack unsuccessful.

---

## 3. Findings
- Repeated requests from the same IP indicate a possible reconnaissance or attack attempt.  
- Payload analysis confirmed attacker intent.  
- No compromise detected.
- Request URL contained "%27%20OR%20%271" and "%27%20OR%20%27x%27%3d%27x"

---

## 4. Key Takeaways
- ✅ Log analysis is essential for identifying repeated malicious activity.  
- ✅ Decoding payloads helps confirm attacker intent.  
- ✅ HTTP responses and app behavior must be analyzed to determine attack success.  
- ✅ Not every malicious attempt results in compromise; validation is essential.  

---

## 5. Conclusion
The alert was a **false positive in terms of compromise**, but the structured investigation reinforced the importance of following SOC workflows:

**Alert → Log Review → Payload Analysis → Response Validation → Conclusion**

---

## 6. Skills Practiced
- Alert triage  
- Log analysis  
- Web application attack investigation (SQLi)  
- Response verification  
- SOC workflow adherence  

---


<h2>Screenshots Walk Through</h2>

<p align="center">
Event: <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/1.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
VirusTotal Verification:  <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/2.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Suspicious Request URL: <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/3.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/4.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Encoder/Decoder:  <br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/5.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br/>
<img src="https://github.com/aeronjlugtu/screenshots/blob/main/6.JPG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
