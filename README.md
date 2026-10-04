# 9proxy vs smartproxy: pay-per-IP or pay-per-GB, and which one actually fits your workload

If you ended up here, you probably did what most people do with a proxy budget: opened a spreadsheet, put these two vendors side by side, and then noticed the columns don't talk to each other. One bills per IP address. The other bills per gigabyte. There is no exchange rate between those two units, which is exactly why this comparison feels harder than it should.

One naming problem first, because it trips people up in search results and in old tutorials. **Smartproxy no longer trades under that name.** The company rebranded to Decodo on 22 April 2025, keeping the same company, infrastructure, accounts, subscriptions and backward-compatible endpoints [5]. So everything below about "Smartproxy" is really about Decodo, and if a tutorial points you at a `smartproxy.com` endpoint that still resolves, that's why.

## What each one actually is

9Proxy is a residential-only network: 20M+ IPs across 90+ countries, with two separate billing models rather than a single product with add-ons. You either buy a pool of residential IPs with unlimited traffic, or you buy bandwidth and generate as many endpoints as you like. There's also a desktop app involved in the per-IP model, which matters more than it sounds like it should [6].

Decodo is the broader catalogue. Residential is still the flagship, but it sits next to mobile, static residential (ISP), datacenter, a Site Unblocker and a Web Scraping API, all billed in different units [3]. Its residential network is advertised at 115M+ IPs across 195+ locations, with a third-party benchmark putting it at roughly 115 million IPs as of May 2026 [12].

If you need three proxy types under one invoice and one support queue, that breadth is the whole argument for Decodo. If you only need residential and you care about what a gigabyte costs you, keep reading, because that's where the two split hard.

## The units are the actual decision

Start with the two models side by side, because the pricing tables only make sense once you know which one you're in.

**9Proxy, per-IP:** you buy a fixed number of residential IPs. Each IP stays usable from a few hours up to about 24 hours, and traffic through it is unmetered during that window. One forwarded IP equals one use [6]. Unused IPs don't expire, so a 2,500-IP balance can be drawn down over months.

**9Proxy, per-GB:** you buy traffic, and endpoints are unlimited. Rotation can be per request or sticky, and nothing needs to be installed locally, since generation runs from the dashboard [6].

**Decodo, per-GB subscription:** you buy a monthly bandwidth tier. Residential is pay-as-you-go at $4/GB, with subscription tiers shaving the rate down as the commitment grows. Unused bandwidth expires with the billing cycle [3][4].

Put a number on it. Say you push 100GB a month. On 9Proxy's GB model that's the 100GB package at **$1.50/GB, or $150**, valid for 180 days [7][11]. On Decodo it's the 100GB tier at **$2.75/GB, so $275**, plus VAT, expiring at the end of the month [3][4]. Same traffic, 45% less on paper, and the unused portion doesn't evaporate after 30 days.

Now change the job. Say you're running 100 separate browser profiles that each need a clean residential address, and the traffic per profile is light but constant. 9Proxy's 100-IP package costs **$24**, and you're not paying per gigabyte at all [2][7]. That's a shape of workload Decodo's per-GB model cannot price competitively, because every megabyte of it is billed.

The reverse also holds. If you're scraping a few million small requests from a target that needs a huge, constantly rotating pool, buying IPs at $0.084 each is the wrong meter. You want bandwidth and rotation, and Decodo's network size and ASN-level targeting start to matter more than the per-GB delta.

## 9Proxy pricing, all of it

Announced on 18 May 2026 and effective from 1 June 2026, 9Proxy raised prices on its IP-based and bundle packages for the first time. Its GB-based residential rates were left untouched by that update [1].

