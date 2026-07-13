# Creating the markdown file with the provided study notes formatted beautifully
markdown_content = """# AWS Identity and Access Management (IAM) — Core Study Notes

A comprehensive reference guide for the AWS Certified Solutions Architect - Associate (SAA) exam.

---

## 🔐 Authentication vs. Authorization

Understanding the difference between these two foundational pillars is crucial for securing AWS environments.

### 1. Authentication
* **Definition:** The process of proving your identity ("Who are you?").
* **Analogy:** > You say: *"I'm Gerard."* > AWS responds: *"Prove it."* > You provide your password ✅.
* **Common Examples:**
  * Username + Password (AWS Management Console)
  * Access Key ID + Secret Access Key (AWS CLI / SDK / API)
  * Multi-Factor Authentication (MFA) tokens

### 2. Authorization
* **Definition:** The process of determining what you are allowed to do once your identity is verified ("What can you do?").
* **Analogy:** > Once AWS knows you are Gerard, it evaluates:  
  > * Can Gerard launch an EC2 instance? ➡️ **YES** > * Can Gerard delete IAM users? ➡️ **NO**
* **Mechanism:** Permissions in AWS are defined and granted using **Policies**.

---

## 🏛️ IAM Hierarchy & Core Components

AWS Identity and Access Management (IAM) is structured around four foundational pillars:

```text
IAM Architecture
├── 👤 Users    (Permanent identity for a person or application)
├── 👥 Groups   (Collections of users for easy permission management)
├── 🎭 Roles    (Temporary identities for services or cross-account access)
└── 📄 Policies (JSON documents defining permitted or denied actions)
