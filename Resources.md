# 📚 Resources – Task 2: Security Alert Monitoring & Incident Response

This document contains links, tutorials, and documentation referred to during the completion of Task 2 under the Cybersecurity Internship at Future Interns.

---

## 🔧 Tools Used

- **Splunk Cloud (Free Trial):**  
  https://www.splunk.com/en_us/download/splunk-cloud.html

- **Splunk Search & Reporting App:**  
  Used for analyzing logs, running SPL queries, and building dashboards.

---

## 📑 Tutorials & Guides

- **Intro to SIEM and Log Analysis for Beginners:**  
  https://www.youtube.com/watch?v=vfN5tBK9c3c  
  *(Used to understand SIEM workflow and basic Splunk interface.)*

- **Splunk Docs – Search Tutorial:**  
  https://docs.splunk.com/Documentation/Splunk/latest/SearchTutorial/WelcometotheSearchTutorial

- **Splunk Search Reference (SPL commands):**  
  https://docs.splunk.com/Documentation/Splunk/latest/SearchReference/Search

- **Elastic Stack Overview (Alternative SIEM platform):**  
  https://www.elastic.co/what-is/elk-stack

---

## 🔐 Cybersecurity References

- **SOC Analyst Learning Path:**  
  https://tryhackme.com/path/outline/soc-level1

- **MITRE ATT&CK Framework:**  
  https://attack.mitre.org/

- **Incident Response Lifecycle – NIST SP 800-61:**  
  https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf

---

## 📌 Queries Used

```spl
index=_internal error OR fail OR login | table _time, host, source, sourcetype, log_level
spl
Copy
Edit
index=_internal sourcetype="splunkd" log_level="ERROR" | stats count by host
✅ Outcome
These resources helped with:

Log analysis and triage

Query building in Splunk SPL

Writing a structured Incident Response Report

Understanding how SIEM platforms operate in real-world SOC environments
