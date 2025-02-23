# ChonLe - Senior Site Reliability Engineer / DevOps Engineer

## 👨‍💻 About Me
Senior SRE/DevOps Engineer with 5 years of experience in building and operating large-scale cloud-native systems. Expertise in automation, infrastructure as code, and cloud architecture on AWS and GCP platforms.

## 🛠 Technical Skills

### Cloud Platforms & Infrastructure
- **AWS**: Extensive experience with EKS, EC2, RDS, S3, CloudFront, Route53
- **GCP**: Expertise in GKE, Compute Engine, Cloud Storage, Cloud SQL
- **Kubernetes**: Deployment and management of EKS/GKE clusters, helm charts, custom controllers
- **Infrastructure as Code**: Terraform, CloudFormation
- **Container Technologies**: Docker, Containerd, Kubernetes

### Monitoring & Observability
- **Monitoring Stack**: Prometheus, Grafana, AlertManager, Datadog
- **Logging**: ELK Stack, Datadog, OpenTelemetry
- **Tracing**: Datadog, OpenTelemetry
- **Metrics**: Custom metrics collection, SLO/SLI implementation

### Development & Automation
- **Programming Languages**: 
  - Golang: Development of internal tools and operators
  - Python: Automation scripts and tooling
  - Bash: Shell scripting for automation
- **CI/CD**: 
  - GitLab CI
  - GitHub Actions
  - ArgoCD

### Security & Compliance
- **Security Tools**: Vault, CertManager, OPA
- **Network Security**: VPC design, Security Groups, NACLs
- **Compliance**: ISO 27001, SOC2 implementation experience

## 🚀 Key Projects & Achievements

### Platform Engineering
#### Kubernetes Platform Automation (2022-2023)
- Built an automated platform for EKS cluster provisioning
- Developed Golang operators for automated resource management:
  - Created custom OpenSearch autoscaling operator
  - Implemented intelligent scaling based on resource metrics and search patterns
  - Built monitoring and alerting for scaling events:
    - Prometheus metrics for cluster scaling operations
    - Grafana dashboards for visualizing scaling patterns
    - Real-time alerts for scaling failures or threshold breaches
- Implemented GitOps workflow with ArgoCD
- **Impact**: Reduced infrastructure provisioning time by 70%, increased developer productivity by 50%

### Infrastructure Optimization
#### Cloud Cost Optimization Initiative (2020-2021)
- Developed tools for cloud cost tracking and optimization:
  - Built DNS proxy service to reduce cross-AZ traffic costs
  - Implemented intelligent DNS caching and request routing
  - Created tools to optimize data transfer between regions
  - Developed service mesh configurations for local traffic prioritization
- **Impact**: Achieved 30% monthly cloud cost savings, reduced cross-AZ traffic by 65%

### Reduced 70% of cost of the Datadog
- The developed service collects metrics from Prometheus and pushes them to Datadog, helping us reduce the cost of Datadog custom metrics by 70%.

### Observability & Monitoring
#### Observability Platform Enhancement (2021-2022)
- Designed and implemented monitoring stack using Prometheus, Datadog
- Implemented distributed tracing with OpenTelemetry
- Built custom dashboards and alerting rules
- **Impact**: Reduced MTTR from 40 minutes to 15 minutes

### Operational Excellence
#### Production System Reliability
- Maintained 99.99% uptime for production systems
- Led 24/7 on-call rotation and incident response:
  - Average resolution time of 15 minutes
  - Established incident management playbooks and runbooks
  - Implemented automated incident response procedures:
    - Built automated issue tracking tool with instant system state capture
    - Developed service for auto-generating screenshots of relevant dashboards
    - Integrated with alerting system for immediate visual context
  - Reduced MTTR by 60% through process improvements

#### Automation Initiatives
- Automated 80% of routine operations tasks:
  - Built self-service platform for database operations:
    - Automated backup/restore for OpenSearch, Redis, DynamoDB, PostgreSQL
    - Implemented point-in-time recovery with snapshot management
    - Created cross-region backup replication
    - Built one-click backup/restore web interface
    - Automated backup verification and monitoring
  - Developed automated certificate rotation system
  - Created user access management and audit system
  - Implemented routine maintenance automation

### Leadership
- Successfully mentored 5 junior engineers
- Reduced deployment time from 45 minutes to 10 minutes
- Established best practices and documentation standards

## 📫 Contact
- Email: vanchonlee@gmail.com
- LinkedIn: www.linkedin.com/in/chonle-devops-sre
- GitHub: github.com/vanchonlee
