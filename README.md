![Banner](readme.md.png)
### Pursuing DevOps engineering
# Contact
- Email: l4nc1nant@gmail.com
- Discord: @lancinant
- Telegram: https://t.me/lancinant
# Skills & Experience
- **OS:** Linux (Ubuntu, Debian), Windows 
- **IaC:** Terraform (Hyper-V provider), Ansible, Ansible Vault
- **Containers:** Docker, Docker Compose
- **Orchestration:** Kubernetes (kubeadm)
- **CI/CD:** GitLab CI
- **Monitoring:** Prometheus, Grafana, Loki, Alertmanager, Alloy, cAdvisor, node_exporter, windows_exporter
- **Networking:** Nginx Reverse Proxy, Cloudflare Tunnel, Tailscale, UFW, HAProxy
- **Cloud:** Oracle Cloud (OCI), GCP, Azure, DigitalOcean, Yandex Cloud
- **Version control:** GitLab (self-hosted)
# Projects
### Portfolio Site (in progress)
Self-hosted DevOps portfolio deployed on a Kubernetes cluster spanning a local control plane (ctl01) and a cloud worker node on OCI (wrk02), connected over Tailscale. Built with a GitLab CI pipeline that builds a Docker image, pushes it to a self-hosted registry, and applies Kubernetes manifests on every push to main. Publicly exposed via Cloudflare Tunnel without opening any cloud firewall ports.
### Self-hosted music streaming service
Self-hosted music streaming service running Navidrome and yubal on nav01, with full high availability. HAProxy on a dedicated OCI instance (proxy01) routes traffic to nav01 as the primary backend and automatically fails over to a hot standby (nav02) when health checks fail. Music libraries kept in sync between nav01 and nav02 via Syncthing. Cloudflare Tunnel runs on proxy01 as the permanent entry point, decoupling public traffic from the home server. Stack monitored via Prometheus and Grafana including HAProxy metrics via the native Prometheus exporter.
### TeamSpeak Server
Self-hosted TeamSpeak server running via LinuxGSM on ts01. Publicly accessible on a free domain registered through DigitalPlat, with Cloudflare DDNS keeping the DNS record updated as the home IP changes.
### Homelab IaC
Full infrastructure-as-code provisioning of a three-host homelab (VMware, Hyper-V) using Terraform and Ansible. Secrets managed with Ansible Vault. Observability stack covers all hosts including Windows nodes via windows_exporter.
# Homelab Hardware
| Host | CPU | RAM | Role |
|---|---|---|---|
| hv01 | i5-3470 | 16GB DDR3 | Jellyfin, Sonarr, Radarr, Jackett |
| hv02 | i5-9500 | 16GB DDR4 | Hyper-V host — ts01, mon01, nav01 |
| hv03 | i7-10750H | 32GB DDR4 | VMware host — jump01, ctl01, wrk01, git01 |
| wrk02 | OCI A1.Flex | 12GB | Cloud k8s worker, portfolio site |
| nav02 | OCI E2.1.Micro | 1GB | Navidrome standby |
| proxy01 | OCI E2.1.Micro | 1GB | HAProxy, Cloudflare Tunnel entry point |
### Homelab Services
- Jellyfin with Sonarr, Radarr, Jackett
- TeamSpeak server via LinuxGSM
- Full monitoring stack (Prometheus, Grafana, Loki, Alertmanager, Alloy) deployed in the cloud for HA
- Navidrome music streaming with HAProxy failover
# In Progress
- Kubernetes cluster (ctl01 + wrk02 + wrk01)
- GitLab CI/CD pipeline for portfolio deployment

