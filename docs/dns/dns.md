---
layout: default
title: DNS
nav_order: 5
has_children: true
permalink: /dns
---

In order to serve your site globally, QUIC.cloud CDN requires you to make changes to your DNS configuration. This can be done in one of two ways:

## Using the QUIC.cloud DNS Option

Regardless of whether you are using a root domain (`example.com`) or a subdomain (`www.example.com`), you can switch to QUIC.cloud's built-in DNS solution, , please see 
  - [Switching to QUIC.cloud DNS](/quic-cloud-doc/dns/quiccloud-dns)

## Using the CNAME Option

Some DNS providers offer CNAME flattening or [`ANAME`/`ALIAS` records](https://en.wikipedia.org/wiki/CNAME_record#ANAME_record), but many do not. If your DNS provider does not offer this feature, you must use a subdomain instead of your root domain (e.g. `www.example.com` instead of `example.com`) when setting up your DNS.

If you have a root domain, and you want to use the CNAME option, please make sure the provider offers CNAME flattening or `ANAME`/`ALIAS` records. Please see 
  - [Configuring DNS for a Root Domain](/quic-cloud-doc/dns/cname-rootdomain)

If you have a root domain, and your provider does not support CNAME flattening. Then you might want to use the QUIC.cloud DNS solution or Change your WordPress site so that it uses a www domain instead of the root domain.

If you have a `www` or other subdomain to be used with QUIC.cloud, please see 
  - [Configuring DNS for a Subdomain](/quic-cloud-doc/dns/cname-subdomain)


