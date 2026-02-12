# DevOps Platform Ansible Playbooks

🚀 Production-ready Ansible playbooks for complete DevOps platform management.

## 🎯 Platform Components

- **Kubernetes Cluster**: 1 Master + 3 Workers (K3s)
- **CI/CD**: Ansible Semaphore
- **Container Registry**: Docker Registry + Harbor
- **Security**: Trivy Scanner, Vault
- **Code Quality**: SonarQube
- **Artifact Management**: Nexus Repository
- **Monitoring**: Prometheus + Grafana
- **Storage**: Longhorn, MinIO
- **IaC**: Terraform

## 📦 Available Playbooks

### 1. health-check.yml
Complete cluster health monitoring
- System uptime
- Disk usage
- Memory usage
- CPU load

### 2. service-integration-test.yml
Test all service integrations
- Prometheus health
- Grafana connectivity
- Docker Registry
- SonarQube API
- MinIO S3

### 3. deploy-app-pipeline.yml
Full CI/CD pipeline
- Build Docker image
- Trivy security scan
- Push to registry
- Deploy to Kubernetes
- Prometheus metrics

### 4. backup-all-to-minio.yml
Automated backup strategy
- Backup all K8s resources
- Upload to MinIO S3
- Versioned backups
- Scheduled execution

## 🔧 Usage with Semaphore

1. Add this repository to Semaphore
2. Configure inventory with your cluster IPs
3. Set up SSH keys
4. Create task templates
5. Run playbooks manually or schedule

## 🌐 Service Access

| Service | URL | Credentials |
|---------|-----|-------------|
| Semaphore | http://10.40.92.46:30860 | admin/admin123 |
| Grafana | http://10.40.92.46:30300 | admin/admin |
| Prometheus | http://10.40.92.46:30090 | - |
| SonarQube | http://10.40.92.46:30902 | admin/admin |
| Nexus | http://10.40.92.46:30810 | admin/[check pod] |
| MinIO | http://10.40.92.46:30901 | minioadmin/minioadmin |
| Vault | http://10.40.92.46:30820 | token: root |

## 📝 Author

**Bahaddin Kayak**
- GitHub: [@bahaddinkyk](https://github.com/bahaddinkyk)
- Email: bahaddinkayak@gmail.com
- Company: TrimlyX Medya Ajans

## 📄 License

MIT License - Feel free to use for your projects!
