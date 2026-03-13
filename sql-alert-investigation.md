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

## 7. References / Notes
- Platform: LetsDefend  
- Related MITRE ATT&CK Technique: [T1190 – Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)  

---

## 8. Screenshots
Add your screenshots here. Upload them to a folder called `screenshots/` inside the repo. Example references:

```markdown
![Log Analysis](screenshots/log-analysis.png)
![Payload Decoding](screenshots/payload-decoding.png)
![HTTP Response](screenshots/http-response.png)
