---
title: "Using SPIRE and OIDC to Authenticate Workloads to Retrieve Vault Secrets"
url: "/docs/latest/keyless/vault/readme/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
This tutorial builds on the Kubernetes Quickstart guide to describe how to set up OIDC Federation between a SPIRE Server and a Vault server. This will allow a SPIRE-identified workload to authenticate against a federated Vault server by presenting no more than its JWT-SVID. Using this technique the workload won’t need to authenticate itself against the Vault server using another authentication method like AppRole or Username & Password.
