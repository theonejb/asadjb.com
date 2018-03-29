---
title: "Dropletconn"
date: 2015-08-11
draft: false
project_url: "https://github.com/theonejb/dropletconn"
---

Dropletconn is a small Go based CLI tool to easily connect to Digital Ocean droplets. It's like Google Cloud CLIs `gcloud compute ssh SERVER` for Digital Oceans.

<!--more-->

Back in 2014 when I started working at JRD Group (justproperty.com) I also got the chance to work as the DevOps guy. We were using Digital Ocean VPS (droplets) and a problem I was facing was that in-order to connect to a droplet, I had to go to the Digital Ocean dashboard to find the IP first, then connect to it via SSH from my command line.

I wanted a more streamlined experience. Not finding anything, I built it myself.

With Dropletconn, you can type `dropletconn list` and it will get the list of droplets in your Digital Ocean account and list them. Kind of like:

```
+---------+-------------+-----------------+---------------+
|   ID    |    NAME     |    PUBLIC IP    |  PRIVATE IP   |
+---------+-------------+-----------------+---------------+
| 1234567 | SERVER_NAME | 000.000.000.000 | 00.000.000.00 |
+---------+-------------+-----------------+---------------+
```

The most useful command for Dropletconn is the `connect` one. You can do `dropletconn connect SERVER_NAME` and it will open a new SSH session to the server.

Even though I don't work with Digital Ocean droplets at my day job anymore, I still have a few running for some personal projects, and Dropletconn is an indispensable utility.