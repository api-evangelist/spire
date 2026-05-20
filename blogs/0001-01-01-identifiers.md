---
title: "Identifiers"
url: "/docs/latest/spire-helm-charts-hardened-about/identifiers/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Defaults The chart deploys SPIRE Controller Manager to manage SPIFFE Identifiers by Kubernetes Custom Resources. The chart deploys a ClusterSPIFFEID Custom Resource that gives an identifier to all pods of the form spiffe://{{ .TrustDomain }}/ns/{{ .PodMeta.Namespace }}/sa/{{ .PodSpec.ServiceAccountName }}. For a lot of use cases you don’t need to add additional identifiers.
