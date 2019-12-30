+++ 
draft = false
date = 2019-12-30T10:40:54+01:00
title = "My Hosting Setup"
description = "I like my hosting automated, fail-safe and maintenance-free. Here's how I manage E-Mail, Webservices, Calendars and File-Sharing without Google."
slug = "my-hosting-setup" 
tags = ["hosting","dns","storage"]
categories = []
externalLink = ""
series = []
toc = false
+++

## What am I actually hosting
To get my life and work organized I make heavy use of good old E-Mail (still the No 1 communication channel in our industry), Calendars (using different calendars for Family, Work and Private matters), Shared Folders and supportive stuff like a Password Manager and Contacts Manager.

I don't want to rely on shared hosting at the big providers (Google) and I also don't want to split services between many cloud providers. I like having most of my stuff in one place that automates itself as much as possible. This includes all the tedious E-Mail-DNS-DKIM-SPF-stuff, Backups, Upgrades and Security (SSL Certificates for example).

## How am I actually hosting
I'm hosting many things that support my daily life and work but want to focus on the main communication Backbone I rely on daily.

All the things mentioned above are running on a single [Cloudron](https://cloudron.io/) instance hosted on a  [Netcup Root Server](https://www.netcup.de/vserver/). I like Netcup a lot. I haven't found another german hoster offering so much performance for basically no money - and I can cancel my subscription on a monthly basis if I don't like it anymore.

[Cloudron](https://cloudron.io/) must be the single most under-valued tool ever. Mine is running for over a year now at Netcup. Before I had it at server4you, then on a virtual machine in my internal network. I always migrated the live-data from one infrastructure to the next via Cloudrons excellent S3-Backup feature and never had any issue.

Cloudron runs the following Apps I use daily:
- Nextcloud
  - **Calendars**
  - **Contacts**
  - Passwords
  - **Files**
  - **Webmail**
  - **Document Editing**
- Minio (S3 Storage)
- Collabora (Document Editing in Nextcloud)
- Syncthing (I use this to keep my Development directory synced between this server and all my Devices)
- Matrix Homeserver (so you can reach me at fabian@hello.peter.saarland)
- A few Wordpress instances
- KodiMD (sometimes I want to write stuff down)
- **E-Mail**

The **bold** services are what enabled me to move away from Google entirely. I still have multiple Google Accounts, but I removed its non-search services from our lives months ago. No more Google Calendar, Drive, Contacts, Mail. Everything is handled by Cloudron and Nextcloud. For me, my work and my family.

It works exceptionally well and opens up additional opportunities for automation (e.g. I'm using [Node-Red]() to automate all accounting chores by scanning my INBOXes for relevant Mail and storing invoices and stuff in Nextcloud automatically for the accountant). Cloudron comes with a superb API that I use to automatically trigger reboots after updates when needed.

Cloudron handles E-Mail and DNS setup. You'll have to marry it to a DNS provider that also has an API (I opted for [Digitalocean](https://m.do.co/c/eed7786c83f3)), but it's worth it. Cloudron regularily updates SPF/DKIM records, adds Subdomains when you launch new apps, and more. Just **set and forget**. You create inboxes and connect.

![E-Mail](/img/cloudron-email.png)

Additionally, Cloudron handles all your backups. Ideally you backup to an external S3 storage. Since Digitalocean ffers [Spaces](https://m.do.co/c/eed7786c83f3) and DNS, it might make sense to use it for both. I personally opted for [Wasabi](https://wasabi.com/) here as they have more competetive pricing for storage.

![Backups](/img/cloudron-backups.png)

## How much is the fish?
Well, here's the catch. As opposed to Google, this doesn't come for free. My current setup costs about 60€ each month: 30€ for a Cloudron Premium Subcription, 20€ for the root server and 10€ for the S3 storage my backups use.

The Cloudron subscription is needed to install more of their so called "Premium Apps". Worth it!

![Backups](/img/cloudron-apps.png)

I'm happily paying it. The system not only does what I need from it, it's a platform to build upon (which I love!). It gets out of my way and doesn't require me to deal with tedious maintenance work or complex setup procedures. **It doesn't hold my data hostage!**. If I want to change hoster, platform or service, I simply export everything and move on.

It's super stable and reliable. I didn't have a single technical-related outage ever. And as mentioned, this setup powers my private stuff, work stuff and family stuff. There's clients for Nextcloud and E-Mail for every major platform, almost everything has an API I can tool with and it's all based on friggin Docker, so portability isn't an issue.

This setup backs most of my communication/automation needs and it's just working. And I can extend it - a lot more than I could extend hosted services (or Google Services). Data Privacy and Control is pretty important to me. I'm handling sensitive data from customers on a daily basis and I feel I can't guarantee any level of data security using hosted services.

The one thing I wish I could change to this setup is the hosting location. While Netcup is awesome, it's still someone else's hardware. Running Cloudron at home would definitely be possible, but comes with additional complexity. Reliably sending E-Mail from "private" IP addresses is virtually impossible due to all the Spammer-Panic the big providers still use as an excuse to limit global E-Mail transit to public IPs. Try to send E-Mail to Telekom, Hotmail, Google, etc from an IP adresse whose PTR record you don't control (which is basically the case for all private IP addresses coming from you local ISP) - most of the time, you will be blocked. As it's my primary tool of communication, I can't afford E-Mails not reaching their destination due to Provider-Limits, so I opt for the hosted version "in the cloud". I could overcome this by adding additional complexity (outgoing mail relay), but currently I don't think it's worth the effort.