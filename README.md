# Triplea-Operator

**Triplea-Operator** automates the deployment and lifecycle management of **InnoDB Cluster** for MySQL on Kubernetes, OpenShift, or OKE.

---

## Key Features

- **Public Docker Registry**: Available for easy pull and deployment.
- **Lightweight and Portable**: Runs seamlessly on Kubernetes, OpenShift, or OKE.
- **Sidecar Architecture**: Monitors the state of InnoDB Cluster in real-time.
- **Automatic Cluster Management**:
  - Configures InnoDB Cluster on containerized environments automatically.
  - Aligns cluster membership with StatefulSet replicas.
  - Adds or removes members dynamically.
- **Resilience and Recovery**:
  - Handles network partitions and pod failures gracefully.
  - Supports cluster reboot from complete outages.
- **Automated Backups**: Provides ad-hoc and scheduled MySQL database backups.

---

## Design Philosophy

- Triplea-Operator is **not a traditional Kubernetes Operator**.
- Designed with simplicity and minimal dependencies for **easy deployment** and **maintenance**.

---

## Installation

```bash
# Pull the Triplea-Operator Docker image
docker pull your-docker-repo/triplea-operator:latest
