# cheap proxies: how to spot a fake per-GB headline, pick the right proxy type, and start at $1/GB with no subscription

Search for cheap proxies and you get a wall of numbers that mostly don't survive the checkout page. One large provider puts "$2.50/GB" in its site navigation and shows $4, $4, $3 and $3 on the plan cards below it, against a list price of $8. Another advertises $1.40/GB and charges $3.50 if you buy a single gigabyte. A third advertises $1.75/GB and charges $7 at 1 GB.

None of that is illegal. It's just the difference between the lowest rate on the biggest plan and the rate you actually pay. So the useful question isn't "who is cheapest" — it's "who is cheapest at my volume, for my type of target, after minimums, targeting surcharges and expiry rules."

That framing is what this article works through. It also explains why a provider selling residential traffic at a flat $1/GB with a $5 minimum — DataImpulse — keeps coming up first in low-volume comparisons, and where that model stops being the cheapest option at all.

## The four things that make a cheap proxy expensive

Advertised rate gaps are only the first problem. Four mechanisms move the real number, and three of them are buried.

**Entry minimums.** Below roughly 10 GB a month, the minimum is your price and the per-GB rate is decoration. Minimums across ten major providers range from $3.50 to $200 a month. Oxylabs fits a 5 GB user exactly at $6/GB, but its next plan up is 125 GB — so a 50 GB workload buys 75 GB it never uses, and the effective rate climbs to $10/GB.

**Expiring bundles.** Subscription providers reset unused gigabytes at the start of the next cycle. If your scraping schedule is lumpy, you're buying traffic you'll never spend. This is the single biggest argument for pay-as-you-go billing with non-expiring balances.

**Targeting surcharges.** Country-level targeting is usually included. City, ZIP and ASN often aren't. One provider bills advanced targeting filters on residential plans at double the standard per-GB rate, which turns a $1/GB figure into $2/GB for a city-targeted job.

**Proxy type.** Datacenter IPs come from servers, are plentiful, and are cheap. Residential IPs come from real consumer devices, are scarcer, and cost more. Mobile IPs sit behind carrier-grade NAT, which makes them very hard to block and the most expensive per gigabyte. Comparing a datacenter rate to a residential rate tells you nothing.

## What the cheapest option actually is at your volume

Here's the same comparison run at three monthly volumes, using publicly listed rates. The pattern that matters: the cheapest provider changes as your volume changes, and it changes by a wide margin.

| Monthly volume | Cheapest option | Effective $/GB | Notes |
| --- | --- | --- | --- |
| 5 GB | DataImpulse | $1.00 | $5 minimum buys 5 GB, no subscription |
| 50 GB | DataImpulse / Evomi | $1.00 | Evomi's entry plan is 100 GB, so it's a poor fit at 5 GB and fine here |
| 1 TB | Evomi | $0.32 | Rayobyte lands at $0.70; flat-rate vendors give no volume discount |

For context, at 5 GB month the same comparison puts Rayobyte at $3.50, Webshare at or below $3.50, Bright Data and Decodo at $4.00, IPRoyal around $5.50 and Oxylabs at $6.00. DataImpulse is the only sub-$2 option at that volume that doesn't force you into a large bundle.

Below roughly 50 GB a month, a flat $1/GB with a $5 floor beats every subscription on the market, because subscriptions charge you for a bundle you won't finish. Above 1 TB, that logic flips, and the flat-rate vendors lose to providers who discount on commitment.

Worth saying plainly: DataImpulse is not the cheapest thing you can buy at enterprise volume. If you're moving terabytes a month, negotiate.

## Cheap by type: datacenter, residential, mobile

Published breakdowns for 2026 put fair ranges at roughly $1–8/GB for residential, $0.50–3/GB for datacenter, and $2–15/GB for mobile. Anything at or near the bottom of those ranges is genuinely cheap; anything at the top is enterprise pricing for enterprise tooling.

Cheapest per gigabyte is datacenter, and it's not close. DataImpulse lists it at $0.50/GB with 99.9% claimed uptime, dropping to $0.45/GB at 1 TB. Datacenter IPs are the right call for high-volume work on sites that don't aggressively fingerprint server traffic — public databases, news archives, price comparison at scale, performance testing.

