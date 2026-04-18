# tfm-gitops

GitOps repository used in the final master's project focused on implementing a secure DevSecOps lifecycle on Kubernetes.

## Project Overview

This repository stores the declarative configuration of the Kubernetes platform, including:

* Kyverno security policies (Policy-as-Code)
* Demo workloads for validation and testing
* ArgoCD Applications for continuous delivery
* Kubernetes manifests managed through GitOps

The goal is to demonstrate how security controls can be integrated into a CI/CD pipeline using:

* **GitHub Actions** for Continuous Integration
* **Trivy** for vulnerability scanning
* **ArgoCD** for Continuous Delivery (GitOps)
* **Kyverno** for admission control and automatic hardening
* **Kubernetes** as execution platform

---

## Repository Structure

```text
tfm-gitops/
├── policies/        # Kyverno ClusterPolicies
├── applications/    # Demo workloads
└── argocd/          # ArgoCD Application manifests
```

---

## Security Model

This repository acts as the single source of truth for the cluster desired state.

Any modification to policies, workloads or manifests must be versioned in Git and automatically synchronized to the cluster by ArgoCD.

This enables:

* Traceability of changes
* Automatic reconciliation
* Drift correction
* Secure-by-default deployments

---

## Example Policies Included

* Disallow root containers
* Disallow privilege escalation
* Restrict untrusted image registries
* Inject default resources
* Inject secure securityContext
* Enforce read-only root filesystem
* Auto-generate NetworkPolicies

---

## Academic Context

This repository supports the practical implementation of a TFM focused on DevSecOps, Kubernetes security and Policy-as-Code.

---

## Author

Ziad El Karrabi El Hanafi
