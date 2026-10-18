# rent a vps: how pay-by-the-hour works, what Vultr really costs, and when it beats the $2.48/month hosts

Renting a VPS in 2026 puts you in one of two very different markets. Most budget hosts — Cloudzy, Regxa, KernelHost — sell fixed monthly plans: cheap, no contract, but you pay for the whole month even if the server is only needed for a weekend. Vultr runs on the opposite model: every plan is metered by the hour, starting at roughly a penny an hour, and billing stops the moment you delete the server. That single difference decides who should rent where. Below you'll find the current price landscape, Vultr's full standard plan lineup, the fine print that never makes it onto pricing pages, and a step-by-step of your first rental.

> **The short version:** for a real ongoing project, start with Vultr's High Performance 1 GB plan — a **$6/month cap**, NVMe storage, 1 TB transfer, and your pick of 32 data center locations. Rent it for a weekend and it costs about 48 cents. 👉 [Check Vultr's current plans and prices](https://www.vultr.com/pricing/?ref=7268283) — and keep in mind Vultr has no money-back guarantee, which sounds worse than it is: with hourly billing you never prepay more than a few dollars to find out whether it fits.

## What it costs to rent a VPS right now

For a usable 1 GB-class server, the current price range runs from about **$0.24 per day** at the true pay-per-use end to **$5–6 per month** at the cheapest no-contract monthly hosts, with promo pricing dipping under $3 for 512 MB boxes. Here's how the hosts ranking for this search compare:

| Host | Entry price | Billing model | What stands out | The catch |
| --- | --- | --- | --- | --- |
| Cloudzy | $2.48/mo (512 MB) | Monthly, no contract | 13 regions, 14-day money-back, 99.95% uptime SLA | The $2.48 is 50% off the $4.95 list price — renewals land at list |
| KernelHost | €4.99/mo | Monthly | Reserved single-tenant resources (VDS), Frankfurt, 3.2 Tbps Arbor DDoS protection, 99.99% SLA | One location; no pay-per-use option |
| Regxa | $4.50/mo | Monthly | 17+ Tbps DDoS protection, "truly unlimited" bandwidth | Unlimited bandwidth only applies in the US, Europe and Middle East — Asian locations (Singapore, India, Sydney) get plan-based caps |
| HourlyVPS | $0.24/day | Hourly meter, billed per day | KVM with NVMe, delete to stop billing | Small provider; plans top out around 64 GB RAM |

UltaHost sits slightly apart as a managed-first option — 55-second deployment, 24/7 support, free snapshots and DDoS protection, plus a 30-day money-back guarantee — which shows up in the price.

Two details in that table get glossed over in most comparisons. Cloudzy's headline $2.48 is a 50% launch discount off a $4.95 list price, so your second month at renewal costs nearly double the number in the ad. And Regxa's "truly unlimited bandwidth" comes with a footnote: it holds only for US, European and Middle Eastern locations, which matters a lot if your users are in Asia.

## Vultr's plans and prices (the full standard lineup)

Vultr's standard VPS product comes in two lines: **Regular Performance** (Intel cores, SSD storage) starting at $5/month, and **High Performance** (AMD EPYC, NVMe) starting at $6/month. Both use the same RAM, storage and transfer ladder; the High Performance line costs about 20% more for newer hardware. All prices are in US dollars, and every plan is billed hourly with a monthly cap — the cap is the most you'll ever pay in a month.

| Line | vCPU / RAM | Storage | Transfer | Monthly cap | Rent |
| --- | --- | --- | --- | --- | --- |
| High Performance | 1 vCPU / 1 GB | 25 GB NVMe | 1 TB | $6 | [Deploy](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| High Performance | 1 vCPU / 2 GB | 55 GB NVMe | 2 TB | $12 | [Deploy](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| High Performance | 2 vCPU / 4 GB | 80 GB NVMe | 3 TB | $24 | [Deploy](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| High Performance | 4 vCPU / 8 GB | 160 GB NVMe | 4 TB | $48 | [Deploy](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| High Performance | 8 vCPU / 16 GB | 340 GB NVMe | 5 TB | $96 | [Deploy](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| High Performance | 16 vCPU / 32 GB | 640 GB NVMe | 6 TB | $192 | [Deploy](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Regular | 1 vCPU / 1 GB | 25 GB SSD | 1 TB | $5 | [Deploy](https://www.vultr.com/pricing/?ref=7268283) |
| Regular | 1 vCPU / 2 GB | 55 GB SSD | 2 TB | $10 | [Deploy](https://www.vultr.com/pricing/?ref=7268283) |
| Regular | 2 vCPU / 4 GB | 80 GB SSD | 3 TB | $20 | [Deploy](https://www.vultr.com/pricing/?ref=7268283) |
| Regular | 4 vCPU / 8 GB | 160 GB SSD | 4 TB | $40 | [Deploy](https://www.vultr.com/pricing/?ref=7268283) |
| Regular | 8 vCPU / 16 GB | 340 GB SSD | 5 TB | $80 | [Deploy](https://www.vultr.com/pricing/?ref=7268283) |
| Regular | 16 vCPU / 32 GB | 640 GB SSD | 6 TB | $160 | [Deploy](https://www.vultr.com/pricing/?ref=7268283) |

A third line, **High Frequency**, starts at the same $6/month but pairs the 1 GB plan with a larger 32 GB NVMe disk on higher-clocked cores — worth a look if your workload is disk- or CPU-bound. Beyond these standard lines, Vultr also sells dedicated-CPU (Optimized Cloud Compute) instances and bare metal servers; those live on the same pricing page and make sense once a standard plan's shared vCPUs become the bottleneck.

Every plan includes a dedicated IPv4 and IPv6 address, free private networking between your instances, one-click OS images (Ubuntu, Debian, Rocky, Windows Server and more — Windows carries a license fee), plus a marketplace of prebuilt apps and custom ISO support. The transfer pool scales with the plan, from 1 TB on the entry tiers up to 6 TB at 32 GB.

## How hourly billing actually works

Every Vultr plan has an hourly rate and a monthly cap. Run the server all month and you pay exactly the cap. Delete it early and you pay only for the hours it existed. On the $6 High Performance plan that works out to roughly a penny per hour:

- **1 day:** 24 × $0.01 ≈ **$0.24**
- **3 days:** ≈ **$0.72**
- **1 week:** ≈ **$1.68**
- **Full month:** **$6.00** cap, no matter how many hours the month has

Now compare that to the monthly-only hosts. A weekend test server on Cloudzy costs you the $2.48 minimum plan price, whether it runs 48 hours or the full month. The same weekend on Vultr is about 72 cents. If you spin up servers a few times a year — a hackathon, a client proof-of-concept, a game server for a long weekend — the hourly model saves you an order of magnitude.

Vultr's hourly meter isn't a promotional gimmick — it's the platform's native billing, the same pay-for-what-you-use model the big clouds run on, which is why there's no minimum term anywhere on the site. For always-on workloads it changes nothing: the cap is the price, and $6 for 1 GB is comfortably in line with the market.

If that flexibility is what you came for, 👉 [deploy a High Performance server by the hour](https://www.vultr.com/products/cloud-compute/?ref=7268283) and delete it when the job's done — the billing follows the same button.

## The costs that don't show on the pricing page

Four things affect the real bill, and competitors rarely spell them out in their own comparisons.

**Bandwidth overage is billed per GB.** Vultr's included transfer pools are generous for typical sites, but if you exceed them, the overage runs about a penny per GB in most regions. Compare that with Regxa's "unlimited" bandwidth in the US/EU/Middle East or Cloudzy's advertised no-egress-fees stance: if you run a download-heavy or media-heavy service, a monthly host with flat bandwidth may price out better than a metered one.

**Snapshots bill separately, at $0.05/GB/month, and they keep billing after you delete the server.** This is the one cleanup step people forget: take a snapshot, delete the instance, and the snapshot storage quietly accrues charges until you remove it from the snapshots list.

**Automatic backups add 20% to the instance price.** Useful for anything persistent; skip it for throwaway servers you've already got in version control.

**DDoS protection is a paid add-on** (around $10/month per server). KernelHost and Regxa both bundle high-capacity DDoS filtering into their entry plans, so if your project is likely to get attacked — game servers and proxies often are — factor that in.

On refunds: Vultr doesn't offer a money-back guarantee, unlike Cloudzy's 14 days, UltaHost's 30 days or Regxa's pro-rated refunds. What offsets it here is the billing model itself. There's no annual prepay to regret and no setup fee, and Vultr has typically offered new accounts a signup credit (historically $100, valid for the first 30 days) that covers your first experiments entirely — check the current offer at signup. One practical note: some new accounts get asked for ID or payment verification before the first deployment, so have a card ready and don't leave it until an hour before you need the server.

## When Vultr is the wrong choice

Root access and a billing meter assume you can run a server yourself. If any of the following describes you, a monthly specialist will serve you better — and it's worth saying so plainly.

You want someone else on call. Vultr's included support is ticket-based, and you are the admin. UltaHost's entire pitch is the opposite: managed VPS rentals with 24/7 expert support, a 30-day money-back guarantee and a 99.99% uptime commitment, at a higher price that buys back your evenings.

You need guaranteed, non-shared performance. KernelHost's €4.99 VDS reserves the vCPU, RAM and NVMe exclusively for your instance, never shared, out of a TÜV Tier3+ certified Frankfurt datacenter with 3.2 Tbps of Arbor DDoS protection. For game or voice servers where a noisy neighbor ruins the evening, that reserved model is genuinely the better product — Vultr's standard lines are shared-tenant cloud.

You want a refund safety net above all else. Cloudzy's 14-day no-questions money-back window is real and straightforward. If your plan is "sign up, poke around for two weeks, decide," that structure beats a metered one on paper.

## Renting your first Vultr server, step by step

The whole process takes about five minutes, most of it spent choosing options.

1. **Create the account and add a payment method.** Cards work; verification is usually instant, but some new accounts get a short identity check before their first deploy.
2. **Deploy.** Choose Cloud Compute → High Performance, pick a plan (1 GB is enough for a blog, a bot, a VPN endpoint or a staging server), pick a location from the 32 available — New Jersey, Miami, Los Angeles, London, Frankfurt, Amsterdam, Tokyo, Singapore, Sydney, São Paulo and Johannesburg among them — then choose your OS image or a marketplace app. Upload an SSH key at this step and you'll never touch a password.
3. **Log in.** Deployment finishes in about a minute and hands you root credentials for SSH. The transfer pool, IPv4 and private networking are all live from that moment.
4. **Delete when done.** Billing stops at deletion, right there in the product list — stopping or powering off is not enough to stop the meter. Before you delete a temporary server: pull off your logs and data, remove the DNS records pointing at it, and revoke any API tokens or deploy keys it held. And if you took a snapshot you no longer need, delete that too, per the section above.

👉 [Open Vultr's plan picker](https://www.vultr.com/pricing/?ref=7268283) if you want to see how the exact configuration and price land on your region before committing to anything.

## FAQ

**Is there a minimum rental period on Vultr?** No. Billing is hourly with a monthly cap, there are no contracts, and you can delete a server minutes after creating it — you'd pay only for those minutes.

**How much does it cost to rent a VPS per day?** On the High Performance 1 GB plan, about $0.24 per day at the penny-per-hour rate, capped at $6 if it runs all month. Smaller daily figures aren't possible on the standard lines since 1 GB is the entry tier.

**Does Vultr offer refunds?** There's no standard money-back guarantee. The practical protection is that you're never prepaying: hourly billing plus the new-account credit means your first tests usually cost nothing. If you're unsure, top up a small balance rather than a large one.

**Vultr or Cloudzy for a cheap always-on server?** If the server runs 24/7 all year, Cloudzy's $2.48 promo plan is the cheaper first term, though it renews at $4.95 for 512 MB. Vultr's $6 gets you 1 GB, hourly flexibility, 32 locations and no renewal cliff. Short-lived or unpredictable workloads tip clearly to Vultr; a permanently-on micro-project on the tightest budget tips to the promo.

## Which one to rent, by situation

- Server for a weekend, a workshop or a release soak test: rent it hourly on Vultr and delete it when you're done — the whole exercise costs a couple of dollars.
- Always-on project on the smallest possible budget: the $2.48–$4.99 monthly tier from Cloudzy, KernelHost or Regxa does the job; just check the renewal price and the bandwidth fine print first.
- Guaranteed performance for a game or voice server: KernelHost's reserved VDS model is the better fit, even at the higher entry price.
- A server you don't want to administer at all: a managed rental like UltaHost's, with its 30-day money-back window.

For everything elastic — anything with a start date, an end date, or an uncertain future — 👉 [rent your first Vultr instance for a few cents an hour](https://www.vultr.com/pricing/?ref=7268283) and let the meter prove whether it's worth keeping.