Residential is the middle tier and the one most people actually need. It costs more because the IPs come from real devices and clear the checks that kill datacenter traffic on e-commerce, SERP and social targets.

Mobile is the expensive one, and it's expensive for a real reason: carrier NAT means thousands of users share one IP, so blocking it means blocking legitimate customers. That resilience is why mobile runs $2 to $15 a GB. On the low end of that range, DataImpulse prices mobile at $2/GB — the same pay-as-you-go model as its residential traffic, with 1 TB dropping to $1.60/GB.

One quick sanity check on type: if you're paying residential rates to scrape a site that never blocks datacenter IPs, you're lighting money on fire. Route the easy targets through the $0.50 tier and keep the residential budget for the targets that need it.

## What a $1/GB provider looks like in practice

DataImpulse arrived in 2022, runs out of Cyprus, and made one bet: flat pay-as-you-go pricing with traffic that never expires.

The network is 90M+ ethically sourced IPs across 195 countries, with the residential side built from a first-party pool via its own app rather than resold third-party supply. The pricing that goes with it:

- Residential at **$1.00/GB**, flat, whether you buy 5 GB or 500 GB, with a $5 minimum. 1 TB drops to $0.80/GB.
- Datacenter at **$0.50/GB**, with 1 TB at $0.45/GB.
- Mobile at **$2.00/GB**, with 1 TB at $1.60/GB.
- Premium residential at **$5.00/GB** as an entry, scaling down to $50 for 10 GB.

Traffic doesn't expire. Buy 50 GB, burn 10 this week and 40 over the next six weeks, and nothing resets on the first of the month. There's no subscription and no monthly minimum beyond the $5 top-up. Protocol coverage is HTTP/HTTPS and SOCKS5, rotation is per-request by default, and sticky sessions can be held for up to 30 minutes.

