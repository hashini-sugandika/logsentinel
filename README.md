# LogSentinel

> A centralized log intelligence platform built on the ELK stack — collects, parses, and visualizes logs from Kubernetes pods and Nginx in real time.

![CI](https://github.com/hashini-sugandika/logsentinel/actions/workflows/ci.yml/badge.svg)

## What is LogSentinel?

LogSentinel collects logs from Kubernetes pods and Nginx access logs, enriches them through a Logstash pipeline, stores them in Elasticsearch, and visualizes them in Kibana with custom dashboards and alerts.

## Architecture
```
Kubernetes Pods + Nginx
        │
        ▼
   Fluentd DaemonSet          ← Runs on every K8s node
        │
        ▼
     Logstash                 ← Parse, filter, enrich
        │
        ▼
  Elasticsearch               ← Store + search
        │
        ▼
      Kibana                  ← Visualize + alert
```

## Tech Stack
- Elasticsearch 8.x
- Logstash 8.x
- Kibana 8.x
- Fluentd (K8s log shipping)
- Nginx (log source)
- Kubernetes + Helm
- GitHub Actions (CI/CD)
- Terraform (GCP infra)

## Getting Started
See [docs/setup.md](docs/setup.md) for setup instructions.
