---
title: "Using Envoy with SPIRE"
url: "/docs/latest/microservices/envoy/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Envoy is a popular open-source service proxy that is widely used to provide abstracted, secure, authenticated and encrypted communication between services. Envoy enjoys a rich configuration system that allows for flexible third-party interaction.
One component of this configuration system is the Secret Discovery Service protocol or SDS. Envoy uses SDS to retrieve and maintain updated “secrets” from SDS providers. In the context of TLS authentication, these secrets are the TLS certificates, private keys, and trusted CA certificates.
