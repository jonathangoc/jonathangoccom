---
title: "I Built This Website Using Hugo"
date: 2022-10-09T17:34:00+00:00
draft: false
layout: "single"
Donate: true
ShowWordCount: true
ShowReadingTime: true
disableShare: false
ShowPostNavLinks: false
ShowCodeCopyButtons: true
ShowBreadCrumbs: true
cover:
    image: "/img/hugo_logo.jpg"
    responsiveImages: true
    hidden: true
tags: ["tech", "hugo", "open source", "website", "themes", "templates", "static page"]
categories: ["Tech", "Building Websites", "Open-source"]
---

# TL;DR
This short article explains why I chose Hugo as the framework to build my personal website, what Hugo is, who Hugo is for, and the details of my website.

# Why I Chose Hugo
There are mainly four reasons why I used Hugo to build my personal website.

- **Open-source:** Hugo is an open-source technology that allows anyone to create a static website. Therefore, the code is maintained by a community of developers and other contributors which consequently makes it performant and more secure.

- **Free:** Being open-source, Hugo is inherently and completely free of use.

- **User friendly:** Hugo is easy to install and easy to use.

- **Themes:** Hugo provides templates created by the community which allows users to easily customise their websites.

# What’s Hugo
In simple terms, Hugo is a website generator written in [Go](https://go.dev/). Unlike other systems that dynamically create a web page with each visitor request, Hugo builds these pages when content is created or updated. 

Websites created by Hugo run without the need of a database or dependencies on expensive runtimes. In other words, Hugo can be used to build static websites.

According to Hugo’s documentation, websites built by this framework are extremely fast and secure and it can be hosted anywhere, including [Netlify](https://www.netlify.com), [Linode](https://www.linode.com/pt/), [Akamai](https://www.akamai.com), [GoDaddy](https://www.godaddy.com), [GitHub Pages](https://pages.github.com/), [Google Cloud Storage](https://cloud.google.com/), [Amazon S3](https://aws.amazon.com/s3/), [Azure](https://azure.microsoft.com/) and others. 

Because the content is considered static, using a CDN like Akamai (or other CDN provider) will increase the performance and security of the website.

In my opinion, Hugo is a great tool for website automation. What I mean by this is users can easily modify the content whilst keeping the same website layout by leveraging templates, metadata, page parameters, and markdown files. This makes it very attractive for bloggers and website authors with less experience. 

# Who’s Hugo for?
Hugo is an open source project under the Apache 2.0 license and for that reason the community has been contributing to the project and this has seen tremendous progress over the last few years. 

That means Hugo provides free themes that users can download and use. That makes it very attractive to people who do not have experience with HTML, CSS and JS technologies, and most importantly don’t want to stress about setting up runtimes, dependencies and managing databases.

If you are a person who’d like to build a blog, a simple landing page or a portfolio website, Hugo could be a good option for you.

# Hugo Basics
Hugo has a well-structured documentation which is available on the website [gohugo.io](https://gohugo.io) and it can easily get you started. This project has also a community and a GitHub page if you need further assistance and information.

For that reason, I am not going to detail the Hugo Modules, Functions, Templates, Variables, etc, as they do a great job there.

However, what I am going to focus on in this article is how I built my website and how I used two different Hugo Themes.

# My Hugo Website
## Website Components: Tools And Services
Firstly, I am going to cover the different tools and services that I’ve selected to build my Hugo Website. 

Of course the most important one being Hugo running my local machine. The other piece of software that I have is [Visual Studio Code](https://code.visualstudio.com) (a code editor) that allows me to create, change and delete the different files of my project.

The last two ones are [Github](https://github.com/) which provides a distributed version control service and Netlify which offers a deployment and hosting platform for web applications and dynamic websites.

## My Website Structure
Hugo requires a specific project folder structure to organise the source content and it will use the content within these folders to render the website correctly. 

When creating a new website using Hugo, this will generate a new directory with the right folders in it.

The content such as website posts should be placed under content. 

| ![](/img/hugo1.jpg) |
| :--: |
| **Figure 1:** Content Folder.  |

The static assets such as images should be placed under the static folder. 


| ![](/img/hugo2.jpg) |
| :--: |
| **Figure 2:** Static Folder.  |

The templates (A.K.A themes) should be placed under the themes folder.

| ![](/img/hugo3.jpg) |
| :--: |
| **Figure 3:** Themes Folder.  |

# How to use two Hugo themes
When building the website I wanted to use two different themes, one for the main page and another one for my resume page. As of Oct 2022, Hugo does not support multiple themes by default. 

There are many threads out there discussing this topic:
- [How to have two themes for different sections of a site?](https://discourse.gohugo.io/t/how-to-have-two-themes-for-different-sections-of-a-site/1948)
- [Multiple themes per site](https://discourse.gohugo.io/t/multiple-themes-per-site/12039)
- [Hugo theme within another theme](https://stackoverflow.com/questions/59208233/hugo-theme-within-another-theme)

[Sami Tok](https://www.egementech.com/author/sami-tok/) proposes a solution [here](https://www.egementech.com/blog/hugo-multi-theme/).

The way I overcame this challenge myself was by building two different websites (each one with its own theme) and then copying the output files under the public folder of the resume page to the main website. I had to make sure the main page was able to locate the objects such as markdown files, HTML and CSS files for the resume page so I had to change some of the paths in the main page.

# Final Thoughts
Using Hugo was fun and easy and does not require a lot of expertise with HTML, CSS, JS and Markdown technologies. I believe it is a good alternative to Wordpress and for people who are not Web2 native developers. Due to the availability of themes, Hugo users can automate the process of building static websites and therefore that makes it very interesting for blog-type websites where articles follow a specific structure and content get updated often.  


