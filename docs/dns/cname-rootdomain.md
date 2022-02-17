---
layout: default
title: Configuring DNS for a Root Domain
nav_order: 8
parent: DNS
permalink: /dns/cname-rootdomain
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

These instructions take you through the general steps required to set up your DNS for use with a root domain such as `example.com`. If you would prefer to only use a subdomain (e.g. `www.example.com` or `sub.example.com`), please see [Configuring DNS for a Subdomain](https://quic.cloud/docs/cdn/dns/setting-up-your-dns-with-your-subdomain/).

These instructions are for setting up your existing DNS records at an external DNS provider. If you are switching to QUIC.cloud DNS, please see [Using QUIC.cloud DNS](https://quic.cloud/docs/cdn/dns/setting-up-your-dns-with-quic-cloud/).

## Keep a Reference


Log into your DNS provider. The first thing you should do, before you change anything, is to take a screenshot of your configuration. You want to have a reference in case you want to revert back.

## Provider-Specific Instructions

Here are some of the provider instructions we know about. If you don't see your provider here, follow the **General Instructions** below.

*   [Cloudflare](https://support.cloudflare.com/hc/en-us/articles/360019093151-Managing-DNS-records-in-Cloudflare) (`CNAME`)
*   [DNSimple](https://support.dnsimple.com/articles/alias-record/) (`ALIAS`)
*   [DNSMadeEasy](https://support.dnsmadeeasy.com/support/solutions/articles/47001001412-aname-records) (`ANAME`)
*   [Hostinger](https://support.hostinger.com/en/articles/4738777-how-to-add-and-remove-cname-records-on-hpanel) (`CNAME`)
*   [Name.com](https://www.name.com/support/articles/115010493967-Adding-an-ANAME-Alias-record) (`ANAME`)


## General Instructions

### Create an A Record

Create a new `A` record that points to your IP. You can give it any domain name that you'd like. It will serve as a back-up record in case you need to switch QUIC.cloud off. Example: `origin.example.com`

### Create a CNAME Record (OPTIONAL)

If you want to also use a subdomain (like `www.example.com`) with your root domain, it needs to have a `CNAME` record.

1.  If there is currently an `A` record for the subdomain, delete it.
2.  Add a `CNAME` record. Set **Name** to your subdomain (`www.example.com`), **Value** to your root domain (`example.com`), and keep the TTL set to the lowest possible value.

### Create an ALIAS, ANAME, or Flattened CNAME Record

1.  Delete the `A` record for your root domain.
2.  Create an `ALIAS`, `ANAME`, or `CNAME` record, depending on which one your DNS provider supports. Set **Name** to your root domain, **Value** the same as the backup `A` record you created earlier (e.g.`origin.example.com`), and keep the TTL set to the lowest possible value.

Visit your site and verify that you can still access everything properly.

**NOTE:** At this point, all you have done is make some local changes to your own DNS. QUIC.cloud is not involved in this process. If you are having issues accessing your site, then it is not related to QUIC.cloud. It is likely to be an error in your DNS configuration. Refer to the backup screenshot you took before you started.

### Edit the ALIAS/ANAME Record

That `ALIAS` or `ANAME` record you added earlier now must be used to connect to QUIC.cloud. Edit it and change the **Value** field to the domain name given to you in [your Dashboard](https://my.quic.cloud) (e.g. `c12345.tier1.quicns.com`).

Visit your site again and verify that you can still access everything properly.

If it is not accessible, review your DNS configurations and run through the steps again. Check if your TTL for the old configuration has expired. Make sure that the correct amount of time has elapsed.

## Next Step
{: .no_toc} 
- [Enable the CDN](/quic-cloud-doc/cdn)