---
title: "Namespaces"
url: "/docs/latest/spire-helm-charts-hardened-about/namespaces/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Namespace Creation Options Value Default Value Description global.spire.namespaces.create false Create both recommeded namespaces global.spire.namespaces.server.create false Create the namespace specified by global.spire.namespaces.server.name (default spire-server) global.spire.namespaces.system.create false Create the namespace specified by global.spire.namespaces.spire.name (default spire-server) Three Namespace Configuration This is the recommended configuration, it automatically creates and deploys SPIRE across 3 namespaces. your-values.yaml snippet: global: spire: recommendations:…
