---
title: "Build on Akamai | Linode"
date: 2022-08-08T10:04:00+00:00
draft: false
layout: "single"
ShowWordCount: true
ShowReadingTime: true
disableShare: false
ShowPostNavLinks: false
ShowCodeCopyButtons: true
ShowBreadCrumbs: true
cover:
    image: "/img/linode-logo-png-transparent.png"
    responsiveImages: true
    hidden: true
tags: ["tech", "akamai", "linode", "cdn", "build on akamai", "cloud compute", "compute", "databases", "dns", "godaddy", "networking", "storage", "wordpress"]
categories: ["Tech", "Buil on Akamai"]
---

For deploying a Website in the Cloud, I used Linode Cloud Computing Services. Linode provides an easy way to design, build, and deploy your own cloud strategy using the following products:

**COMPUTE** – Build, release, and scale faster with virtual machines and tools for every workload.

| ![](/img/l1.jpg) |
| :--: |
| **Figure 1:** Linode Compute Services.  |

**STORAGE** – Dependable, easily-accessible storage and management.

| ![](/img/l2.jpg) |
| :--: |
| **Figure 2:** Linode Storage Services.  |

**DATABASES** – Simple, Reliable, and Scalable Managed Databases.

| ![](/img/l3.jpg) |
| :--: |
| **Figure 3:** Linode DB Services.  |

**NETWORKING** – Secure your network, balance traffic, and control your infrastructure.

| ![](/img/l4.jpg) |
| :--: |
| **Figure 4:** Linode Networking Services.  |

The video below shows how easy it is to deploy a Linode instance with WordPress.

{{< youtube uA4UUlBK_QY >}}

**Video 1:** Deploying a Linode instance.

Once the instance is up and running, you could easily use the given public IP address and add a DNS record within your DNS solution to point the website to the Linode instance (origin).

{{< youtube l441uvf5Tn4 >}}

**Video 2:** Updating DNS records.

After the TTL has expired, the A record for www.jonathangoc.com will be pointing to the origin 176.58.127.193.

{{< youtube kf8J8B73d7s >}}

**Video 3:** Testing the Set-up.

The process above shows how easy it is to deploy a WordPress Website on Linode and you can do it in less than 10min.