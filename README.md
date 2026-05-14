
# **Pursuing DevOps Engineering**

![Banner](banner.png)

Email: l4nc1nant@gmail.com | Discord: @lancinant | Telegram: https://t.me/lancinant

---

## Skills & Experience

| Area | Technologies |
|---|---|
| OS | Ubuntu, Debian, Windows |
| IaC | Terraform (Hyper-V provider), Ansible, Ansible Vault |
| Containers | Docker, Docker Compose |
| Orchestration | Kubernetes (k3s) |
| CI/CD | GitLab CI |
| Monitoring | Prometheus, Grafana, Uptime Kuma, cAdvisor, Alertmanager |
| Networking | Nginx Reverse Proxy, Cloudflare Tunnel, Tailscale, UFW, HAProxy |
| Cloud | OCI, GCP, Azure, DigitalOcean, Yandex Cloud |
| Version Control | GitHub |
| Registry | Harbor |

---

## Projects

### Portfolio Site *(in progress)*
Self-hosted portfolio deployed on a k3s cluster with a local control plane and a cloud worker node on OCI, connected over Tailscale. GitLab CI pipeline builds a Docker image, pushes to a self-hosted Harbor registry, and applies Kubernetes manifests on every push to main. Publicly exposed via Cloudflare Tunnel without opening cloud firewall ports. Harbor HTTPS termination via Tailscale Serve.

`k3s` `GitLab CI` `Harbor` `Tailscale` `Cloudflare Tunnel` `OCI`

### Music Streaming — HA Stack
Self-hosted Navidrome service with full high availability. HAProxy on a dedicated OCI instance (proxy01) routes traffic to nav01 as primary and fails over to nav02 on health check failure. Music libraries kept in sync via Syncthing. Cloudflare Tunnel on proxy01 is the permanent public entry point, decoupling traffic from the home server. Stack monitored via Prometheus and Grafana including HAProxy native Prometheus exporter.

`Navidrome` `HAProxy` `Syncthing` `Cloudflare Tunnel` `Prometheus` `Grafana` `OCI`

### TeamSpeak Server
Self-hosted TeamSpeak running via LinuxGSM. Publicly accessible on a free domain registered through DigitalPlat, with Cloudflare DDNS keeping the DNS record updated as the home IP changes. Uptime monitored via Uptime Kuma.

`TeamSpeak` `LinuxGSM` `Cloudflare DDNS` `Uptime Kuma`

---

## Homelab Services

- Jellyfin with Sonarr, Radarr, Jackett
- TeamSpeak server via LinuxGSM
- Full monitoring stack (Prometheus, Grafana, Loki, Alertmanager, Alloy) deployed in the cloud for HA
- Navidrome music streaming with HAProxy failover

---

## In Progress

- Kubernetes cluster with two workers
- GitLab CI/CD pipeline for portfolio deployment
- GitHub Actions for CI/CD
- K8s at operational level (replicas, controllers, etc.)
- Docker In-Depth

---

## Future Plans

- Scripting in Go / Python
- Advanced IaC
- RHEL administration (AlmaLinux, Rocky)
```
