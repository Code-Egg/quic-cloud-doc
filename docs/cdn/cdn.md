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

[![Turn on CDN in WordPress Plugin](https://quic.cloud/wp-content/uploads/2020/04/Screenshot-2021-08-05-153527.png)](https://quic.cloud/wp-content/uploads/2020/04/Screenshot-2021-08-05-153527.png)

From your WordPress dashboard, navigate to **LiteSpeed Cache > CDN**, set **QUIC.cloud CDN** to `ON`, and press the **Save Changes** button.

### Add Your Server IP

[![Add Server IP](https://quic.cloud/wp-content/uploads/2020/04/Screenshot-2021-08-05-153438.png)](https://quic.cloud/wp-content/uploads/2020/04/Screenshot-2021-08-05-153438.png)

Back in your QUIC.cloud dashboard, navigate to **Settings**, set **Server IP** to your domain's IP address, and press the **Save Settings** button.

If you don't know your site's IP address, open your browser's developer tools, go to the **Network** tab, load up a page on your site, and look for the `Remote Address` response header.

### Enable the CDN

[![Enable CDN at QUIC.cloud](https://quic.cloud/wp-content/uploads/2020/04/Screenshot-2021-08-05-153503.png)](https://quic.cloud/wp-content/uploads/2020/04/Screenshot-2021-08-05-153503.png)

Navigate to **CDN** and press the **Enable CDN** button.

From there, QUIC.cloud may walk you through additional setup screens, especially if [your DNS is not yet verified](https://quic.cloud/docs/cdn/troubleshooting/domain-verification-issues/). If everything is fine with your DNS, then within a few minutes the CDN should be enabled and an SSL certificate automatically generated. You can click the **Refresh Status** link if you are impatient.

Configure HTTP Access
------------------------------------------------

From the same **CDN** page you are currently on, navigate to **CDN Config > Connection**. Here you can define the way that QUIC.cloud connects with your origin server, and your site visitors.

[![Configure HTTP Access](https://quic.cloud/wp-content/uploads/2020/04/Untitled.png)](https://quic.cloud/wp-content/uploads/2020/04/Untitled.png)

*   **Connection Type to Origin**: How do you want QUIC.cloud to connect to your origin server? QUIC.cloud can either `Match` your backend server's connection type (which could be either HTTP or HTTPS), or it can always use `HTTP Only`.
*   **Frontend Force HTTPS**: How do you want to connect to your site's visitors? If set to `ON`, QUIC.cloud will force an HTTPS connection. If `OFF`, it will either match your origin server, or default to HTTP, depending on the value of **Connection Type to Origin**.
*   **Enable QUIC Backend**: If your origin server can handle QUIC and/or HTTP/3 connections, try this option. This will allow QUIC.cloud servers to attempt connecting to your origin server using QUIC and/or HTTP/3.

## Configure Your Firewall

When your site goes through QUIC.cloud servers, all the requests to your origin server come from QUIC.cloud IPs. This will likely trigger some firewall rules. Add the [QUIC.cloud IPs to your firewall's allowlist](https://quic.cloud/docs/getting-started/adding-quic-cloud-ips-to-allowlist/) to avoid triggering security rules.

## Verify

Here's a simple way to tell if QUIC.cloud CDN is serving your site: Use the [LSCache Check tool](https://check.lscache.io)

Enter your URL, and check the response headers. Look for the `x-qc-pop` header. If it’s there, it means your site was accessed via a QUIC.cloud PoP, your site was configured correctly, and you are good to go!