👉 [Start with the $5 / 5 GB residential intro pack](https://bit.ly/dataimPulse)

Two things to know before you assume "everything included." Country-level targeting is in the base price. State, city, ZIP and ASN targeting are a paid add-on, and on residential plans third-party documentation puts that surcharge at double the standard per-GB rate. If your job needs city-level precision, budget $2/GB, not $1/GB.

On performance, the honest version is that the numbers come from two different places. DataImpulse publishes a 99.51% success rate. An independent editorial benchmark landed at 99.3%. Both are strong for the price point; neither is a substitute for testing on your own targets, because success rate is entirely target-dependent. The company also cites a 4.8/5 G2 score, which is its own published figure rather than something independently verified.

## All DataImpulse plans and prices

Every product currently listed, with the entry pack, the rate and the volume tier that changes it.

| Proxy type | Entry pack | Effective price | Volume tier | Billing | Buy |
| --- | --- | --- | --- | --- | --- |
| Residential | $5 / 5 GB | $1.00/GB | $800 / 1 TB ($0.80/GB) | Pay-as-you-go, traffic never expires | [Get the $5 residential pack](https://bit.ly/dataimPulse) |
| Premium residential | $5 / 1 GB | $5.00/GB (also $50 / 10 GB) | Custom pricing from $20,000 at 5 TB+ | Pay-as-you-go, no subscription | [Check premium residential rates](https://bit.ly/dataimPulse) |
| Mobile | $5 / 2.5 GB | $2.00/GB | $1,600 / 1 TB ($1.60/GB) | Pay-as-you-go, traffic never expires | [See mobile proxy pricing](https://bit.ly/dataimPulse) |
| Datacenter | $5 / 10 GB | $0.50/GB | $450 / 1 TB ($0.45/GB) | Pay-as-you-go, traffic never expires | [Buy the $5 datacenter pack](https://bit.ly/dataimPulse) |
| Enterprise / 5 TB+ | Custom quote | Negotiated | Datacenter from $2,250; mobile from $8,000 | Volume contract | [Request an enterprise quote](https://bit.ly/dataimPulse) |

A note on the premium tier, since the $5/GB number looks off next to the $1/GB standard rate. Premium residential is a different sub-pool with sub-50ms response targets, all targeting options at no surcharge, and a dedicated proxy manager. Most buyers don't need it. If standard residential is already clearing your targets, the premium tier is a 5× price increase for headroom you won't use.

## How to test a cheap proxy without wasting money

Nobody should take a per-GB rate on faith, including the $1 one. The right protocol is unglamorous and costs $5.

1. Buy the smallest pack available. At DataImpulse that's 5 GB of residential, 10 GB of datacenter or 2.5 GB of mobile for $5.
2. Run 100–500 requests against your real targets — not a proxy checker, not a generic HTTP endpoint. Your actual URLs, from your actual code.
3. Log four numbers: success rate, median latency, geo accuracy for the regions you care about, and bytes per successful request.
4. Divide your spend by successful requests. That's your real unit cost, and it's the only figure comparable across providers.

Two practical warnings. First, byte efficiency varies hugely by target: a lightweight API response and a JavaScript-rendered page can differ by an order of magnitude in transfer size, which means the same 5 GB pack covers wildly different workloads. Second, a provider that looks 4× cheaper per GB can be more expensive per successful request if its success rate is worse — which is exactly what the per-request calculation is for.

On refunds, DataImpulse's intro plans carry a 7-day money-back guarantee on card payments, provided less than 80% of the traffic has been consumed. Crypto purchases on intro plans are not refundable. There's no free trial at all — proxy access starts at the $5 minimum.

👉 [Open a DataImpulse account and run your own 500-request test](https://bit.ly/dataimPulse)

## Where "cheap" turns into a bad decision

Some cheap proxy options are cheap because they're not what you think they are.

**Free proxy lists.** Every public list is shared by thousands of users, often logged, and typically dead within days. They're the right tool for exactly one thing: seeing what a proxy error looks like.

**Cheap rates you can't actually buy.** The $2/GB headline on one major provider's page title doesn't appear as a plan row on that same page at all, which bottoms out at $2.75/GB. If a rate isn't selectable at checkout, it isn't your rate.

**Bundles bigger than your workload.** Buying 100 GB at a discount to use 20 GB a month only works if the balance rolls over. With expiring traffic, you're paying 5× the useful rate.

**Wrong tool for the target.** DataImpulse's own documentation is unusually direct about this: it isn't a static ISP reseller, isn't a fully managed scraping API, and isn't appropriate for banking or government sites. If you need any of those, a cheap rotating residential network is the wrong purchase no matter how low the per-GB figure goes.

**A free trial that auto-converts.** Worth checking the terms before entering a card. Some providers activate a paid plan automatically if you don't cancel before the trial ends.

## Picking by workload

If you spend under $50 a month, the short answer is flat-rate pay-as-you-go, and DataImpulse's $1/GB residential tier is the lowest legitimate entry cost on the market with a $5 floor and no subscription.

If your targets don't need residential legitimacy, drop to the datacenter tier at $0.50/GB and cut your bill in half for the same volume.

If your targets specifically fingerprint non-mobile traffic, mobile at $2/GB is where the money goes, and it's the cheapest published mobile rate among the major providers at low volume.

If you're consistently above 1 TB a month, stop reading consumer comparison tables and start negotiating. That's where Evomi's and Rayobyte's volume pricing beats every flat rate, DataImpulse's included.

### Does a cheap proxy service need a subscription?

No, and you shouldn't accept one unless the volume discount genuinely pays for it. Pay-as-you-go billing with non-expiring traffic is the more transparent model for any workload that fluctuates month to month.

### Does unused traffic expire?

With DataImpulse, no. Bytes you buy stay on your balance indefinitely. With several subscription-based providers, unused gigabytes disappear at the start of the next billing cycle — check this line before you compare rates.

### Are there DataImpulse coupon codes?

No public promo codes are listed, and the company's position is that none are needed, since $1/GB sits below most competitors' discounted rates. Coupon aggregators listing a code for this brand are worth treating with suspicion.

### Can I try it before paying?

Partially. There's no free tier or free trial, but testing costs $5 for the smallest pack, and intro plans bought by card carry a 7-day money-back guarantee if you've used under 80% of the traffic.

Cheap proxies are a solvable problem, just not by sorting a table of headline rates. Work out your monthly volume, decide whether your targets need residential IPs at all, check the minimum, check whether the balance expires, then buy the smallest pack that proves the number. $5 and 500 requests gets you further than an hour of comparison reading.
