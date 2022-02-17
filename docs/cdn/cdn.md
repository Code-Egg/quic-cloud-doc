---
layout: default
title: CDN
nav_order: 6
has_children: true
permalink: /cdn
---


## Start Using the CDN

Once your DNS is configured, there are a few simple steps to get started using the CDN.

### Turn on QUIC.cloud CDN

From your WordPress dashboard, navigate to **LiteSpeed Cache > CDN**, set **QUIC.cloud CDN** to `ON`, and press the **Save Changes** button.

### Enable the CDN

Navigate to **CDN** and press the **Enable CDN** button.

From there, QUIC.cloud may walk you through additional setup screens, especially if [your DNS is not yet verified](https://quic.cloud/docs/cdn/troubleshooting/domain-verification-issues/). If everything is fine with your DNS, then within a few minutes the CDN should be enabled and an SSL certificate automatically generated. You can click the **Refresh Status** link if you are impatient.

## Configure Your Firewall

When your site goes through QUIC.cloud servers, all the requests to your origin server come from QUIC.cloud IPs. This will likely trigger some firewall rules. Add the [QUIC.cloud IPs to your firewall's allowlist](https://quic.cloud/docs/getting-started/adding-quic-cloud-ips-to-allowlist/) to avoid triggering security rules.

## Verify

Here's a simple way to tell if QUIC.cloud CDN is serving your site: Use the [LSCache Check tool](https://check.lscache.io)

Enter your URL, and check the response headers. Look for the `x-qc-pop` header. If it’s there, it means your site was accessed via a QUIC.cloud PoP, your site was configured correctly, and you are good to go!