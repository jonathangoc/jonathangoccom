---
title: "The (Un)compressed Traffic Billing Paradigm"
date: 2020-07-20T16:47:00+00:00
draft: false
layout: "single"
Donate: true
ShowWordCount: true
ShowReadingTime: true
disableShare: false
ShowPostNavLinks: false
ShowCodeCopyButtons: true
ShowBreadCrumbs: true
tags: ["tech", "akamai", "cdn", "a2", "brotli", "zopfli", "cloudflare gateway", "compressed content", "compression", "deflate", "delivery property", "fastly", "gzip", "last mile acceleration", "lma", "origin compression", "proxy property", "resource optimizer", "traffic billing issues"]
categories: ["Tech", "Web Performace"]
cover:
    image: "/img/c1.png"
    responsiveImages: true
    hidden: true
---

# TL;DR

This blog post explores concerns about the costs of delivering uncompressed and compressed content on Akamai and other Content Delivery Networks, whilst providing a solution to help organizations effectively manage these costs.

# Overview

Nowadays, digital businesses and organisations are looking for improving the performance of their Websites and Application aiming to provide a better experience for their end-users. One of the optimisation techniques available today is Content Compression (A.K.A. HTTP Compression).

Content Compression is a capability used by web servers to compress content before it is sent to the requesting browsers. The requesting browsers will announce what methods are supported to the web server before downloading the correct format and browsers that do not support compliant compression methods will download uncompressed data. The most common compression schemes include **Gzip**, **Deflate** and **Brotli**.

The compressed and uncompressed content is stored at the origin where it can be served directly to the client browsers or through a CDN. Most CDN solutions provide compression capabilities and Akamai offers that through the Last Mile Acceleration (for Gzip compression) or Resource Optimiser (for Brotli and Zopfli compression).

# The Problem

For Akamai, if the content was in an uncompressed form at any time between receiving it from the origin and delivering it to the client, it will be considered uncompressed content and Akamai will charge organizations not on the compressed object that was delivered to the end-user but on the uncompressed object that was fetched from origin. Additionally, the Traffic Reports in Akamai Control Center (ACC) will reflect the uncompressed traffic size which will therefore show more data delivered on Akamai than is actually happening.

I believe the idea behind that is because Akamai has to expend compute resources to parse and compress the content at the Edge. However, CDNs like Cloudflare and Fastly only charge for content that actually gets delivered to the end-users regardless of whether the content was uncompressed at the origin or not. As long as the content is delivered compressed, they will charge customers for compressed content.

That makes the Akamai billing model a challenge for many organizations.

# A Common Use-case

An example of this problem is when organizations move their traffic from a third-party CDN (e.g. Cloudflare) to Akamai and keep their uncompressed content in AWS S3 (the origin).

Unlike Cloudflare, Akamai charges for uncompressed content even if the content was delivered compressed to end users as the object received from the origin is uncompressed and therefore cached on Akamai uncompressed.

Because of that, organizations can experience an increase in traffic volume and costs.

# The Solution

In order to reduce the traffic volume and costs generated by the uncompressed content, another delivery property can be deployed between AWS S3 (the origin) and the current Akamai delivery property.

I will call the first one – Proxy Property (PP) – and the latter – Delivery Property (DP).

The idea is that PP will request the uncompressed content from AWS S3, compress it, and cache it at the edge while DP will have PP as the origin and will deliver compressed content to end-users.

# Results – Traffic Analysis

After experimenting with this solution, this is what I have found.

The first analysis was to understand if the number of hits was the same before and after the change. The graphic below shows the traffic for DP – property delivering traffic directly to end-users.

| ![](/img/ta1.png) |
| :--: |
| **Figure 1:** Traffic data in hits per second.  |

Figure 1 shows the traffic profile (how end-users interact with the service) hasn’t changed at all (same number of requests per day). But what I ended up discovering was that the traffic volume (number of bytes delivered to end-users) is a lot lower after the change was made as you can see in the graphic below.

| ![](/img/ta2.png) |
| :--: |
| **Figure 2:** Traffic data in bits per second.  |

# Conclusion

The reason why the traffic volume (bytes delivered) is lower is that PP tracks edge traffic it delivers as uncompressed (as it comes uncompressed from the AWS S3 even if the edge actually delivers the content compressed), whilst DP tracks the origin traffic as compressed (as PP – the origin in this case – delivers the content it got upstream from the actual AWS S3 origin uncompressed and compresses it for delivery).

Whilst this solution may reduce the traffic volume and costs, it does add additional complexity to the setup and introduces a second request flow when the content isn’t in cache and that can add a performance penalty to the service (and additional billing as Akamai delivers the content twice – once from DP and once from PP).

It is always recommended that organizations enable content compression at the origin to avoid excessive traffic and additional costs when using CDNs.

