---
title: "AWS OIDC Authentication"
url: "/docs/latest/keyless/oidc-federation-aws/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
This tutorial builds on the Kubernetes Quickstart guide to describe how a SPIRE identified workload can, using a JWT-SVID, authenticate to Amazon AWS APIs, assume an AWS IAM role, and retrieve data from an AWS S3 bucket. This avoids the need to create and deploy AWS IAM credentials with the workload itself.
In this tutorial you will learn how to:
 Deploy the OIDC Discovery Provider Service Create the required DNS A record to point to the OIDC Discovery document endpoint Create a sample AWS identity provider, policy, role, and S3 bucket Test access to the S3 bucket  Prerequisites Note the following required accounts, prerequisites, and limitations before starting this tutorial:
