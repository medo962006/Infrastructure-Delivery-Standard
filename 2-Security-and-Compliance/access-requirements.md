# 🔑 Access & Provisioning Requirements

To ensure a secure and efficient kickoff, I have standardized the access I require to begin your DevOps or Cloud Engineering project. 

I strictly adhere to the **Principle of Least Privilege**. Please review the requirements below based on the type of work we are doing.

---

## 1. Cloud Provider Access (AWS/GCP/Azure)
*   **Preferred Method:** Create a dedicated **IAM User** or **IAM Role** for me with strictly scoped permissions. 
    *   *Note:* Avoid sharing your "Root" account credentials.
*   **Required Permissions:** 
    *   For Infrastructure as Code (Terraform/CloudFormation): I need permission to Create/Read/Update/Delete (CRUD) the specific resources we are building (e.g., VPC, EC2, RDS, EKS).
    *   For Troubleshooting/Audit: "Read-only" or "View" access is usually sufficient.
*   **Multi-Factor Authentication (MFA):** Please ensure MFA is enabled on the account I am accessing.

## 2. Source Control & CI/CD (GitHub/GitLab/Bitbucket)
*   **Repository Access:** Please invite me as a **Collaborator** or grant me **Read/Write access** to the specific repositories involved in the project.
*   **Secret Management:** I will guide you on how to add necessary API keys or Cloud credentials to your Repository Secrets so that I can configure your CI/CD pipelines without ever seeing your actual production passwords.

## 3. Server/Compute Access (EC2/Droplets/VPS)
*   **SSH Access:** Please provide an SSH key or add my public key to the server's `~/.ssh/authorized_keys` file.
*   **Alternative (Preferred for AWS):** If we are using AWS, **Systems Manager (SSM) Session Manager** is the industry standard. It allows me to access your instances securely through the AWS Console/CLI without needing to manage open SSH ports (port 22) or handle SSH keys.

## 4. Communication & Project Tools
*   **Slack/Teams:** Please invite me to your relevant engineering or project channels.
*   **Project Management:** Please grant access to your Jira, Trello, or Linear board so I can track my tasks against your project milestones.

---

## 🛑 Important Security Note
*   **Do not send credentials via Upwork Messages:** Please do not send passwords, SSH private keys, or secret keys directly in the chat.
*   **How to share securely:**
    1.  Use **[1Password](https://1password.com/)**, **[Bitwarden](https://bitwarden.com/)**, or **[Passbolt](https://www.passbolt.com/)** to share credentials securely.
    2.  Use a **temporary, time-limited password link** (e.g., [Bitwarden Send](https://bitwarden.com/products/send/)).
    3.  Grant access directly via the Cloud Provider's IAM console using my email address.

**If you have questions about which permissions are appropriate for our project, let's discuss this during our Kickoff call!**