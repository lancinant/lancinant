![Banner](readme.md.png)
### Pursuing DevOps engineering
# Contact
- Email: l4nc1nant@gmail.com
- Discord: @lancinant
- Telegram: https://t.me/lancinant
# Skills & Experience
- **OS:** Ubuntu, Debian, Windows 
- **IaC:** Terraform (Hyper-V provider), Ansible, secret management via Ansible Vault
- **Containers:** Docker, Docker Compose
- **Orchestration:** Kubernetes (k3s)
- **CI/CD:** GitLab CI
- **Monitoring:** Prometheus, Grafana, Uptime Kuma (cAdvisor, Alertmanager, 
- **Networking:** Nginx Reverse Proxy, Cloudflare Tunnel, Tailscale, UFW, HAProxy
- **Cloud:** simple deployments on Oracle Cloud (OCI), GCP, Azure, DigitalOcean, Yandex Cloud 
- **Version control:** Github
- **Container registry:** Harbor
# Projects
### Portfolio Site (in progress)
Self-hosted DevOps portfolio deployed on a k3s cluster with a local control plane (ctl01) and a cloud worker node on OCI (wrk02); connected over Tailscale. Built with a GitLab CI pipeline that builds a Docker image, pushes it to a self-hosted Harbor, and applies Kubernetes manifests on every push to main. Publicly exposed via Cloudflare Tunnel without opening any cloud firewall ports. Harbor's https termination is achieved through `tailscale serve`.
### Self-hosted music streaming service
Self-hosted music streaming service running Navidrome and yubal (music downloader) on nav01, with full high availability. HAProxy on a dedicated OCI instance (proxy01) routes traffic to nav01 as the primary backend and automatically fails over to a standby (nav02) when health checks fail. Music libraries kept in sync between nav01 and nav02 via Syncthing. Cloudflare Tunnel runs on proxy01 as the permanent entry point, decoupling public traffic from the home server. Stack monitored via Prometheus and Grafana including HAProxy metrics via the native Prometheus exporter.
### TeamSpeak Server
Self-hosted TeamSpeak server running via LinuxGSM on ts01. Publicly accessible on a free domain registered through DigitalPlat, with Cloudflare DDNS keeping the DNS record updated as the home IP changes. Uptime monitored via Uptime Kuma.

### Homelab Services
- Jellyfin with Sonarr, Radarr, Jackett
- TeamSpeak server via LinuxGSM
- Full monitoring stack (Prometheus, Grafana, Loki, Alertmanager, Alloy) deployed in the cloud for HA
- Navidrome music streaming with HAProxy failover
# In Progress
- Kubernetes cluster (ctl01 + wrk02 + wrk01)
- GitLab CI/CD pipeline for portfolio deployment
- Github Actions for CI/CD
- K8s at operational level (replicas, controllers, etc.)



