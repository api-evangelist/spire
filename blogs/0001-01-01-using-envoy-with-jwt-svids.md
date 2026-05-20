---
title: "Using Envoy with JWT-SVIDs"
url: "/docs/latest/microservices/envoy-jwt/readme/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
This tutorial builds on the SPIRE Envoy-X.509 Tutorial to demonstrate how to use SPIRE to perform JWT SVID authentication on a workload’s behalf instead of X.509 SVID authentication. The changes required to implement JWT SVID authentication are shown here as a delta to that tutorial, so you should run, or at least read through, the X.509 tutorial first. To illustrate JWT authentication, we add sidecars to each of the services used in the Envoy X.
