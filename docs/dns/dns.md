---
layout: default
title: DNS
nav_order: 2
has_children: true
permalink: /dns
---

In order to serve your site globally, QUIC.cloud CDN requires you to make changes to your DNS configuration. This can be done in one of two ways:

1.  You can add a `CNAME` record at your existing DNS provider, and point it to QUIC.cloud
2.  You can switch to QUIC.cloud's built-in DNS solution

The `CNAME` option is available mostly to those who wish to use a subdomain (like `www.example.com` or `sub.example.com` with QUIC.cloud, while the QUIC.cloud DNS option is available to everyone.

Using the CNAME Option
----------------------

Some DNS providers offer CNAME flattening or [`ANAME`/`ALIAS` records](https://en.wikipedia.org/wiki/CNAME_record#ANAME_record), but many do not. If your DNS provider does not offer this feature, you must use a subdomain instead of your root domain (e.g. `www.example.com` instead of `example.com`) when setting up your DNS.

If you have a `www` or other subdomain to be used with QUIC.cloud, please see [Configuring DNS for a Subdomain](/cname-subdomain) to proceed.

If you have a root domain, and you really want to use the CNAME option, you have two choices:

1.  Change your DNS provider to a provider that offers CNAME flattening or `ANAME`/`ALIAS` records, so you can continue to use your root domain. Please see [Configuring DNS for a Root Domain](/cname-rootdomain) to proceed.
2.  Change your WordPress site so that it uses a `www` domain instead of the root domain. Please see [Switching from a Root Domain to a www Domain](/root-www) to proceed.

Using the QUIC.cloud DNS Option
-------------------------------

Regardless of whether you are using a root domain (`example.com`) or a subdomain (`www.example.com`), you can switch to QUIC.cloud's built-in DNS solution. Please see [Switching to QUIC.cloud DNS](https://quic.cloud/docs/cdn/dns/setting-up-your-dns-with-quic-cloud/) to proceed.