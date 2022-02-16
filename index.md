---
layout: default
title: Home
nav_order: 1
description: "QUIC.cloud is a WordPress Acceleration Platform, the first and only complete WordPress optimization solution."
permalink: /
---

# QUIC.cloud
{: .fs-9 }

QUIC.cloud is a WordPress Acceleration Platform, the first and only complete WordPress optimization solution.
{: .fs-6 .fw-300 }

---

## Prerequisites
- A [WordPress](https://wordpress.com/) site
- A [LiteSpeed Cache for WordPress plugin](https://litespeedtech.com/products/cache-plugins/wordpress-acceleration)

## Getting Started
Pairing WordPress and QUIC.cloud is required, but creating a QUIC.cloud account is not.

To pair your WordPress site with QUIC.cloud in order to use any online services 
- [Pairing WordPress and QUIC.cloud](/quic-cloud-doc/pairing) 

Once you have paired WordPress with QUIC.cloud, you can begin using [Image Optimization](https://quic.cloud/quic-cloud-services-and-features/image-optimization-service), [Page Optimization](https://quic.cloud/quic-cloud-services-and-features/critical-css-service) and other cloud services immediately.

To use CDN Service, there're more steps that you need to follow
1. [Creating a QUIC.cloud account](/quic-cloud-doc/account)
2. [Setup DNS](/quic-cloud-doc/dns)
3. [Setup CDN](/quic-cloud-doc/cdn)

## About QUIC Cloud

QUIC Cloud is &copy; 2021-{{ "now" | date: "%Y" }} by [QUIC.cloud](https://quic.cloud/)
Learn more at [QUIC.cloud](https://quic.cloud/).


## Contributors
Many thanks to our QUIC Cloud Documentation contributors!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>


