---
title: "A Step-by-step Guide: How To Deploy a Hugo Website on Linode"
date: 2022-10-09T17:34:00+00:00
draft: true
layout: "single"
Donate: true
ShowWordCount: true
ShowReadingTime: true
disableShare: false
ShowPostNavLinks: false
ShowCodeCopyButtons: true
ShowBreadCrumbs: true
cover:
    image: "/img/sbs.jpg"
    responsiveImages: true
    hidden: true
tags: ["tech", "hugo", "open source", "website", "themes", "templates", "static page", "linode", "hosting"]
categories: ["Tech", "Building Websites", "Open-source"]
---

# TL;DR
Because Hugo renders static websites, you can host your new Hugo website virtually anywhere. This article describes the process of hosting and deploying a Hugo website on Linode - Akamai’s Cloud Computing Platform. 

# Step-by-step Guide

This guide has 3 main sections:
- How to spin up a Linode instance.
- How to point a Domain to the Linode instance.
- How to install and use Hugo to build a website.

# How To Spin Up A Linode Instance.
- Create a new Linode Instance Using the Linode Web Console.
- Select Ubuntu 22.04 LTS.
- Select the Region (London, UK).
- Select the plan that suits you.
- Once the instance is up and running, access the instance using SSH and enter the password.

```bash
ssh root@[instance_ip_address]
```

# How To Point A Domain To The Linode Instance
- Login into your DNS solution provider console.
- Create a DNS type A record and point it to the ```instance_ip_address``` provided by the Linode instance.

# How To Install And Use Hugo To Build A Website
Now are you connected to the Linode instance, it's time to play with Hugo.

- First things first, update your system apt index before installing Hugo.

```bash
sudo apt update
sudo apt -y install hugo
```

- You can confirm the location of Hugo binary after installation using which.

```bash
$ which hugo
/usr/bin/hugo
```

- And confirm the installed version.

```bash
$  hugo version
hugo v0.92.2+extended linux/amd64 BuildDate=2022-02-23T16:47:50Z VendorInfo=ubuntu:0.92.2-1
```
- Now that Hugo is installed, you can start creating the website. Before doing that, you’ll need to create new content for your site. In this example, the site is called akamai-hugo-linode-website.

```bash
hugo new site akamai-hugo-linode-website 
```

- Change into the directory of the new site.

```bash
cd akamai-hugo-linode-website
```

- Initialise a git repository.

```bash
git init
```

- Add the reveal-hugo theme as a submodule in the themes directory.

```bash
git submodule add https://github.com/dzello/reveal-hugo.git themes/reveal-hugo
```

- Open ```config.toml``` and add the following contents.

```toml
theme = "reveal-hugo"

[markup.goldmark.renderer]
unsafe = true

[outputFormats.Reveal]
baseName = "index"
mediaType = "text/html"
isHTML = true
```

- This tells Hugo to use the reveal-hugo theme and it registers a new output format called “Reveal”. Next, create a file in content/_index.md and add the following:

```markdown
+++
title = "My Presentation"
outputs = ["Reveal"]
+++

# Hello world!

This is my first slide.
```

- Now, initialise Hugo server.

```bash
hugo server
```

- Test the website within the Linode instance.

```bash
curl http://localhost:1313/
```

- The result is.

