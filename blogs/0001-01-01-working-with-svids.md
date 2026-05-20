---
title: "Working with SVIDs"
url: "/docs/latest/deploying/svids/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
A SPIFFE-compatible identity provider such as SPIRE will expose SPIFFE Verifiable Identity Documents (SVIDs) via the SPIFFE Workload API. Workloads can use SVIDs retrieved from this API to verify the provenance of a message or to establish mutual TLS secured channels between two workloads. Interacting with the Workload API Developers coding a new workload that needs to interact with SPIFFE can interact directly with the SPIFFE Workload API to: Retrieve the workload’s identity, described as a SPIFFE ID such as spiffe://prod.
