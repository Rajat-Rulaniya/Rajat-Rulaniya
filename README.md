<h1 align="center">Rajat Rulaniya</h1>

<p align="center">
  <b>DevOps & Cloud Engineer</b><br/>
  <em>I design and build end-to-end infrastructure, from CI/CD pipelines to Kubernetes clusters,<br/>with a strong focus on automation, security, and real-world reliability.</em>
</p>

---

## 🧠 About Me

**Systems-first mindset.** I don't rely on motivation, I build systems that guarantee execution.

- 🔧 I break complex systems into small, executable components and build them step by step
- 📚 Strong believer in **deep work** and **deliberate practice**. Long-term mastery over short-term results
- 🎯 I don't aim to *"learn DevOps"*. I aim to become someone who can **design, build, and operate real infrastructure**
- ⚡ I optimize for **consistency**, not intensity

---

## 🧰 Core Stack

| Category | Technologies |
|----------|-------------|
| **☁️ Cloud** | AWS (EKS, EC2, ECS, VPC, IAM, EBS, S3, RDS, Networking) |
| **🔄 CI/CD & GitOps** | Jenkins, GitHub Actions, ArgoCD |
| **📦 Containers & Orchestration** | Docker, Kubernetes, Helm |
| **🏗️ Infrastructure as Code** | Terraform |
| **🔒 Monitoring & Security** | Prometheus, Grafana, Trivy, SonarQube, GitLeaks |
| **💻 Languages & Systems** | Linux, Bash, Python, Go, Networking |

---

## 🏗️ Featured Projects

### 🚀 [DevSecOps End-to-End Pipeline](https://github.com/Rajat-Rulaniya/devsecops-end-to-end) &nbsp; <sub>`AWS` `EKS` `Jenkins` `ArgoCD` `Terraform` `Trivy` `SonarQube`</sub>

Production-grade DevSecOps pipeline for a 3-tier application. **Zero manual steps from commit to production.**

<details>
<summary><b>What I built  →</b></summary>
<br/>

- Complete **11-stage Jenkins CI pipeline** integrating secret scanning (GitLeaks), SAST (SonarQube), and vulnerability scanning (Trivy at filesystem + image level)
- **GitOps-based CD** using ArgoCD. CI never touches the cluster; image tags are updated in a [separate manifest repo](https://github.com/Rajat-Rulaniya/k8s-gitops-manifests), and ArgoCD syncs to EKS
- AWS infrastructure (**VPC + EKS + IAM + OIDC/IRSA + Nginx Ingress + cert-manager + ArgoCD**) provisioned using modular Terraform
- Automated Docker image build → Trivy scan → push to Docker Hub → update GitOps repo → ArgoCD deploy → Slack notification
- TLS automated via **Let's Encrypt** + cert-manager, ingress routing via Nginx

```
Push to main → Security Scans → Build & Scan Images → Update GitOps Repo → ArgoCD Syncs → Live in Production
```

</details>

---

### ⚙️ [Blue-Green Deployments on Kubernetes](https://github.com/Rajat-Rulaniya/prod-grade-cicd-k8s) &nbsp; <sub>`Jenkins` `Kubernetes` `Helm` `Docker` `Trivy`</sub>

Zero-downtime deployment system using **blue-green strategy** on Kubernetes with instant rollback.

<details>
<summary><b>What I built  →</b></summary>
<br/>

- **Independent CI/CD pipelines** for frontend (React) and backend (Spring Boot), each with their own Jenkinsfile
- Automated traffic switching using **Kubernetes Service selector patching**. Instant cutover, zero downtime
- **Helm charts** with color-scoped resources. Every Deployment and ConfigMap is namespaced by `blue` / `green`
- Security scanning with **pipeline-level enforcement**. Trivy blocks the release on HIGH/CRITICAL CVEs
- **Instant rollback**. No redeployment needed, just patch the Service selector back to the previous color
- Dedicated **Slack channels** per service (`#backend-alerts`, `#frontend-alerts`, `#security-alerts`)

```
Deploy to inactive color → Health check → Patch Service selector → Traffic switches instantly
Old color stays running → Rollback = one kubectl patch command
```

</details>

---

### ⚡ [Instant Kubernetes Cluster](https://github.com/Rajat-Rulaniya/instant-k8s-cluster) &nbsp; <sub>`Terraform` `Ansible` `Bash` `AWS`</sub>

**One-command** Kubernetes cluster provisioning system on AWS. Designed for learning and experimentation.

<details>
<summary><b>What I built  →</b></summary>
<br/>

- Fully automated cluster setup using **Terraform + Ansible + Bash**. Just run `./create_cluster.sh`
- Dynamic infrastructure: configurable **K8s version**, **node count**, **instance types** via variables
- Automated **kubeconfig** setup. Start running `kubectl` immediately after provisioning
- **Self-healing API server certificates**. Systemd service regenerates certs on instance restart
- Safe re-runs. Script checks Terraform state and exits if cluster already exists

```
./create_cluster.sh  →  Terraform provisions  →  Ansible configures  →  kubectl get nodes ✅
```

</details>

---

## 🧠 Deep Interests

- 🌐 Distributed systems and system design
- ☁️ Cloud architecture and scalability patterns
- ⚙️ Infrastructure automation at scale
- 🔐 DevSecOps: security baked into pipelines
- 🔍 Understanding how systems work under the hood

---

## 🎯 Direction

Focused on becoming a high-level **DevOps & Cloud engineer** capable of **designing and operating production systems from scratch**. Not just using tools, but **understanding how they work under the hood**.

Targeting engineering roles that value **depth**, **ownership**, and **real execution**.

---

## 🤝 Connect

- **LinkedIn** → [in/rajat-rulaniya](https://www.linkedin.com/in/rajat-rulaniya/)
- **X (Twitter)** → [@RajatRulaniya](https://x.com/RajatRulaniya)
- **Email** → [rajatrulaniya2005@gmail.com](mailto:rajatrulaniya2005@gmail.com)

---

<p align="center">
  <em>"I don't aim for motivation. I build systems that guarantee execution."</em>
</p>
