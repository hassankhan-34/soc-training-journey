# SOC Alert Classification & Severity Guidelines

## 1. Alert Severity Levels
* **Critical:** Active, high-impact compromise in progress (e.g., successful ransomware execution, active data exfiltration, or domain controller compromise). Requires immediate containment.
* **High:** Significant malicious activity detected that poses an immediate risk (e.g., confirmed brute-force success, credential dumping, or known malware execution).
* **Medium:** Suspicious activity or policy violations that require investigation but lack immediate proof of full system compromise (e.g., port scans, unusual administrative scripts, or repeated failed logins).
* **Low:** Anomalous or low-risk events that deviate from baseline behavior but show no indicators of malicious intent (e.g., rare application usage or unrecognized device connection).

## 2. Alert Classifications
* **True Positive (TP):** 
  * *Definition:* The alert accurately represents actual malicious activity, a real security incident, or an unauthorized policy violation.
  * *Action:* Proceed to containment, investigation, and incident documentation.

* **False Positive (FP):** 
  * *Definition:* The alert was triggered by benign or authorized activity (e.g., a vulnerability scanner, system administrator testing, or legitimate software behavior) that matched a detection rule.
  * *Action:* Document the root cause and create tuning/exclusion notes to reduce noise.

* **Benign / Expected (True/False Hybrid):** 
  * *Definition:* The event occurred exactly as flagged, but it is known to be harmless, authorized business logic, or standard user behavior.
