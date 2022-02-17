---
layout: default
title: Configuring DNS for a Subdomain
nav_order: 7
parent: DNS
permalink: /dns/cname-subdomain
---

{: .no_toc} 

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}

</details>

These instructions take you through the general steps required to set up your DNS for use with a subdomain such as `www.example.com` or `sub.example.com`. If you would prefer to use your root domain (e.g. `example.com`), please see [the main DNS area](https://quic.cloud/docs/cdn/dns/) for the available options.

These instructions are for setting up your existing DNS records at an external DNS provider. If you are switching to QUIC.cloud DNS, please see [Using QUIC.cloud DNS](https://quic.cloud/docs/cdn/dns/setting-up-your-dns-with-quic-cloud/).

## Keep a Reference

Log into your DNS provider. The first thing you should do, before you change anything , is to take a screenshot of your configuration. You want to have a reference in case you encounter an issue and you want to revert back.

## Provider-Specific Instructions

Here are some of the provider instructions we know about. If you don't see your provider here, follow the **General Instructions** below.

*   [Azure](https://docs.microsoft.com/en-us/azure/dns/dns-operations-recordsets-portal)
*   [Cloudflare](https://support.cloudflare.com/hc/en-us/articles/360019093151-Managing-DNS-records-in-Cloudflare)
*   [cPanel](https://docs.cpanel.net/cpanel/domains/zone-editor/#manage-zone)
*   [Digital Ocean](https://docs.digitalocean.com/products/networking/dns/how-to/manage-records/)
*   [DNSimple](https://support.dnsimple.com/articles/manage-cname-record/)
*   [DNSMadeEasy](https://support.dnsmadeeasy.com/support/solutions/articles/47001001393-cname-record)
*   [Hostinger](https://support.hostinger.com/en/articles/4738777-how-to-add-and-remove-cname-records-on-hpanel)
*   [Name.com](https://www.name.com/support/articles/115004895548-Adding-a-CNAME-Record)
*   [Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/9646/2237/how-to-create-a-cname-record-for-your-domain/)

## General Instructions

### Create a CNAME Record

The subdomain you are planning to use with QUIC.cloud needs to have a `CNAME` record.

1.  If there is currently an `A` record for the subdomain, delete it.
2.  Add a `CNAME` record. Set **Name** to your subdomain (`www.example.com`), **Value** to your root domain (`example.com`), and keep the TTL set to the lowest possible value.

Visit your site and verify that you can still access everything properly.

**NOTE:** At this point, all you have done is make some local changes to your own DNS. QUIC.cloud is not involved in this process. If you are having issues accessing your site, then it is not related to QUIC.cloud. It is likely to be an error in your DNS configuration. Refer to the backup screenshot you took before you started.

### Edit the CNAME Record

That `CNAME` record you added earlier now must be used to connect to QUIC.cloud. Edit it and change the **Value** field to the domain name given to you in [your Dashboard](https://my.quic.cloud) (e.g. `c12345.tier1.quicns.com`).

Visit your site again and verify that you can still access everything properly.

If it is not accessible, review your DNS configurations and run through the steps again. Check if your TTL for the old configuration has expired. Make sure that the correct amount of time has elapsed.


## Next Step
{: .no_toc} 
- [Enable the CDN](/quic-cloud-doc/cdn)