```html
<!doctype html>
<html lang="en">
  <head>
	<meta name="generator" content="Hugo 0.92.2" /><script src="/livereload.js?mindelay=10&amp;v=2&amp;port=1313&amp;path=livereload" data-no-instant defer></script>
    <meta charset="utf-8">
<title>My Presentation</title>

<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <link rel="stylesheet" href="/reveal-js/css/reset.css">
<link rel="stylesheet" href="/reveal-js/css/reveal.css"><link rel="stylesheet" href="/reveal-js/css/theme/moon.css" id="theme">
<link rel="stylesheet" href="/highlight-js/default.min.css">
    
  </head>
  <body>
    
    <div class="reveal">
      <div class="slides">

    <section><h1 id="hello-world">Hello world!</h1>
<p>This is my first slide.</p>
</section><section>
<h1 id="slide-2">Slide 2</h1>
<p>Hello Slide Number 2.</p>
</section><section>
<h1 id="slide-3">Slide 3</h1>
<p>Let&rsquo;s keep talking.</p>
</section><section>
<h1 id="slide-4">Slide 4</h1>
<p>In fact, I don&rsquo;t know what I am doing.</p>
</section><section>
<h1 id="but-let-me-tech-you-something-">But Let me tech you something &hellip;</h1>
<pre tabindex="0"><code class="nohighlight" data-noescape>graph LR
    Edge Server --&gt; Parent Server
    Parent Server --&gt; Origin
</code></pre></section>

</div>

    </div>
<script type="text/javascript" src=/reveal-hugo/object-assign.js></script>

<a href="/reveal-js/css/print/" id="print-location" style="display: none;"></a>
<script type="text/javascript">
  var printLocationElement = document.getElementById('print-location');
  var link = document.createElement('link');
  link.rel = 'stylesheet';
  link.type = 'text/css';
  link.href = printLocationElement.href + (window.location.search.match(/print-pdf/gi) ? 'pdf.css' : 'paper.css');
  document.getElementsByTagName('head')[0].appendChild(link);
</script>

<script type="application/json" id="reveal-hugo-site-params">{"theme":"moon"}</script>
<script type="application/json" id="reveal-hugo-page-params">null</script>

<script src="/reveal-js/js/reveal.js"></script>

<script type="text/javascript">
  
  
  function camelize(map) {
    if (map) {
      Object.keys(map).forEach(function(k) {
        newK = k.replace(/(\_\w)/g, function(m) { return m[1].toUpperCase() });
        if (newK != k) {
          map[newK] = map[k];
          delete map[k];
        }
      });
    }
    return map;
  }
  
  var revealHugoDefaults = { center: true, controls: true, history: true, progress: true, transition: "slide" };
  var revealHugoSiteParams = JSON.parse(document.getElementById('reveal-hugo-site-params').innerHTML);
  var revealHugoPageParams = JSON.parse(document.getElementById('reveal-hugo-page-params').innerHTML);
  
  var options = Object.assign({},
    camelize(revealHugoDefaults),
    camelize(revealHugoSiteParams),
    camelize(revealHugoPageParams));
  Reveal.initialize(options);
</script>
  
  <script type="text/javascript" src="/reveal-js/plugin/markdown/marked.js"></script>
  
  <script type="text/javascript" src="/reveal-js/plugin/markdown/markdown.js"></script>
  
  <script type="text/javascript" src="/reveal-js/plugin/highlight/highlight.js"></script>
  
  <script type="text/javascript" src="/reveal-js/plugin/zoom-js/zoom.js"></script>
  
  <script type="text/javascript" src="/reveal-js/plugin/notes/notes.js"></script>

  <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
  <script>
    mermaid.initialize({startOnLoad: false});
    let render = (event) => {
      let mermaidElems = event.currentSlide.querySelectorAll('.mermaid');
      if (!mermaidElems.length){
          return
      }
      mermaidElems.forEach(mermaidElem => {
          let processed = mermaidElem.getAttribute('data-processed');
          if (!processed){
              
              mermaid.init(undefined, mermaidElem);
          }
      });
    };
    Reveal.addEventListener('slidechanged', render);
    Reveal.addEventListener('ready', render);
  </script>
  </body>
</html>
```

- If you try to test from the public Internet (using the IP address or domain) you won’t be able to access the website. To make this website available to the public Internet you would need to deploy an Apache Server.

```bash
sudo apt install apache2 apache2-doc apache2-utils
```

- Now let’s check the status of the Apache Server.

```bash
$ systemctl status apache2

● apache2.service - The Apache HTTP Server
     Loaded: loaded (/lib/systemd/system/apache2.service; enabled; vendor preset: enabled)
     Active: active (running) since Mon 2022-10-03 10:51:21 UTC; 1min 22s ago
       Docs: https://httpd.apache.org/docs/2.4/
   Main PID: 3014 (apache2)
      Tasks: 55 (limit: 1030)
     Memory: 5.0M
        CPU: 64ms
     CGroup: /system.slice/apache2.service
             ├─3014 /usr/sbin/apache2 -k start
             ├─3016 /usr/sbin/apache2 -k start
             └─3017 /usr/sbin/apache2 -k start
```

- If you now use the public IP address of your Linode instance (or the domain) you will see that you will get the default page of the Apache server.
 
- Because we want to deploy a Hugo website we can disable the Apache2 Default page.

```bash
ls /etc/apache2/sites-available/

sudo a2dissite 000-default.conf

sudo systemctl reload apache2
```

- We would also need to configure the firewall to allow HTTP traffic on port 80 and 443 into the Apache server. We would also allow OpenSSH so we can continue accessing the instance using OpenSSH.

```bash
sudo ufw app list

sudo ufw allow 'Apache Full'

sudo ufw allow 'OpenSSH'

sudo ufw status

sudo ufw enable
```

- Now, we will create the directories for the new Hugo website.

```bash
cd /var/www/html/

sudo mkdir linode.jonathangoc.com

cd linode.jonathangoc.com

sudo mkdir public_html

sudo mkdir logs

sudo mkdir backups
```

- Once this is done, we will create the configuration file.

```bash
cd /etc/apache2/sites-available

sudo vi linode.jonathangoc.com.conf
```

- And add the configuration settings.

```
<VirtualHost *:80>
     ServerAdmin joncarva@akamai.com
     ServerName linode.jonathangoc.com
     ServerAlias linode.jonathangoc.com
     DocumentRoot /var/www/html/linode.jonathangoc.com/public_html/
     ErrorLog /var/www/html/linode.jonathangoc.com/logs/error.log
     CustomLog /var/www/html/linode.jonathangoc.com/logs/access.log combined
</VirtualHost>
```

- To enable the website we need to reload the apache server.

```bash
sudo a2ensite linode.jonathangoc.com.conf

sudo systemctl reload apache2
```

- Now, we should be set to copy the Hugo website created to the folder public_html folder previously created.

```bash
cd ~/akamai-hugo-linode-website/public
cp -r . /var/www/html/linode.jonathangoc.com/public_html/
```

- Finally, if you go to the browser and type the domain of your website (in my case: linode.jonathangoc.com) you will be able to fetch the website's content.


