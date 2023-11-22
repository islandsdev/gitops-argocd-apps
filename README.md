# gitops-argocd-apps

### Overview

#### ArgoCD Application Objects

```
argocd/
├── dev
│   ├── backend
│   │   ├── ameego.yml
│   │   ├── analytics.yml
│   │   ├── api.yml
│   │   ├── caput.yml
│   │   ├── cortex.yml
│   │   ├── doordash.yml
│   │   ├── grubhub.yml
│   │   ├── hermes.yml
│   │   ├── hippo-executor.yml
│   │   ├── hippo-scheduler.yml
│   │   ├── hippo-server.yml
│   │   ├── olo.yml
│   │   ├── skip.yml
│   │   ├── socket.yml
│   │   └── uber.yml
│   ├── frontend
│   │   ├── customer.yml
│   │   └── merchant.yml
│   └── ingress.yml
└── prod
```

#### Kustomize Folder Structure

```
kustomize
├── dev
│   └── mentum-eks-cluster-dev
│       ├── backend
│       │   ├── ameego
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── externalSecret.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── analytics
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── externalSecret.yml
│       │   │   │   ├── ingress.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── api
│       │   │   ├── base
│       │   │   │   ├── configMap.yml
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── externalSecret.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── caput
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── cortex
│       │   │   ├── base
│       │   │   │   ├── configMap.yml
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── doordash
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── externalSecret.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── grubhub
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── externalSecret.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── hermes
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── externalSecret.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── hippo-executor
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── hippo-scheduler
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── hippo-server
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── olo
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── skip
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── externalSecret.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   ├── socket
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   └── uber
│       │       ├── base
│       │       │   ├── deployment.yml
│       │       │   ├── externalSecret.yml
│       │       │   ├── kustomization.yml
│       │       │   ├── podDisruptionBudget.yml
│       │       │   └── service.yml
│       │       └── kustomization.yml
│       ├── frontend
│       │   ├── customer
│       │   │   ├── base
│       │   │   │   ├── deployment.yml
│       │   │   │   ├── kustomization.yml
│       │   │   │   ├── podDisruptionBudget.yml
│       │   │   │   └── service.yml
│       │   │   └── kustomization.yml
│       │   └── merchant
│       │       ├── base
│       │       │   ├── deployment.yml
│       │       │   ├── kustomization.yml
│       │       │   ├── podDisruptionBudget.yml
│       │       │   └── service.yml
│       │       └── kustomization.yml
│       └── ingress-static-file
│           └── ingress.yml
└── prod
    └── mentum-eks-cluster-prod
```
