---
title: "Federation"
url: "/docs/latest/spire-helm-charts-hardened-advanced/federation/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
The typical architecture for Federated SPIRE using the Helm charts uses a 1:1 relationship between SPIRE instances and Kubernetes Clusters, as well as multiple Kubernetes clusters. Federation Configuration There are 4 pieces of configuration related to Federation. Enabling Federation Set spire-server.federation.enabled=true. your-values.yaml snippet: spire-server: federation: enabled: true Exposing Federation Bundle Endpoint outside the Kubernetes Cluster Set spire-server.federation.ingress.enabled=true.
