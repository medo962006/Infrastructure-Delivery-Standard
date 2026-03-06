# ⚖️ Terms & Conditions of Service

To ensure a smooth, professional, and highly productive working relationship, I adhere to the following Terms and Conditions for all Upwork engagements. 

These terms are designed to protect both your business and my time, ensuring that the focus remains entirely on delivering high-quality DevOps engineering.

---

## 1. 📢 Communication
*   **Primary Channel:** All official contract milestones, payments, and major project approvals must be conducted via the **Upwork Messages** platform to comply with Upwork's Terms of Service.
*   **Day-to-Day Chat:** I am happy to join your company's Slack, Microsoft Teams, or Discord for day-to-day engineering communication once the Upwork contract is active.
*   **Response Time:** During my standard working hours, I aim to respond to all non-emergency messages within **4 to 6 hours**. 

## 2. 🌍 Working Hours & Availability
*   **Standard Hours:** My standard working hours are **Monday through Friday, 9:00 AM to 6:00 PM (GMT+2)**. 
*   **Meetings:** I am highly flexible and can schedule video calls (Zoom, Google Meet, Microsoft Teams) that overlap with your timezone (EST, PST, CET, etc.) with at least 24 hours of notice.
*   **Weekends & Holidays:** Unless we have an active [Service Level Agreement (SLA)](./service-level-agreement.md) for emergency production support, weekend work is not guaranteed and must be negotiated in advance.

## 3. 🛡️ Production Environments & Risk
*   **No Direct Production Changes:** As a strict rule, I do not make manual, unrecorded changes directly to production environments. All changes must go through Infrastructure as Code (Terraform/CloudFormation) or CI/CD pipelines.
*   **Testing & Staging:** I require access to a staging or development environment to validate all deployments before they are promoted to production.

## 4. 🛑 Scope Creep & Revisions (Fixed-Price)
*   **Defined Scope:** For fixed-price contracts, the deliverables will be explicitly defined in a Statement of Work or the Upwork Milestone description.
*   **Out of Scope:** If a new feature or infrastructure requirement is requested that was not in the original scope, I will flag it as "Out of Scope." We can then add a new milestone or switch to an hourly contract to accommodate the new requirements.
*   **Revisions:** Fixed-price milestones include **two (2) rounds of minor architectural/code revisions**. Complete redesigns of agreed-upon architectures will require a new milestone.

## 5. 💻 Code Ownership & Intellectual Property
*   Upon the successful completion of the project and full release of funds via Upwork, **100% of the Intellectual Property (IP), code, and infrastructure configurations** are transferred to you, the client.
*   I will never reuse your proprietary application code or expose your business logic. 
*   *Note: I reserve the right to reuse generalized, open-source DevOps boilerplates (e.g., standard VPC Terraform modules, standard Dockerfiles) across multiple projects, as these do not contain sensitive client data.*

## 6. 🔒 Security & Access
*   I strictly adhere to the Principle of Least Privilege (PoLP). I will only request the exact IAM permissions, GitHub access, and server access required to complete the job. 
*   For detailed access requirements, please see my [Access Requirements Guide](../2-security-and-compliance/access-requirements.md).