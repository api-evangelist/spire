---
title: "Quickstart for Kubernetes"
url: "/docs/latest/try/getting-started-k8s/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Overview This guide walks you through getting a SPIRE Server and SPIRE Agent running in a Kubernetes cluster, and configuring a workload container to access SPIRE.
In this introduction to SPIRE on Kubernetes you will learn how to:
 Create the appropriate Kubernetes namespaces and service accounts to deploy SPIRE Deploy the SPIRE Server as a Kubernetes statefulset Deploy the SPIRE Agent as a Kubernetes daemonset Configure a registration entry for a workload Fetch an x509-SVID over the SPIFFE Workload API Learn where to find resources for more complex installations  The steps in this guide have been tested using Kubernetes versions 1.
