---
layout: default
title: QUIC.DNS
nav_order: 2
parent: dns
permalink: /dns/quiccloud-dns
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

QUIC.cloud's own DNS solution is provided free of charge and allows you to use your root domain with QUIC.cloud CDN, if you wish. If you want to know more before you switch, check out [our blog post introducing QUIC.cloud DNS](https://quic.cloud/introducing-quic-cloud-dns/). 

## Import Existing DNS Records to QUIC.cloud 

Making QUIC.cloud your DNS provider takes only a few steps. 

1. From [your dashboard](https://my.quic.cloud), click on **DNS Zones** in the top menu. 
2. Click the **+Add New Domain to DNS Zones** link. 
3. Enter your domain name and press the **Add Domain** button. ![DNS Records](https://quic.cloud/wp-content/uploads/2020/10/Records.png) QUIC.cloud will attempt to detect your current DNS records. This may take a few minutes. Once detection is complete, you will be asked to confirm that your DNS information is correct. Accept all of the detected records, or uncheck any that you no longer need, and click the **+ Enable and Add Records** button. 

## Update Your Nameservers 

Once your DNS records have been imported into QUIC.cloud, you will need to instruct your domain registrar where to find your DNS records. ![QUIC.cloud Nameservers](https://quic.cloud/wp-content/uploads/2020/10/Name-Servers.png) Visit your QUIC.cloud **DNS Zone** and locate the two Nameservers displayed as `NS1` and `NS2`. These are the new Nameservers that you will need to save with your domain registrar. Your **domain registrar** is the the provider you purchased your domain name from. Sometimes this is the same as your hosting provider, but that is not always the case. Make sure that you are in the right place before you change anything! Log into your domain registrar. Your previous DNS provider's nameservers should still be on file. You'll see them listed under `NS1`, `NS2`, and possibly `NS3` and `NS4` as well. If your domain is registered with one of these providers, you can click the appropriate link below to follow their instructions for adding custom nameservers: - [Hostinger](https://support.hostinger.com/en/articles/1696789-how-to-change-nameservers-at-hostinger) - [GoDaddy](https://www.godaddy.com/help/change-nameservers-for-my-domains-664) - [Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/767/10/how-to-change-dns-for-a-domain/) If your registrar is not listed above, you'll need to look for the area of their site which allows you to manage Nameservers. It may be called "DNS Zone" or "Manage DNS" or something similar. Change the `NS1` and `NS2` records, to match those displayed in your QUIC.cloud **DNS Zone**. If your domain registrar has additional records (`NS3`, `NS4`, etc.) erase those values. You should now only have QUIC.cloud-provided NS records at your domain registrar. Once you've updated your domain registrar, come back to your QUIC.cloud **DNS Zone** and click the **Refresh Status** link. ## Verify After the above steps are complete, you can check the status of your domain's DNS with a tool like [DNSChecker.org](https://dnschecker.org/). There are typically delays due to DNS caching, but if your DNS has still not propagated after 24 hours, please open a [support ticket](https://quic.cloud/support/) and we'll look into it. 

