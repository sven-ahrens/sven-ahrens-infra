# sven-ahrens-infra

This repo contains all the Kubernetes manifests needed to deploy my Laravel-based portfolio project to a **manually managed K8s cluster** on Google Cloud VMs — no GKE, no Helm charts, no handholding. Just raw YAML, managed with Kustomize.

---

## 🧠 What’s this?

This repo powers [`sven-ahrens`](https://github.com/sven-ahrens), a Laravel-based portfolio site that:
- Introduces me (👋)
- Showcases my skills and projects (💼)
- Embeds a live **cluster monitoring dashboard** (📊), built into the Laravel app

The infrastructure here deploys that app using raw Kubernetes + Kustomize. It's intended to be a real-world example of building, running, and managing a cloud-native app without relying on GKE or managed services.

---

## 🔧 What's in this repo

- `Deployment`, `Service`, `Ingress`, `Secrets`, and `ConfigMaps`
- Kustomize setup with overlays (e.g., `dev`, `prod`)
- Ingress NGINX config (deployed manually)
- Service Account + RBAC for Laravel app to access the Kubernetes API
