# gitops-argocd-apps

### Overview

#### ArgoCD Application Objects

```
argocd
├── api.yml
├── customer.yml
├── ingress.yml
├── merchant.yml
├── socket.yml
└── uber.yml
```

#### Kustomize Folder Structure

```
kustomize
├── dev
│   └── mentum-eks-cluster-dev
│       ├── backend
│       │   ├── api
│       │   ├── doordash
│       │   ├── grubhub
│       │   ├── skip
│       │   ├── socket
│       │   └── uber
│       ├── frontend
│       │   ├── customer
│       │   └── merchant
│       └── ingress-static-file
│           └── ingress.yml
└── prod
    └── mentum-eks-cluster-prod
```
