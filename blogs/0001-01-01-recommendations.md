---
title: "Recommendations"
url: "/docs/latest/spire-helm-charts-hardened-about/recommendations/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
Enable Recommendations In a production deployment there are a series of recommendations we have. By enabling the recommendations, you can easily get all of them applied to your deployment. If there are particular recommmendations you do not wish to use, you can still set those recommendations to false to disable them. your-values.yaml snippet: global: spire: recommendations: enabled: true Individual Recommentations Name Value Namespace Layout global.
