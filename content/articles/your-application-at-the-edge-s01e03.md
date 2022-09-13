---
title: "Your Application At The Edge [S01E03]"
date: 2019-05-07T12:58:00+00:00
draft: false
layout: "single"
Donate: true
ShowWordCount: true
ShowReadingTime: true
disableShare: false
ShowPostNavLinks: false
ShowCodeCopyButtons: true
ShowBreadCrumbs: true
tags: ["tech", "[s01e03]", "akamai", "cdn","change host file", "gas mask", "ion", "onboarding", "testing in staging", "web performance", "your application at the edge"]
categories: ["Tech", "Your Application At The Edge"]
cover:
    image: "/img/ate2.png"
    responsiveImages: true
    hidden: true
---

# Intro

This blog post will cover the details on how to deliver your Website or Application using the Akamai Edge Platform as the CDN infrastructure.

# What’s Hot?

Have you checked the previous [Your Application at the Edge [S01E02]]({{< ref "articles/your-application-at-the-edge-s01e02" >}}) blog post? It explains how you can use NS as an origin.

# Context

As described in the previous post, Figure 1 shows the end-to-end architecture in which we have the origins (on the left-hand side), the Akamai Edge Platform (in the middle), and the end-users (on the right-hand side).

| ![](/img/arch1.jpg) |
| :--: |
| **Figure 1:**  High-level Architecture Overview. |

In the current scenario NetStorage (NS) is our origin (see Figure 2) and its deployment was covered in the previous blog post. In this one, we will focus our attention on the delivery piece which is provided by Ion – one of Akamai’s Web Performance Delivery Products.

| ![](/img/arch3.png) |
| :--: |
| **Figure 2:**  Ion – Web Performance Delivery Product Positioning. |

Ion is a suite of integrated performance optimisations, tools, and intelligence that together address each stage of delivering compelling online experiences, from development and deployment, through middle-mile and cellular networks, to user devices, browsers, and apps.

Let’s explore how we can configure an Ion Property for delivering our content through the CDN platform.

# Requirements

The first requirement is to have the content of the Website or Application in NS or in your origin. If you are using your own origin make sure you have the hostname and that your origin supports IPv4, HTTP and/or HTTPS Traffic, and it’s reachable through a DNS lookup request.

# Creating an Ion Property

1. Login into Akamai Control Centre using your credentials
2. Click on “Create” and select “Property”.
3. Select the Product (for this guide we will choose Ion Standard) and give the Property a name. In my case, I will call it jc-website.
4. So now the first thing to do is to add a Hostname to the property. You can do this by going to the Property Hostnames Section and clicking on “Add”. I will add www.jcnotebook.com and www.jcnotebook.com.edgesuite.net. The latter will give me access to the Website and its content as I don’t have registered www.jcnotebook.com. This is a trick you can do to build Test Properties and test them without having to register the domain name with a Domain Registrars such as GoDaddy.

| ![](/img/pm1.png) |
| :--: |
| **Figure 3:**  Adding hostnames to the Delivery Property. |

5. Scroll down to the Rule and Behaviours. In the Origin Server, you have to choose your NS Group as your origin. Then you have to create a new CP Code for reporting the traffic for that particular delivery property. In my case, I am not allowing POST HTTP method because my Website is a single page to show some content and there is no need for the end-user to send content to my Website. Additional I am turning on RUM to have more visibility into the user traffic.

| ![](/img/pm2.png) |
| :--: |
| **Figure 4:**  Configuring the Default Rule. |

6. Moving to the next section: Performance – I am disabling SureRoute because my WebSite only has static content. Leave the other behaviour as they are.
7. In the Offload Rule, I am changing my caching options from “No Store” to “Cache” and setting the TTL to 1 hour. I could have chosen 7 days or more for the TTL since we are delivering static content but in future, I will cover how to improve performance by showing you how the increase the TTL and how it plays out when optimising content delivery.

| ![](/img/pm3.png) |
| :--: |
| **Figure 5:**  Setting the caching TTL to 1 hour. |

8. Apply the same logic to CSS, JS files, and other static objects.
9. If no errors show up please save your configuration and push it to the Akamai Staging Network.

| ![](/img/pm4.png) |
| :--: |
| **Figure 6:**  Activating the Delivery Property to Staging Network. |

# How To Test Your Property In Staging

1. Find the edge hostname for your domain (it should end with “edgesuite.net”) – in my case is www.jcnotebook.com.edgesuite.net.
2. Find the IP address of the staging edge hostname related to the edge hostname you found (replace “edgesuite.net” with “edgesuite-staging.net”) – in my case: www.jcnotebook.com.edgesuite- staging.net.

 ```bash
 ~ dig www.jcnotebook.com.edgesuite-staging.net
; <<>> DiG 9.10.6 <<>> www.jcnotebook.com.edgesuite-staging.net
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 57357
;; flags: qr rd ra; QUERY: 1, ANSWER: 3, AUTHORITY: 0, ADDITIONAL: 1 ;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096 ;; QUESTION SECTION:
;www.jcnotebook.com.edgesuite-staging.net. IN A ;; ANSWER SECTION:
www.jcnotebook.com.edgesuite-staging.net. 21578 IN CNAME a1831.dscr.akamai- staging.net.
a1831.dscr.akamai-staging.net. 20 IN A 23.50.55.19 a1831.dscr.akamai-staging.net. 20 IN A 23.50.55.27
;; Query time: 129 msec
;; SERVER: 172.27.216.42#53(172.27.216.42) ;; WHEN: Mon Dec 17 16:31:32 GMT 2018
;; MSG SIZE rcvd: 141
```

My Staging IP Addresses are 23.50.55.19 and 23.50.55.27.

3. Add the IP address to your host file to make all requests from your PC going to staging edge host (/etc/ hosts on UNIX/Mac c:\windows\system32\drivers\hosts on Windows). It will not work if you are behind a corporate web proxy.

```bash
23.50.55.19 www.jcnotebook.com
```

**Note:** For OS X users there is a great tool called Gas Mask which allows you to edit the host file very easily.

4. Make sure that your web browser closed all already opened connections to the production edge host. For example by restarting it or starting a new instance.
5. To be sure your web browser now connects to staging edge hostname, open dev-tools then enter your Website address (http://www.jcnotebook.com/index.html) into the address bar. Once it loads, check the Server IP. It should be the same as the one you just entered into the host file. It is a good practice to recheck this during testing just to be sure that you test what is supposed to be tested.

# Summary

On-boarding the Website into the Akamai Edge Platform using the Ion Web Performance product was pretty straightforward. The fact that I am using static content makes things easier because Akamai’s Control Centre provided me with a default template in which I can quickly modify the caching settings, use compression methods and choose the origin.

I didn’t have to make changes to the DNS records but for those who have a public doming, they need to CNAME their domain to the Akamai edge hostname.

They can use Akamai’s Edge DNS as their DNS Infrastructure.

For more advanced behaviours, like SureRoute for Performance, Advanced Caching, Adaptive Acceleration, Image Compression, and others you would have to add them by yourself to the property as per your requirements and make sure you test them carefully.

# What’s next?

In the blog post, I will explore the Monitor Tools available within Akamai Control Centre, how to analyse traffic and how to use WebPageTest – an open-source tool – for testing website performance.

