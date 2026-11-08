# Best dedicated hosts: is $79/month enough, when does managed pay for itself, and what does the price turn into at renewal? (full plan table + a five-provider cost check)

Dedicated hosting generally starts above $100 a month, while shared hosting sits under $10, so any price in between needs a reason. SpinServers' Dallas catalogue opens at **$79/month** for a 4-core Xeon E3-1280 v5 with 32GB of ECC memory, a 1TB NVMe drive and 30TB of monthly transfer on a 10Gbps port, provisioned automatically. That is below most entry tiers in the big comparison roundups, and the machine is bare metal: you get hardware and bandwidth, you supply the systems administration.

Three things decide whether that is a good deal: what the price becomes after the first term, what management costs if you do not want to run the box yourself, and whether you can get your money back when the configuration turns out wrong. All three are covered below, along with every SpinServers configuration currently listed and a five-provider cost check.

If your site runs happily on a $3 to $20 shared or managed WordPress plan and traffic is flat, dedicated hosting is not the answer. The rest of this page is for sites, apps and datasets that have outgrown a VPS.

## The short answer: which configuration most buyers should start with

> The Dallas **Intel Xeon E3-1280 v5** (4 cores / 8 threads, 32GB DDR4 ECC, 1TB M.2 NVMe, 30TB on a 10Gbps port, 1 IPv4) at **from $79/month**, billed monthly, is the right starting point for a single high-traffic WordPress or WooCommerce site, a busy API, a VPN or game server, or any workload where the database is the bottleneck rather than raw core count. Move up only when you can name the resource you are short of.
>
> 👉 [See the Dallas E3-1280 v5 configuration and its current price](https://bit.ly/Spinservers)

The reason to start low is that dedicated hardware is sold in coarse steps. Doubling cores roughly doubles the bill, while most sites run out of disk throughput or memory long before they run out of cores. NVMe storage and 32GB of RAM solve the two problems that actually cause slowdowns on a single-server site.

## Every SpinServers configuration, Dallas and San Jose

SpinServers sells bare metal in two locations, Dallas, Texas and San Jose, California. All prices below are USD and billed monthly. Where a build is priced individually rather than printed as a "from" rate, the order link goes to that configuration.

**Dallas, TX**

| Configuration | CPU | RAM | Storage | Network | Price / order |
| --- | --- | --- | --- | --- | --- |
| Intel Xeon E3-1280 v5 | 4C / 8T, 3.7GHz turbo | 32GB DDR4 ECC | 1TB M.2 NVMe | 30TB on 10Gbps, 1 IPv4 | **From $79/mo** ·  [order](https://bit.ly/Spinservers) |
| Dual Xeon E5-2630L v3 | 16C / 32T, 2.90GHz turbo | 128GB DDR4 ECC | 1TB NVMe | 30TB on 10Gbps | [check price](https://bit.ly/Spinservers) |
| Dual Xeon Gold 6148 | 40C / 80T, 3.70GHz turbo | 256GB DDR4 | 2 × 1.92TB SSD | 30TB, 2 × 10Gbps (LACP) | [check price](https://bit.ly/Spinservers) |
| Dual Xeon Platinum 8173M | 56C / 112T, 3.50GHz turbo | 512GB DDR4 | 4 × 1.92TB SSD | 30TB, 2 × 10Gbps (LACP) | [check price](https://bit.ly/Spinservers) |

**San Jose, CA**

| Configuration | RAM | Storage | Network | Provisioning | Price / order |
| --- | --- | --- | --- | --- | --- |
| 12C / 24T, 2.6GHz (3.1 turbo) | 64GB DDR3 ECC | 1 × 240GB SSD | 2 × 10Gbps, 30TB, 1 IPv4 | Instant | [check price](https://bit.ly/Spinservers) |
| 4C / 8T, 3.7GHz (4.0 turbo) | 32GB DDR4 ECC | 1 × 1TB M.2 NVMe | 2 × 10Gbps, 30TB, 1 IPv4 | Instant | [check price](https://bit.ly/Spinservers) |
| 16C / 32T, 1.8GHz (2.9 turbo) | 64GB DDR4 | 1 × 1.6TB SSD | 2 × 10Gbps, 30TB | Instant | [check price](https://bit.ly/Spinservers) |
| 16C / 32T, 1.8GHz (2.9 turbo) | 64GB DDR4 | 1 × 1.6TB NVMe | 2 × 10Gbps, 30TB, 1 IPv4 | Instant | [check price](https://bit.ly/Spinservers) |
| 24C / 48T, 1.8GHz (2.5 turbo) | 64GB DDR4 | 1 × 1.6TB SSD | 2 × 10Gbps, 30TB | Instant | [check price](https://bit.ly/Spinservers) |
| 16C / 32T, 1.8GHz (2.9 turbo) | 256GB DDR4 | 2 × 1.6TB SSD, hardware RAID | 2 × 10Gbps, 30TB | Instant | [check price](https://bit.ly/Spinservers) |
| 32C / 64T, 2.1GHz (3.0 turbo) | 512GB DDR4 | 2 × 3.84TB SSD, RAID w/ battery-backed cache | 2 × 10Gbps, 30TB, 1 IPv4 | Instant | [check price](https://bit.ly/Spinservers) |

Two practical notes on the network figures. The Dallas boxes ship with a single 10Gbps port and 30TB of monthly transfer; the San Jose boxes pair two 10Gbps ports, which matters if you plan to bond them or run failover. And 30TB a month works out to roughly **93Mbps sustained** if you spread it perfectly evenly across 30 days, so the port speed is there for bursts, backups and migrations rather than for a constant 10Gbps firehose.

## What the second year costs

Introductory pricing is the oldest trick in hosting, and it is not confined to cheap shared plans. Here is the arithmetic on the numbers each provider publishes.

| Provider | First-term price | Renewal price | 24-month total | Then, per year |
| --- | --- | --- | --- | --- |
| IONOS (1TB HDD tier, 2-year term) | $48/mo | $75/mo | $1,152 | $900 |
| IONOS (480GB SSD tier) | $55/mo | $85/mo | $1,320 | $1,020 |
| InMotion Hosting | $35/mo | $69.99/mo | $1,259.88 | $839.88 |
| SpinServers Dallas E3-1280 v5 | $79/mo, billed monthly | confirm at order | $1,896 | $948 |

Read the SpinServers column honestly: on sticker price alone, IONOS wins. Over two years the IONOS HDD deal costs $744 less than the $79 Dallas box, and even the SSD tier is cheaper. What the extra money buys is a different machine. IONOS's entry tier is 16GB of RAM, a spinning disk and a 1Gbit/s unmetered port; SpinServers gives you 32GB, NVMe and 10Gbps with 30TB of transfer. If your workload genuinely fits in 16GB with an HDD, take the cheaper deal and put the difference somewhere else.

InMotion's numbers show the opposite pattern worth knowing about. Its dedicated line starts at $35/month and renews at $69.99, which doubles the bill in year two. Within the same company, only the entry Aspire and CC-1000 plans jump at renewal, while the rest renew at their initial price. Renewal rules are set per plan, not per brand, so the only safe move is to read the renewal line for the specific configuration you are buying.

The Windows tax deserves its own line. IONOS charges **$35 to $38 per month extra** for Windows on its cheap server deals, which is $420 to $456 a year on top of the plan. Linux dedicated servers typically run about $20/month less than their Windows equivalents across the industry. If a provider quotes you a headline price and you intend to run Windows, add that back before comparing.

## Managed or unmanaged: where the money actually goes

SpinServers sells bare metal. You get the hardware, the network and the IP, and everything above the operating system is your problem: patching, firewall rules, backups, monitoring, and the 3 a.m. call when a disk fails. That is why the entry price is $79 rather than $250.

Unmanaged is cheaper and gives you full control, but you carry the firewall and the maintenance yourself. Managed means the provider handles OS updates, monitoring and security patching; you pay for labour rather than silicon, so the same monthly budget buys noticeably fewer cores and less RAM. Neither is better. They suit different teams.

The dividing line is easy to apply. If nobody on your team can comfortably rebuild a compromised server from backups, you need either a managed plan or a budget for someone who can. A single-site WordPress install with a caching stack is well within reach of a competent generalist; a multi-tenant SaaS with a database cluster is not. The worst outcome is buying unmanaged to save $100 a month and losing a weekend of revenue the first time something breaks.

👉 [Check exactly what the $79 Dallas bare-metal configuration includes before you decide](https://bit.ly/Spinservers)

## The line items that are not in the headline price

Add-ons are where hosting bills drift. Real examples from the roundups: Plesk on Liquid Web costs **$26/month** on top of the server; IONOS sells cloud backup at **$7/month**; Liquid Web's Server Secure Plus security bundle runs **$10 to $49/month** depending on what you enable. None of these are unreasonable, and all of them change the total.

"Configurable" is also doing less work than it appears. On IONOS, the configure step lets you change RAM, storage and operating system, and not much else. HostGator goes the other way: its dedicated resources are barely customisable at all, but you can pay monthly, quarterly, semi-annually, annually or over three years, which makes it a reasonable place to run a short project. SpinServers sits at the other end of the spectrum, with a fixed catalogue of pre-built configurations you pick from rather than a configurator, which is why the specs per dollar are strong and the lead time is short.

## Uptime percentages and refund windows, translated

Uptime guarantees sound identical until you convert them into downtime. Over a 365-day year:

- **99.9%** allows about 8 hours 46 minutes of downtime.
- **99.99%** allows about 52 minutes.
- **99.999%** allows about 5 minutes.
- **99.9999%**, the figure Hostwinds advertises, allows about 31.6 seconds for the entire year.

A single percentage point between 99.9% and 99.99% is the difference between an afternoon down and a coffee break. Check what the guarantee actually covers too: Liquid Web's SLA covers network uptime and pays credits when it misses, which is a narrower promise than "your site is always up."

Refunds vary more than uptime. A 30-day money-back window is the common industry value, offered by Bluehost, IONOS, Liquid Web and HostGator. Atlantic.Net states plainly that it offers no money-back guarantee at all. If you are testing an unfamiliar provider, the refund window is worth more than a spec sheet, because the configuration you regret is the one you cannot return.

## Five providers side by side

Pure information, no links: these are the entry prices and terms each provider's comparison listing showed. Treat them as a starting point, since renewal terms and promotions change.

| Provider | Entry price as listed | Renewal | Entry specs | Money-back |
| --- | --- | --- | --- | --- |
| IONOS | $48/mo on a 2-year term ($55 SSD tier) | $75/mo ($85 SSD) | 16GB RAM, 1TB HDD, unmetered 1Gbit/s | 30 days |
| Liquid Web | $77.50/mo unmanaged | Not stated | 16GB RAM, 2 × 480GB, 10TB transfer | 30 days |
| InMotion Hosting | $35/mo | $69.99/mo | 1TB SSD | Not listed |
| HostGator | $144.19/mo | Not stated | 32GB RAM, 1000GB storage, unmetered | 30 days |
| Atlantic.Net | $99/mo | Not stated | 64GB RAM, 20TB on 1Gbps, 2 × 480GB SSD RAID1 | None |

IONOS appears at $41/month on one roundup and $48 on another because the lower figure does not state the commitment behind it. Go with the $48 number if you want to compare like for like, and remember that Liquid Web's $77.50 is its unmanaged tier: managed service from the same company costs more, and Plesk or its security bundle adds to that.

## Matching the configuration to the workload

**One busy site, WooCommerce or a membership build.** Dallas E3-1280 v5 at $79. Four fast cores plus NVMe handles PHP and MySQL comfortably once caching is in place. You are buying disk throughput, not cores.

**Ten or more sites, or a heavy database.** Dual Xeon E5-2630L v3 in Dallas with 128GB of RAM. Memory is what lets you keep query caches and several application stacks resident instead of swapping.

**SaaS with sustained concurrency.** Dual Xeon Gold 6148 (40C / 80T, 256GB) or the San Jose 32C / 64T with 512GB and battery-backed RAID. Redundant storage matters more than clock speed once you have paying users.

**Latency-sensitive workloads and APAC traffic.** San Jose. The Dallas and San Jose catalogues overlap in spec, so pick on geography, not on price.

**Regulated or isolated workloads.** Bare metal gives you the isolation and predictable performance that shared virtualisation cannot, which is the main reason regulated workloads move off VPS in the first place. Ask any provider directly about compliance documentation before you commit.

**Short-term projects.** Do not sign a two-year term to save $20 a month on a three-month project. Monthly billing costs more per month and less in total when you leave early.

## Before you order

1. **Get the renewal price in writing**, even on monthly billing. Ask whether the listed rate is introductory.
2. **Confirm the cancellation terms.** Not every provider offers 30 days; Atlantic.Net offers none at all.
3. **Price the licences separately.** Windows adds $35 to $38/month at IONOS; a control panel can add $26.
4. **Check whether DDoS protection and backups are included or extra.** They are bundled at some providers and sold as add-ons at others.
5. **Pick the location by audience.** Dallas for North America and Europe, San Jose for the West Coast and Asia.
6. **Confirm the bandwidth policy.** Ask what happens if you exceed the monthly transfer allowance rather than assuming it is free.

## FAQ

**Is $100/month enough for a dedicated server?**
Yes, for entry-level hardware. SpinServers starts at $79/month, Liquid Web's unmanaged tier at $77.50, IONOS at $48 on a two-year commitment. Budget the add-ons on top: Windows licensing, a control panel, management, backups.

**Can I run an unmanaged server myself?**
You need to be comfortable with SSH, firewall rules, OS patching, backup verification and incident response. If any of those would be a first-time experience, a managed plan is cheaper than the outage.

**SSD or HDD?**
SSDs are faster and more resilient, cost more and hold less; HDDs are large and cheap but less durable. Unless you need very fast storage, a traditional hard drive is enough for file storage, while databases and application files belong on NVMe. Aim for 1TB or more of usable disk either way.

**Do I need a 10Gbps port?**
For most sites, no. 30TB of monthly transfer averages out to about 93Mbps if spread evenly, so a 1Gbit port is not the limiting factor. The faster port earns its keep during backups, migrations and traffic spikes.

**Can I upgrade later?**
With a fixed catalogue, upgrading usually means migrating to a different server rather than adding a stick of RAM. Plan for roughly double your current needs so the move can wait.

## How to decide

If you need one fast server and you can administer it, the Dallas E3-1280 v5 at **$79/month** with 32GB and 1TB NVMe is the configuration to start with, and the $21 difference over a cheaper 16GB HDD plan buys you the two resources that actually cause slowdowns. If you need many cores or large memory, the dual E5-2630L v3 at 128GB or the Gold 6148 at 256GB are the next two rungs, and both provision automatically. If you cannot run the box yourself, price a managed plan from another provider into the comparison honestly rather than discovering the gap at 3 a.m.

Two checks before you pay: confirm the renewal rate and the cancellation window in writing. Those two lines decide what the server really costs, and they are the lines sales pages tend to leave for the checkout page.

👉 [Start with the $79/month Dallas configuration and see the full SpinServers catalogue](https://bit.ly/Spinservers)
