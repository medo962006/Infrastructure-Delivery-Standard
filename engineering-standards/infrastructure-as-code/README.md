# 🏗️ Infrastructure as Code (IaC) Standards

I believe that manual infrastructure setup (Click-Ops) is a major liability. To ensure scalability, repeatability, and security, I exclusively use **Infrastructure as Code (IaC)**.

This repository serves as a library of my production-grade, battle-tested templates. When you hire me, you aren't paying for me to write Terraform from scratch; you are paying for the implementation of these hardened, security-focused modules.

---

## 🛠️ My IaC Philosophy
*   **Modularity:** Infrastructure is broken down into small, reusable components (e.g., a VPC module, an EKS cluster module, an RDS module).
*   **Security-First:** Every template includes built-in security groups, KMS encryption, and resource tagging by default.
*   **Version Control:** All infrastructure changes are tracked in Git, peer-reviewed via Pull Requests, and deployed through CI/CD pipelines.
*   **State Management:** I utilize remote backends (e.g., S3 + DynamoDB) to ensure team collaboration and state locking.

## 📂 Boilerplate Library
In this section, you will find examples of my standard modules:

*   [**Secure AWS VPC Module**](./terraform-aws-vpc/): A highly-available, multi-AZ VPC design including Public/Private subnets, NAT Gateways, and flow logging.
*   [**Standard EKS Cluster**](./terraform-eks/): A production-ready Kubernetes cluster setup including managed node groups, OIDC providers, and IAM roles for service accounts (IRSA).
*   [**Hardened RDS Module**](./terraform-rds/): A private RDS instance with encryption at rest, automated backups, and restricted security groups.

---

### 💡 Why does this matter for your business?
By using these pre-vetted modules, we drastically reduce the chance of human error and deployment time. We can spin up an entire production-ready environment in hours, not weeks, with the confidence that the architecture follows industry best practices.

*Note: These are generalized templates. During our project, I will tailor them to meet your specific networking, scale, and compliance requirements.*