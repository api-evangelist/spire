---
title: "Service Selection"
url: "/docs/latest/spire-helm-charts-hardened-about/service-selection/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Services provided by the chart There are multiple services provided by the chart. They can be enabled/disabled as needed using helm values. Production Services Service Name Value Enabled by Default SPIRE Server spire-server.enabled true SPIRE Agent spire-agent.enabled true SPIRE Controller Manager spire-server.spireControllerManager.enabled true SPIFFE OIDC Discovery Provider spiffe-oidc-discovery-provider.enabled true SPIFFE CSI Driver spiffe-csi-driver.enabled true Experimental Services Service Name Value Enabled by Default Tornjak Frontend tornjak-frontend.
