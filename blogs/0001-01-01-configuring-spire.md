---
title: "Configuring SPIRE"
url: "/docs/latest/deploying/configuring/"
date: "Mon, 01 Jan 0001 00:00:00 +0000"
author: ""
feed_url: "https://spiffe.io/index.xml"
---
To customize the behavior of the SPIRE Server and SPIRE Agent to meet your application’s needs you edit configuration files for the server and agent.
How to configure SPIRE The SPIRE Server and Agent are configured in a file called server.conf and agent.conf respectively.
By default the Server expects the configuration file to reside at conf/server/server.conf, however the Server can be configured to use a configuration file in a different location with the --config flag.
