# Hi, I'm Chaewoon

**Cloud / DevOps / Platform Engineering**

I build and operate infrastructure around Kubernetes and AWS. My experience spans cluster bootstrap, networking, identity, storage, CI/CD, GitOps, recovery, and cost optimization across managed cloud, on-premises, and homelab environments.

I enjoy turning operational questions into systems that are repeatable, observable, and recoverable.

## Selected Work

### Hanbi — Kubernetes AI Education Platform

Built an on-premises Kubernetes platform with one teammate to make 32 NVIDIA RTX 5000 Ada GPUs across five physical servers available to students through browser-based Jupyter environments.

- Bootstrapped Kubernetes with kubeadm and containerd, then integrated Cilium, Longhorn, JupyterHub, Authentik, and Argo CD
- Configured network boundaries, per-student persistent storage, resource profiles, OIDC session invalidation, and container security controls
- Rebuilt the entire cluster, restored the Authentik database, and documented installation, recovery, and class-operation runbooks

### Hivewiki — AWS/EKS Capstone Infrastructure

Owned the AWS infrastructure for a three-person capstone team and received the Gold Award (2nd place) at Hallym University's Software Capstone Design.

- Shared one EKS control plane across dev and prod while separating scheduling, network, IAM, and data boundaries
- Automated off-hours hibernation and reboot of compute, database, cache, and network resources
- Against a monthly baseline estimate of more than $345, recorded an actual May cost of $206.14 and reported the reduction conservatively at approximately 35% after accounting for final shutdown days
- Investigated and fixed Cilium NetworkPolicy issues affecting the EKS Pod Identity link-local credential endpoint

[Infrastructure](https://github.com/Hallym-Workerbees/hivewiki-infra) · [GitOps](https://github.com/Hallym-Workerbees/hivewiki-gitops) · [Web](https://github.com/Hallym-Workerbees/hivewiki-web)

### CGV Infrastructure Project — CI/CD and GitOps

Designed and implemented a Tekton-based CI pipeline and Argo CD-based delivery flow for an AWS EKS microservices project.

- Reused parameterized Tekton Tasks across services written in different languages
- Stopped promotion before the GitOps `image.tag` update when SonarQube or Trivy checks failed
- Used SemVer plus commit SHA image tags, automatic sync for dev, and manual sync for prod and DR
- Developed a Go Ticket service using asynchronous events through Amazon MSK

[Team Repository](https://github.com/cloudwave-CGV/cloudwave-CGV) · [Ticket Service](https://github.com/fudoge/ticket-svc) · [Presentation](https://assets.chaewoon.work/cgv-cgip.pdf)

### AWS Serverless Multi-Region DR

Proposed and implemented an active-passive disaster recovery design for a university cloud-computing project. Route 53, API Gateway, Lambda, and DynamoDB Global Tables kept a single client domain while failing over between Seoul and Tokyo.

- Validated failover and failback using actual API responses under the same domain
- Observed approximately 1–2 minutes for both transitions
- Kept regional failover logic out of the Android application

[Implementation Notes](https://blog.chaewoon.work/ko/p/aws-route53--api-gateway%EB%A1%9C-dr-failover%EA%B5%AC%EC%84%B1%ED%95%98%EA%B8%B0/)

### Homelab and Network Experiments

I run self-hosted services and am rebuilding the environment around Proxmox, OpenTofu, NixOS, k3s, Flux, and Cilium. The lab is where I practice backup and restore, GitOps recovery, remote access design, and Kubernetes networking through reproducible experiments.

[Home Infrastructure (v1, archived)](https://github.com/fudoge/home-infra) · [Homelab (current)](https://github.com/fudoge/homelab)

## Technologies

| Area | Tools and platforms |
| --- | --- |
| Cloud & Platform | AWS, EKS, Kubernetes, kubeadm, k3s, Proxmox |
| Networking & Storage | Cilium, Gateway API, BGP/FRR, Longhorn, Tailscale |
| IaC & Configuration | OpenTofu, Terraform, Terragrunt, Ansible, Nix |
| CI/CD & GitOps | Argo CD, Tekton, Flux, GitHub Actions, pre-commit |
| Observability & Security | Prometheus, Grafana, Loki, Hubble, Trivy, SonarQube, Falco, SOPS |
| Systems & Programming | Linux, containerd, Docker, Go, Python, Bash |

## Certifications

[CKA](https://www.credly.com/badges/2ddaf836-1b25-4c29-becc-22b2cf78d4f7/public_url) · [CKAD](https://www.credly.com/badges/09742ed1-3318-46e7-b81f-5da98e28ce06/public_url) · [CKS](https://www.credly.com/badges/b4029b46-734a-4ff8-9c6c-4f5da2f65e6a/public_url) · [AWS Solutions Architect – Associate](https://www.credly.com/badges/a0cb166b-4cb5-4f8d-a40a-b2bf3b7e444d/public_url)

TOEIC Speaking IH

## Education

- Hallym University — expected graduation in February 2027
- CJ OliveNetworks Cloud Wave 6th — 400-hour training program

## Links

[Blog](https://blog.chaewoon.work) · [Solved.ac](https://solved.ac/profile/chaewoon67) · [LeetCode](https://leetcode.com/u/fudoge/)
