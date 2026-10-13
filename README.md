# Hi, I'm Robert Carlson 👋
### Platform & DevOps Engineer

I am a Platform and DevOps Engineer with over 10 years of experience building reproducible, self-service infrastructure, robust CI/CD pipelines, and secure cloud-native developer ecosystems. I focus on bridging the gap between infrastructure stability and developer velocity.

---

## 🏗️ Featured Platform Ecosystem

Instead of isolated repositories, my public work demonstrates a cohesive, layered cloud platform architecture emulated completely at **zero cost** on a local development environment (Windows 11 WSL2 Ubuntu).

### 1. [Internal Developer Platform (IDP) Core](https://github.com)
*The Application & Control Plane Layer*
*   **Cluster Orchestration:** Local multi-node Kubernetes provisioning using `k3d`.
*   **GitOps Delivery Engine:** Declarative application deployment powered entirely by `Argo CD`.
*   **Developer Abstractions:** Using `Crossplane` to manage dynamic, per-request infrastructure behind clean API boundaries (XRDs).
*   **Platform Governance:** Policy enforcement via `Kyverno` (v1.19.1) utilizing `ImageValidatingPolicy` for container security.
*   **Secrets Architecture:** Dynamic secrets injection powered by the `External Secrets Operator (ESO)` and `HashiCorp Vault`.

### 2. [Platform-as-Code (PaC) Foundations](https://github.com)
*The AWS Landing Zone Layer*
*   **Foundational IaC:** Multi-environment (`dev` and `staging`) foundation layers built with highly reusable `Terraform` modules.
*   **Zero-Cost Emulation:** Local AWS-shaped infrastructure (VPC networking, IAM, S3 storage) validated against a local emulator container.
*   **State & Locking Management:** Robust remote state management using emulated S3 buckets and DynamoDB locking tables, isolated outside the cluster to ensure state resilience.
*   **Shift-Left Guardrails:** Automated GitHub Actions workflows running `terraform fmt`, `tflint`, security scans, and `terraform test` using mock providers.

---

## ⚖️ The Architectural Boundary

My platform design strictly separates operational concerns to mirror modern corporate scaling strategies:
*   **Terraform:** Owns slow-changing foundations (VPCs, IAM frameworks, base S3 storage buckets) run by platform engineers.
*   **Crossplane:** Owns fast, dynamic, per-request developer resource instantiation.
*   **Argo CD:** Owns the absolute state of what is running inside Git.

---

## 🛠️ Technical Toolkit

*   **Orchestration & Runtime:** Kubernetes, k3d, Docker Desktop
*   **Infrastructure as Code & GitOps:** Terraform, Argo CD, Crossplane, Helm
*   **Security & Policy:** Kyverno, HashiCorp Vault, External Secrets Operator (ESO), Keyless Container Signing
*   **CI/CD & Automation:** GitHub Actions, Bash, Go, Package Managers (`Yarn v4.4.1`, `apt`, `yum`)
*   **Environments:** Linux (Ubuntu), Windows 11 WSL2, VS Code

---

## 📈 Engineering Philosophies

*   **Infrastructure Identity:** If it isn't in Git, it doesn't exist.
*   **Engineering Honesty:** Emulators are fantastic for syntax, module paths, and local feedback loops, but true engineering maturity means recognizing where simulation ends and real cloud guardrails (real IAM, network charges, regional quotas) begin.

📫 **Connect with me:** [robertcarlson2056@gmail.com](mailto:robertcarlson2056@gmail.com)
