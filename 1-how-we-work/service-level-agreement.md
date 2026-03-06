# 🚑 Service Level Agreement (SLA) & Incident Response

For clients engaged in a **Monthly Maintenance** or **Retainer** contract via Upwork, I provide guaranteed incident response times to ensure your production environments remain highly available.

This SLA outlines how incidents are classified and how quickly you can expect a response and remediation plan when things go wrong.

---

## 🚨 Incident Severity Levels & Target Response Times

I classify infrastructure issues into four severity levels. "Response Time" refers to the maximum time it will take for me to acknowledge the alert, begin investigating, and communicate with your team.

| Severity | Definition | Target Response Time | Target Update Frequency |
| :--- | :--- | :--- | :--- |
| **Sev 1 (Critical)** | **Production is down.** Complete outage of a critical system (e.g., database crashed, Kubernetes cluster unreachable, site offline). | **< 1 Hour** | Every 30 Minutes |
| **Sev 2 (High)** | **Severe degradation.** Core functionality is impacted, but the system is partially up (e.g., CI/CD pipeline blocked, high latency, failing deployments). | **< 4 Hours** | Every 2 Hours |
| **Sev 3 (Normal)** | **Non-critical issue.** Staging/Dev environment issues, minor bugs, or configuration changes needed. | **Next Business Day** | Daily |
| **Sev 4 (Low)** | **Requests & Maintenance.** General inquiries, architecture discussions, package updates, or new feature requests. | **2-3 Business Days** | As Needed |

---

## ⏰ Support Coverage Hours

*   **Standard SLA:** Covers Monday – Friday, 9:00 AM to 6:00 PM (Cairo Time / EET).
*   **24/7 Emergency SLA:** Available *only* via a premium, pre-negotiated retainer contract on Upwork. If 24/7 coverage is required, I must be integrated into your alerting stack (e.g., PagerDuty, Opsgenie, Datadog) to trigger automated phone calls for Sev 1 incidents.

## 🛠️ How to Report an Incident

To ensure SLA targets are met, incidents must be reported through agreed-upon channels:
1.  **Automated Alerts:** (Preferred) Alerts triggered by Datadog, CloudWatch, Prometheus, etc., routed directly to Slack/PagerDuty.
2.  **Direct Pinging:** A message in our dedicated Slack/Teams channel tagging me directly with the severity level (e.g., `@MyName [SEV 1] - Production DB Down`).
3.  **Upwork Messages:** For Sev 3 and Sev 4 issues. *(Note: Upwork messages are not actively monitored 24/7 for Sev 1 emergencies).*

## 🛑 SLA Exclusions

The following scenarios are exempt from SLA response guarantees:
*   **Application-Level Bugs:** If the infrastructure is healthy but your application code (Node.js, Python, PHP, etc.) is throwing 500 errors due to a bad code deployment by your developers.
*   **Third-Party Outages:** Outages caused directly by the cloud provider (e.g., AWS `us-east-1` going down) or SaaS tools (e.g., GitHub Actions being offline). I will still investigate and communicate this, but I cannot resolve AWS-level outages.
*   **Revoked Access:** If my IAM roles, VPN access, or GitHub permissions are revoked, modified, or expired, preventing me from accessing the environment.

---

*Note: This SLA goes into effect only after an architecture audit is completed and baseline monitoring/alerting tools are implemented.*