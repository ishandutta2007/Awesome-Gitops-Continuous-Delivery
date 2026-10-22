# Awesome-Gitops-Continuous-Delivery

## Top GitOps & Continuous Delivery Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Declarative Deployments, Kubernetes Reconciliation & Self-Hosted Delivery Pipelines*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **GitOps & Continuous Delivery**. These tools enable teams to declare their desired infrastructure and application state in Git, then continuously reconcile the live environment to match—providing auditability, rollback capability, and drift detection without manual deployment steps.



**Examples** include Argo CD, Flux, Harness, GitLab CI/CD, Octopus Deploy, Codefresh, Spinnaker, GitHub Actions, AWS CodePipeline, and CircleCI (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, Kubernetes-native reconciliation, and transparent delivery pipelines—ideal for platform teams that need data sovereignty, avoid per-seat SaaS pricing, and require auditable deployment workflows. The open-source GitOps landscape is anchored by **Argo CD** (the UI-rich multi-cluster standard) and **Flux** (the lightweight Kubernetes-native operator), both CNCF Graduated projects, with **Konflux** emerging as a supply-chain-trust-focused alternative built on Tekton.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global Continuous Delivery and GitOps market is estimated between **$3.8 billion and $5.5 billion** in 2026, growing at a robust ~17–19% CAGR toward an estimated $18+ billion by 2034. The sector exhibits a **moderately fragmented and hybrid market structure**: hyperscalers and all-in-one developer platforms (Microsoft/GitHub, GitLab, AWS) dominate enterprise mindshare and consolidated CI/CD spend, while specialized continuous delivery, Kubernetes reconciliation, and GitOps workflows remain highly fragmented and distributed across innovative venture-backed platforms and open-source standards.



## SaaS/Hosted Platforms

| Company / Product | Company Size (Valuation / Revenue) | Starting Pricing (Paid Tier) | Free Tier / Trial Limits | Key Focus & Deployment Strengths |
| :--- | :--- | :--- | :--- | :--- |
| **[GitHub Actions](https://github.com/features/actions)** | ~$3.95T Market Cap *(Microsoft)* / $1B+ ARR *(GitHub)* | **$4/user/month** *(Team plan; $0.008/min for additional Linux build minutes)* | **Free forever plan**: Unlimited minutes on public repositories; 2,000 Linux runner minutes/month & 500 MB storage on private repositories. | Deep GitHub repo integration, expansive actions ecosystem, and native hosted runners. |
| **[AWS CodePipeline](https://aws.amazon.com/codepipeline/)** | ~$2.82T Market Cap *(Amazon)* / $100B+ Run Rate *(AWS)* | **$1.00/active pipeline/month** *(V1; free for first 30 days)* or **$0.002/action min** *(V2)* | **Free forever plan**: 1 free active pipeline/month (V1) or 100 free action execution minutes/month (V2 across account). | Managed AWS-native delivery pipelines with deep IAM, ECS, EKS, and Lambda integration. |
| **[GitLab CI/CD](https://about.gitlab.com/)** | ~$9.0B Market Cap / ~$955M ARR *(FY2026)* | **$29/user/month** *(Premium tier, billed annually)* | **Free forever plan**: 400 compute runner minutes/month, 5 users per namespace, and 10 GiB storage. | Comprehensive DevSecOps platform with source code management, container registry, and auto-devops. |
| **[Harness](https://www.harness.io/)** | $5.5B Valuation *(Series E)* / $250M+ ARR | **$40/developer/month** *(Essentials / Team tier; modular Developer 360 baseline)* | **Free forever plan**: 2,000 Harness Cloud Credits/month, 1,000 free monthly HSUs, limited to 2 developers & 60 pipeline concurrency. | AI-driven continuous delivery, automated canary verification, GitOps management, and governance. |
| **[CircleCI](https://circleci.com/)** | $1.7B Valuation *(Series F)* / ~$56M Annual Revenue | **$15/month** *(Performance plan, includes 5 active users and 30,000 monthly credits)* | **Free forever plan**: 30,000 credits/month (~3,000 default Linux build mins), up to 5 users, and 30 concurrent jobs. | Fast build pipelines, extensive caching, Docker layer caching, and flexible cross-platform runners. |
| **[Octopus Deploy](https://octopus.com/)** | ~$625M Valuation / $83.4M ARR | **$8.67/project/month** *($104/project/year on Professional tier, billed annually)* | **Free forever plan**: 10 projects, 10 users, 10 deployment target machines, and 10 tenants. | Complex multi-environment deployment orchestration, runbook automation, and unified Argo CD GitOps layer. |
| **[Codefresh](https://codefresh.io/)** | ~$50M Valuation *(Acquired by Octopus Deploy)* | **$99/user/month** *(Team tier; or custom enterprise contract)* | **Free forever plan**: 1 concurrent build slot with community runner limits; plus 14-day full-feature trial on request. | Kubernetes-native container pipeline CI engine with deep GitOps workflow synergy. |
| **[Spinnaker (Hosted via OpsMx)](https://www.opsmx.com/)** | OpsMx: $22M Raised / ~$22M Revenue *(Spinnaker: Netflix open-source)* | **Custom quote-based** *(Enterprise contract based on target clusters & deployment volume)* | **Free trial**: 14-day guided proof-of-concept / SaaS evaluation upon request; open-source core is 100% free self-hosted. | Enterprise multi-cloud continuous delivery at massive scale with automated verification and canary deployment. |

## Open-Source GitHub Projects



- **[Argo CD](https://github.com/argoproj/argo-cd)**  

  The leading GitOps continuous delivery tool for Kubernetes. **Purpose-built for CD with a polished UI**, multi-cluster visibility, and flexible manual sync controls . Uses pull-based in-cluster controllers that continuously reconcile Git state with cluster state. Supports Helm and Kustomize, integrates with Sealed Secrets, SOPS, and Vault for secret management . **CNCF Graduated** and production-safe. Best for teams that want a web UI, ApplicationSets for multi-cluster deployment, and explicit sync control with visual diff.



- **[Flux](https://github.com/fluxcd/flux2)**  

  Open and extensible continuous delivery solution for Kubernetes. **Lightweight, Kubernetes-native operator** following controller patterns, with a CLI-first workflow and native Helm/OCI handling . Composable controllers mean you use only what you need. **CNCF Graduated** and production-safe. Integration with SOPS, Sealed Secrets, and Vault. **Trade-off vs Argo CD**: no built-in UI by default (Weave GitOps provides one), but smaller footprint and tighter alignment with Kubernetes conventions. Best for platform teams that want a minimal, composable GitOps engine without UI overhead.



- **[Konflux](https://github.com/konflux-ci/konflux-ci)**  

  Open-source, Kubernetes-native CI/CD platform with **supply chain trust built in from the start**. Built on Tekton and Conforma, it produces signed container images with SBOMs, SLSA provenance attestations, and policy gates before release . Runs on Kind, OpenShift, or any conformant Kubernetes cluster—full instance on a local Kind cluster in minutes . Apache 2.0 licensed. Integrates Buildah, Sigstore, Clair, Quay, and Renovate out of the box . Best for organizations that need software supply chain security (SLSA, SBOM, signing) as a first-class feature rather than an add-on.



### Additional Strong Open-Source Options



- **Jenkins X** — CI-driven GitOps platform with integrated pipelines and preview environments. Uses a push model (pipeline applies changes) rather than continuous reconciliation, making it less "pure GitOps" than Argo CD or Flux . Best for teams that want an integrated CI/CD experience with GitOps-style deployment.

- **Tekton** — Kubernetes-native CI/CD building blocks. The foundation under Konflux, but usable directly for custom pipelines. Best for platform teams building bespoke delivery systems.

- **Frameworks for building custom systems**: Use **Argo CD** for UI-driven multi-cluster GitOps with visual sync control. Choose **Flux** for a lightweight, CLI-first operator that follows Kubernetes conventions. Add **Konflux** when supply chain security (SLSA provenance, SBOM, signing) must be enforced in the pipeline. For CI, pair with **GitHub Actions** or **GitLab CI/CD** depending on your repository platform.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- **Argo CD vs Flux**: Both are CNCF Graduated and production-safe. Argo CD offers a richer UI and more explicit sync control; Flux is lighter, more composable, and CLI-native . The choice often comes down to whether your team wants a visual dashboard or a minimal operator.

- **Codefresh's GitOps features have moved to Octopus Deploy**; evaluate Octopus if you were considering Codefresh for Argo CD-based CD .

- Harness paid plans are quote-only; published capacity ceilings (not prices) are available for sizing without a sales call .

- Self-hosted GitOps requires proper RBAC, secret management (SOPS/Sealed Secrets/Vault), and drift detection configuration.



---



**Made for platform engineers, DevOps teams, SREs, and organizations building auditable, declarative delivery pipelines.**  

Let's make GitOps and continuous delivery more open, trustworthy, and self-determinable.
