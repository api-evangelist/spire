---
title: "Registering workloads"
url: "/docs/latest/deploying/registering/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
How to create a registration entry A registration entry contains the following: a SPIFFE ID a set of one or more selectors a parent ID The server will send to the agent a list of all registration entries for workloads that are entitled to run on that node. Agents cache these registration entries and keep them updated. During workload attestation, the agent discovers selectors and compares them to those in the cached registration entries to determine which SVIDs they should assign to the workload.
