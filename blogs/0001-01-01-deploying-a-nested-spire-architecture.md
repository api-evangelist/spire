---
title: "Deploying a Nested SPIRE Architecture"
url: "/docs/latest/architecture/nested/readme/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Nested SPIRE allows SPIRE Servers to be “chained” together, and for all SPIRE Servers to issue identities in the same trust domain, meaning all workloads identified in the same trust domain are issued identity documents that can be verified against the root keys of the trust domain. Nested topologies work by co-locating a SPIRE Agent with every downstream SPIRE Server being “chained”. The downstream SPIRE Server obtains credentials over the Workload API that it uses to directly authenticate with the upstream SPIRE Server to obtain an intermediate CA.