**Residential proxies by IP** (unlimited traffic per IP, unused IPs don't expire):

| Package | Effective rate per IP | Total | Buy |
| --- | --- | --- | --- |
| 100 IPs | $0.24 | $24 | Grab the 100-IP starter package |
| 500 IPs | $0.144 | $72 | Get the 500-IP package |
| 1,000 + 500 bonus IPs | $0.084 | $126 | Buy the 1,000 IP package with 500 bonus IPs |
| 2,500 IPs | $0.084 | $210 | Check the 2,500-IP package |
| 5,000 IPs | $0.072 | $360 | See the 5,000-IP package |
| 15,000 IPs | $0.048 | $720 | Open the 15,000-IP package |
| 25,000 IPs | $0.035 | $863 | Compare the 25,000-IP package |
| 50,000 IPs | $0.029 | $1,438 | View the 50,000-IP package |
| 100,000 IPs | $0.023 | $2,300 | Open the 100,000-IP business package |
| 200,000 IPs | $0.021 | $4,140 | Check the 200,000-IP business package |
| 500,000 IPs | $0.018 | $8,625 | See the 500,000-IP business package |

**Residential proxies by GB** (unlimited endpoints, 180-day validity):

| Package | Rate per GB | Total | Buy |
| --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | Try the 5GB bandwidth package |
| 50 + 5 bonus GB | $2.10 | $105 | Get the 50GB package with 5 bonus GB |
| 100 GB | $1.50 | $150 | Buy the 100GB package |
| 200 GB | $1.00 | $200 | Check the 200GB package |
| 1,000 GB | $0.80 | $800 | Open the 1,000GB package |
| 2,000 GB | $0.75 | $1,500 | View the 2,000GB package |

**Enterprise bandwidth** (unlimited validity, team access per 9Proxy's docs):

| Package | Rate per GB | Total | Buy |
| --- | --- | --- | --- |
| 3,000 GB | $0.72 | $2,160 | Ask about the 3,000GB enterprise package |
| 6,000 GB | $0.70 | $4,200 | See the 6,000GB enterprise package |
| 10,000 GB | $0.68 | $6,800 | Check the 10,000GB enterprise package |

**Bundle packages** (IPs plus traffic in one purchase, 180-day validity on the bandwidth):

| Bundle | Contents | Total | Buy |
| --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | Get the Starter bundle |
| Popular | 1,500 IPs + 50 GB | $180 | Buy the Popular bundle |
| Pro | 5,000 IPs + 500 GB | $720 | See the Pro bundle |

Two small things that don't show up in a pricing column: 9Proxy's partner terms list up to 15% affiliate commission and a **5% discount for users who arrive through a referral link**, which is how the sign-up link in this article works. And Caproxy's review notes a 60-second credit-back policy — if an IP fails inside the first minute after activation, the credit returns to your balance, plus a "Today List" that lets you reuse proxies touched in the last 24 hours at no extra cost [11]. Those are worth checking against the current terms before you rely on them.

## Decodo pricing, for a fair look

Decodo's residential side is a monthly bandwidth ladder, and the advertised "from $2/GB" figure sits at the top of it rather than at the bottom. The 1,000GB monthly tier is what hits $2/GB. What a first-time buyer actually clicks is $3.75/GB on the smallest plan [3][4].

| Residential tier | Rate per GB | Monthly cost |
| --- | --- | --- |
| Pay as you go | $4.00 | per-GB spend, no commitment |
| 3 GB | $3.75 | $11.25 |
| 10 GB | $3.50 | $35 |
| 25 GB | $3.25 | ~$81 |
| 50 GB | $3.00 | $150 |
| 100 GB | $2.75 | $275 |
| 1,000 GB | $2.00 | $2,000 |
| Enterprise | from $2.00 | custom |

Every listed figure is quoted before VAT, so EU buyers should add tax. Other Decodo products, for context: static residential from $0.27/IP advertised (the cheapest purchasable dedicated tier is several times higher), mobile from $2.25/GB, datacenter from $0.020/IP, Site Unblocker from $0.95 per 1,000 requests, and a Web Scraping API from $0.09 per 1,000 requests with a genuinely free tier of 2,000 standard requests [3][8].

## Head to head

|  | 9Proxy | Decodo (formerly Smartproxy) |
| --- | --- | --- |
| Billing model | Per IP with unlimited traffic, or per GB | Per GB, monthly subscription or PAYG |
| Residential pool | 20M+ IPs, 90+ countries | 115M+ IPs, 195+ locations |
| Entry price | $24 for 100 IPs / $15 for 5GB | $11.25 for 3GB, or $4/GB PAYG |
| 100GB of traffic | $150 | $275 + VAT |
| Traffic expiry | 180 days, or never on per-IP and Enterprise | Expires with the monthly cycle |
| Targeting | Country, state, city, ZIP, ISP | Country, state, city, ZIP, ASN |
| Session length | Rotating or configurable sticky; IPs live hours to ~24h | Default 10-minute sticky, custom up to 24 hours |
| Protocols | HTTP/HTTPS, SOCKS5 | HTTP/HTTPS, SOCKS5 with UDP |
| Setup | Dashboard for per-GB; desktop app required for per-IP | Dashboard and API only |
| Free trial | Limited trials for new users, subject to availability | 3 days / 100MB, card required |
| Refunds | 60-second credit-back on failed IPs (per third-party review) | 14-day money-back, first purchase, under 20% used |
| Other products | Residential only | Mobile, ISP, datacenter, scraping API, unblocker |

The pool gap is real and worth being honest about: 115M+ across 195+ locations is a bigger, wider network than 20M+ across 90+. Independent benchmarking also puts Decodo's residential success rate at 99.86% with a 0.63-second average response, and rates its IP pool as the least abused tested, with a fraud score of 32.72 against a 45.57 market average [12]. For targets that fingerprint aggressively, those numbers are the ones that decide whether your run finishes.

9Proxy's own claims are 99.95% uptime across 8,000+ servers, and one third-party write-up reports roughly 99.5% success and about 0.6 seconds average response in its own testing [11]. Treat that as one reviewer's result, not a benchmark.

## Where each one wins

**9Proxy wins on cost per gigabyte above roughly 50GB a month, and on anything IP-bound.** At 100GB you're paying $1.50/GB against $2.75/GB, and your bandwidth doesn't die at the end of the billing cycle. If your real constraint is "how many separate clean identities can I hold," per-IP with unlimited traffic is a fundamentally cheaper structure than metering every request.

**Decodo wins on pool breadth, target granularity and the rest of the stack.** ASN targeting, SOCKS5 with UDP, 195+ locations and a scraping API on the same invoice are things 9Proxy simply doesn't sell. If your work involves mobile proxies or a datacenter tier alongside residential, Decodo is one vendor instead of two.

The honest awkwardness is the per-IP model's learning curve. Because per-IP proxies run through a desktop app doing local port forwarding, and because each IP burns once forwarded, you need to think about session planning rather than just pointing a script at a gateway. Caproxy's review puts it bluntly, flagging 9Proxy as not beginner-friendly [11]. The per-GB side has no such problem; it lives entirely in the dashboard, with username/password or IP whitelisting and country down to ISP-level targeting [6].

## Trials, refunds and the fine print

Decodo's trial runs 3 days with 100MB, needs a card, and auto-activates the plan when it ends unless you cancel. Taking the free trial also disqualifies you from the 14-day money-back option — the two are mutually exclusive, and the refund only covers a first purchase with under 20% of traffic used [3][4]. Worth knowing before you click, since 100MB proves your integration works but tells you almost nothing about whether the IPs survive a real target.

9Proxy's official partner posts say limited new-user trials exist depending on availability, and you have to specify whether you want to test the per-IP or the per-GB model. There's no standing free tier. Practical approach: if you mainly want to check whether residential IPs get through your target, start with the 5GB bandwidth package at $15 or the 100-IP package at $24 rather than waiting on trial stock.

## Which one, by situation

- **Solo scraping a handful of targets at 50–200GB a month:** 9Proxy, on the GB model. The 100GB package at $150 with 180-day validity wastes less.
- **Managing dozens to thousands of accounts or browser profiles with light traffic each:** 9Proxy's per-IP packages. Unlimited traffic per IP is the cheapest structure for that shape of work.
- **Heavy rotation against hard targets, plus mobile or datacenter in the same stack:** Decodo. Bigger pool, wider targeting, one invoice.
- **You need to test on a small budget with a guaranteed refund path:** Decodo's trial covers the connectivity check; the 3GB plan covers the real test with the refund window intact.
- **You're already deep into one ecosystem's tooling:** stay. The switching cost for API integration is real, and neither vendor is so much cheaper that it pays for a rewrite.

If you want to run the 9Proxy numbers against your own traffic profile, 👉 sign up through this link and the packages above stay visible in your account after purchase.

## Quick answers

**Is Smartproxy still active?**
Yes, under the name Decodo since April 2025. Same company, same infrastructure and subscriptions, with legacy endpoints still supported [5].

**Which is cheaper for 100GB of residential traffic?**
9Proxy at $150 versus Decodo at $275 plus VAT. Both figures come from published tiers, not quotes [3][4][7].

**Does 9Proxy have a monthly minimum?**
No. Both its IP and GB packages are one-off balance purchases, and unused IPs don't expire [6].

**Is 9Proxy's per-IP "unlimited" really unlimited?**
Unlimited traffic during an IP's active life, which runs from a few hours to about 24 hours. One forwarded IP is one use, so you're buying sessions, not permanent addresses [6].

**Which handles failures better?**
Decodo publishes a 14-day money-back guarantee with conditions. 9Proxy's documented mechanism is narrower: a 60-second credit-back on IPs that fail immediately after activation [11]. Different scopes, read both before committing volume.

## Bottom line

These two aren't competing for the same line in your budget. Decodo is a bandwidth-metered platform with the bigger pool and the wider product catalogue, and the price you pay for that breadth is $2.75 to $4.00 per gigabyte at the volumes most people actually buy. 9Proxy sells the other meter: unlimited traffic per IP, or bandwidth that starts at $3.00/GB and drops to $0.68/GB in the same table, with 180 days to use it.

Pick by what your workload burns. If it burns gigabytes, run the numbers above and 9Proxy usually comes out ahead from about 50GB a month. If it needs hundreds of separate identities with barely any traffic each, per-IP stops being a pricing style and starts being the only model that makes sense.
