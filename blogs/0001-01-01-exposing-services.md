---
title: "Exposing Services"
url: "/docs/latest/spire-helm-charts-hardened-about/exposing/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Default By default no SPIRE services are exposed outside the Kubernetes cluster. The below sections cover how to expose them. Exposable Services Production Services Service Name Section Value Default DNS Name SPIRE Server spire-server.ingress spire-server.$trustDomain SPIRE Federation Bundle Endpoint spire-server.federation.ingress spire-server-federation.$trustDomain SPIFFE OIDC Discovery Provider spiffe-oidc-discovery-provider.ingress oidc-discovery.$trustDomain Experimental Services Service Name Value Default DNS Name Tornjak Frontend tornjak-frontend.
