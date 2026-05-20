---
title: "Installation"
url: "/docs/latest/spire-helm-charts-hardened-about/installation/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Quick start To do a quick install suitable for non production environments such as minikube: helm upgrade --install --create-namespace -n spire spire-crds spire-crds \ --repo https://spiffe.github.io/helm-charts-hardened/ helm upgrade --install -n spire spire spire \ --repo https://spiffe.github.io/helm-charts-hardened/ Production Deployment Preparing a production deployment requires a few extra steps. Save the following to your-values.yaml, ideally in your git repo. global: openshift: false # If running on openshift, set to true spire: recommendations: enabled: true namespaces: create: true…
