# Task 2 – Security Alert Monitoring & Incident Response (FUTURE_CS_02)

This repository contains all work related to **Task 2** of the Cyber Security Internship by Future Interns.

The task simulates the responsibilities of a SOC (Security Operations Center) analyst:  
Monitoring logs, analyzing security alerts, and drafting a professional incident response report using Splunk.

---

## 📌 Deliverables

| File / Folder              | Description |
|---------------------------|-------------|
| `Incident_Response_Report.pdf` | A complete Incident Response Report including screenshots, SPL queries, alert classification, and mitigation steps. |
| `alert_search_query.png`       | Screenshot of Splunk SPL query used to identify suspicious login attempts or alert patterns. |
| `failed_logins_dashboard.png`  | Screenshot showing frequency of error logs from the Splunk internal index — mimicking repeated failed logins or system alerts. |
| `Tools_Used.txt`               | List of tools used during this task: Splunk Cloud, search SPL, documentation. |
| `Resources.md`                 | Learning links and resources used to understand SIEM tools and incident response strategies. |
| `Screenshots/`                | Directory containing supporting evidence of searches performed. |
| `soc_sample_logs`             | Sample logs analyzed. (If upload was restricted in Splunk Cloud, internal logs were used instead.) |

---

## 🔧 Tools Used

- Splunk Cloud Platform (Free Trial)
- SPL (Search Processing Language)
- Git & GitHub

---

## 🔍 Key SPL Queries Used

```splunk
index=_internal error OR fail OR login | table _time, host, source, sourcetype, log_level

index=_internal sourcetype="splunkd" log_level="ERROR" | stats count by host
