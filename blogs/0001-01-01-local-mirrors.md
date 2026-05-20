---
title: "Local Mirrors"
url: "/docs/latest/spire-helm-charts-hardened-advanced/mirror/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Identify Containers needing mirroring Run: helm template spire --repo https://spiffe.github.io/helm-charts-hardened/ -f your-values.yaml | yq e -rN \ '[.spec, .spec.template.spec] | flatten(1) | .[]| [.containers, .initContainers] | flatten(1) | .[].image' - \ | sort -u Example output: cgr.dev/chainguard/bash:latest cgr.dev/chainguard/kubectl:latest cgr.dev/chainguard/wait-for-it:latest-20230113 ghcr.io/spiffe/spiffe-csi-driver:0.2.3 ghcr.io/spiffe/spire-agent:1.6.3 ghcr.io/spiffe/spire-controller-manager:0.2.2 ghcr.io/spiffe/spire-server:1.6.3…
