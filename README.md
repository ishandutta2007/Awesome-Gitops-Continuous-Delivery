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

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Harness](https://www.harness.io/)**  

  Modular DevOps platform covering CI, CD & GitOps, IaC Management, and Security Testing Orchestration. **Pricing is opaque**: paid plans require contacting sales, with documented capacity ceilings (Essentials: 60 concurrent pipelines, 500 users; Enterprise: 500 pipelines) . Third-party data shows first-time buyers often achieve 20–30% off initial quotes, and enterprise buyers can negotiate 30–40% below list with multi-year commitments . Best for organizations that want an integrated platform with strong governance and are prepared for enterprise sales cycles.



- **[GitLab CI/CD](https://about.gitlab.com/)**  

  Integrated DevOps platform with native CI/CD, container registry, and security scanning. **Premium tier at $29/user/month** (annual) with 10,000 compute minutes; Ultimate adds compliance and security features at custom pricing . The self-managed edition is a first-class target, with mature runner infrastructure and parent-child pipelines for monorepos . Best for teams that want a single platform for code, CI, and CD with self-hosting options.



- **[Octopus Deploy](https://octopus.com/)**  

  Dedicated CD platform for complex deployments. **Free tier**: 10 projects, 10 users, 10 machines. **Professional**: ~$4,330/year for 20 projects. **Enterprise**: ~$24,600/year for 100 projects . Note: **Argo CD and Kubernetes CD features have moved to Octopus Deploy** from Codefresh, making it the destination for Codefresh GitOps users . Best for organizations that need deployment orchestration across mixed environments (VMs, Kubernetes, databases) with runbook automation.



- **[Codefresh](https://codefresh.io/)**  

  CI platform with strong Kubernetes integration and container-based pipelines. **Important transition**: GitOps-powered deployments, Argo CD, and advanced Kubernetes delivery have **moved to Octopus Deploy**—Codefresh now focuses on CI . Users report a learning curve but praise the pipeline flexibility and native K8s support . Best for teams that need container-focused CI without the full Octopus CD layer.



- **[Spinnaker](https://spinnaker.io/)**  

  Open-source multi-cloud continuous delivery platform originally from Netflix. **Release 2026.3.0** (September 2026) includes AWS SDK v2 migration and fixes for large YAML handling . Primarily self-hosted, though commercial support exists. Best for large enterprises with multi-cloud deployment needs and dedicated platform teams.



- **[GitHub Actions](https://github.com/features/actions)**  

  CI/CD integrated into GitHub. **Pricing update**: GitHub-hosted runner prices dropped up to 39% on January 1, 2026. A proposed $0.002/minute charge for self-hosted runners was **postponed** after community feedback . Free minutes remain for public repos. Best for teams already on GitHub that want tight code-to-pipeline integration.



- **[AWS CodePipeline](https://aws.amazon.com/codepipeline/)**  

  Fully managed continuous delivery service on AWS. Pay-per-use with no upfront fees . Integrates with CodeBuild, CodeDeploy, and third-party tools. **Note**: AWS has restricted new customer access to CodeCommit; verify CodePipeline availability for your account before selecting. Best for AWS-native architectures.



- **[CircleCI](https://circleci.com/)**  

  CI/CD platform with **credit-based pricing**. Free tier includes 30,000 credits/month (expiring monthly); Performance plan allows purchasing additional credits at $15 per 25,000 credits, which roll over for a year . Supports Docker, Linux VM, Windows, macOS, and GPU execution environments. Best for teams that need flexible compute options and are comfortable with credit-based cost management.



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
