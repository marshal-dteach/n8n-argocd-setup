## This is a kubernetes based setup for n8n with argocd


We are using kustomize to manage different types of environments - dev, prod and staging

Deployment will be done as per GitOps principles -
1. Declarative - Git will be the only source of truth - We are managing the configuration from git only, no one can change the configuration locally.
2. Versioned - Each change will be versioned and can be easily rollbacked to older state.
3. Reconciled - ArgoCD will keep the changes in sync between git and kubernetes.
4. Observability - Will be achieved through ArgoCD dashboard.
5. PR based Ops - all the changes to the environment will be done through git.