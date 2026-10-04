# unmetered residential proxies: how pay-per-IP billing works, when it beats per-GB plans, and what to check before you buy

If you searched for unmetered residential proxies, the bill you're trying to avoid is probably already visible in your head: a per-GB provider, a scraping job whose page weight you don't control, and a monthly invoice that swings by hundreds of dollars depending on how heavy a target's JavaScript happens to be.

"Sold as unmetered" is where most buying mistakes start, because the word covers at least three different billing structures. Some of them are genuinely flat. Some have fair-use thresholds buried in a policy page. One of them doesn't meter traffic at all and instead meters how many exit IPs you hold. Knowing which one you're looking at changes both your cost per GB and the bottleneck you'll hit in month two.

## Three different things get called "unmetered"

| What the provider means | How it actually works | Typical examples |
| --- | --- | --- |
| No metering at all | Flat price, traffic isn't counted. The real ceiling is concurrency, threads or ports | ProxyScrape (residential and shared datacenter), IPRoyal ISP/datacenter |
| Unlimited under fair use | Published thresholds you can hit; overage is billed or throttled | Bright Data: 100 GB/month per ISP proxy, then pay-as-you-go rates. Decodo: FUP triggers at 10 TB per term or 25 GB per IP, concurrency drops. Oxylabs: 100 concurrent sessions for the first 50 GB, then 10. Webshare: unlimited only at 1,000 premium proxies |
| Unmetered *per IP* | Traffic never counts. You buy a number of IPs and use them as sessions | 9Proxy's IP-based packages |

The fair-use row is the one that catches people. A plan described as unlimited bandwidth can still have a monthly per-proxy ceiling that, once crossed, either bills you at pay-as-you-go rates or quietly cuts your session count for the rest of the month. That's not deception so much as a bandwidth policy living on a different page from the pricing table.

There's also a fourth thing that isn't unmetered at all: mobile proxies, where IPRoyal, for example, applies a 20–25 GB/day soft cap per connection. Worth flagging because "unlimited 4G" shows up in the same search results.

## Why bandwidth-based pricing gets expensive so fast

The arithmetic that pushes people toward unmetered plans is dull but decisive. Modern e-commerce and social pages routinely weigh 2–5 MB once you render them. A pipeline pulling 100,000 pages a month can burn through a meaningful chunk of a terabyte, and at mid-market residential rates that lands somewhere in the $1,500–$3,000 range monthly, as one recent integration guide puts it. Same job, same success rate, wildly different invoice.

Now flip it. Pay per IP instead, and the cost of that pipeline is fixed by how many IPs you need, not how much data moves through them. Scrape 100 pages through one IP or 10,000 through it, the price doesn't move. If your workload is bandwidth-heavy and your sessions are long rather than fast-rotating, that's the entire argument for this model.

## How the pay-per-IP side of 9Proxy works

9Proxy is a residential proxy network with 20M+ IPs across 90+ countries, HTTP/HTTPS and SOCKS5 support, and two separate pricing models that behave very differently. The IP-based model is the unmetered one.

A few specifics that matter more than the marketing line:

- **Traffic isn't counted while the IP is active.** You're paying for exit IPs, not for data.
- **Unused IPs don't expire.** They sit in your balance until you use them, which makes buying ahead of a spike a reasonable move rather than a gamble.
- **Individual IPs last a few hours to roughly 24 hours.** That's the nature of residential exit nodes, not a limitation specific to 9Proxy. You're buying a working session, not a permanent address.
- **It runs through the desktop app.** IP-based usage works via local port forwarding in 9Proxy's Proxy Program, with optional auto-rotation across selected ports at custom intervals. If you wanted a dashboard-only setup, that's the GB-based model instead.
- **Per-IP cost falls hard with volume.** The entry tier works out to $0.24 per IP; the 500,000-IP tier drops to about $0.018. When you see "from $0.015/IP" in advertising, that's the floor at maximum volume, not what a first purchase costs.

The other thing worth knowing: 9Proxy raised prices on IP-based and bundle packages on June 1, 2026, the first adjustment in the company's history. GB-based pricing was left untouched. If you're comparing against older reviews and roundups, some of them still list the previous rates, like $20 for 100 IPs. The current numbers are below.

## Every current 9Proxy package

### IP-based packages (unmetered bandwidth per IP)

| Package | What you get | Price | Billing | Purchase |
| --- | --- | --- | --- | --- |
| 100 IPs | 100 residential IPs, unmetered traffic | $24 ($0.24/IP) | One-off, balance-based | [Check the 100-IP package](https://bit.ly/9-Proxy) |
| 500 IPs | 500 residential IPs, unmetered traffic | $72 ($0.144/IP) | One-off, balance-based | [Check the 500-IP package](https://bit.ly/9-Proxy) |
| 1,000 IPs + 500 bonus | 1,500 IPs total, unmetered traffic | $126 ($0.084/IP) | One-off, balance-based | [Check the 1,000 + 500 IP package](https://bit.ly/9-Proxy) |
| 2,500 IPs | 2,500 residential IPs | $210 ($0.084/IP) | One-off, balance-based | [Check the 2,500-IP package](https://bit.ly/9-Proxy) |
| 5,000 IPs | 5,000 residential IPs | $360 ($0.072/IP) | One-off, balance-based | [Check the 5,000-IP package](https://bit.ly/9-Proxy) |
| 15,000 IPs | 15,000 residential IPs | $720 ($0.048/IP) | One-off, balance-based | [Check the 15,000-IP package](https://bit.ly/9-Proxy) |
| 25,000 IPs | 25,000 residential IPs | $863 ($0.035/IP) | One-off, balance-based | [Check the 25,000-IP package](https://bit.ly/9-Proxy) |
| 50,000 IPs | 50,000 residential IPs | $1,438 ($0.029/IP) | One-off, balance-based | [Check the 50,000-IP package](https://bit.ly/9-Proxy) |
| Business 100,000 IPs | High-volume residential pool | $2,300 ($0.023/IP) | One-off, balance-based | [Check the Business 100,000-IP package](https://bit.ly/9-Proxy) |
| Business 200,000 IPs | High-volume residential pool | $4,140 ($0.021/IP) | One-off, balance-based | [Check the Business 200,000-IP package](https://bit.ly/9-Proxy) |
| Business 500,000 IPs | High-volume residential pool | $8,625 ($0.018/IP) | One-off, balance-based | [Check the Business 500,000-IP package](https://bit.ly/9-Proxy) |

### Bundle packages (IPs plus bandwidth)

| Package | What you get | Price | Validity | Purchase |
| --- | --- | --- | --- | --- |
| Starter bundle | 100 IPs + 5 GB | $30 | Traffic valid 180 days | [Check the Starter bundle](https://bit.ly/9-Proxy) |
| Popular bundle | 1,500 IPs + 50 GB | $180 | Traffic valid 180 days | [Check the Popular bundle](https://bit.ly/9-Proxy) |
| Pro bundle | 5,000 IPs + 500 GB | $720 | Traffic valid 180 days | [Check the Pro bundle](https://bit.ly/9-Proxy) |

### GB-based packages (rotating endpoints, metered traffic)

| Package | Rate | Price | Billing | Purchase |
| --- | --- | --- | --- | --- |
| 5 GB | $3.00/GB | $15 | One-off, 180-day validity | [Check the 5 GB package](https://bit.ly/9-Proxy) |
| 50 GB + 5 GB | $2.10/GB | $105 | One-off, 180-day validity | [Check the 50 GB package](https://bit.ly/9-Proxy) |
| 100 GB | $1.50/GB | $150 | One-off, 180-day validity | [Check the 100 GB package](https://bit.ly/9-Proxy) |
| 200 GB | $1.00/GB | $200 | One-off, 180-day validity | [Check the 200 GB package](https://bit.ly/9-Proxy) |
| 1,000 GB | $0.80/GB | $800 | One-off, 180-day validity | [Check the 1,000 GB package](https://bit.ly/9-Proxy) |
| 2,000 GB | $0.75/GB | $1,500 | One-off, 180-day validity | [Check the 2,000 GB package](https://bit.ly/9-Proxy) |
| Enterprise 3,000 GB | $0.72/GB | $2,160 | Unlimited validity | [Check the Enterprise 3,000 GB package](https://bit.ly/9-Proxy) |
| Enterprise 6,000 GB | $0.70/GB | $4,200 | Unlimited validity | [Check the Enterprise 6,000 GB package](https://bit.ly/9-Proxy) |
| Enterprise 10,000 GB | $0.68/GB | Enterprise pricing | Unlimited validity | [Check the Enterprise 10,000 GB package](https://bit.ly/9-Proxy) |

Enterprise also brings team features: one owner plus up to five members, no-expiration bandwidth sharing inside the team, per-member traffic controls, and activity logs. If you're an agency reselling capacity to clients, that last part is more useful than another 10% off GB pricing.

## The math, with the assumptions stated out loud

Say you buy 100 IPs for $24 and each one carries 40 GB before it rotates out. That's 4,000 GB of traffic for $24. On 9Proxy's own GB-based pricing, the closest tier to 4,000 GB would run into the low thousands of dollars. Same provider, same IP pool, roughly a hundredfold difference — because one model charges for IPs and the other charges for data.

Flip the assumptions and the conclusion flips with them. If each IP only carries 300 MB of lightweight API polling before rotating, 100 IPs give you 30 GB. Buying 50 GB of GB-based credit for $105 and rotating freely through the full pool is both cheaper and simpler than renting exit IPs you barely touch. Unmetered only wins when your workload actually moves data.

## Which 9Proxy model fits which workload

**Pick IP-based when:** you're running long sessions against tricky targets, doing account-based work that needs a stable exit, or pulling page-heavy content where per-GB pricing is unpredictable. Bandwidth stops being a line item.

**Pick GB-based when:** you need a fresh IP per request, wide geographic spread, or light payloads at high request counts. It also works entirely from the dashboard with username/password or IP whitelisting, no desktop app involved, and gives you unlimited endpoints with targeting down to country, state, city, ZIP and ISP level.

**Pick a bundle when:** some of your jobs need stable IPs and others just need rotation. The 180-day traffic validity means the unmetered half doesn't get wasted while you're not using it.

**Pick Enterprise when:** you're running continuous infrastructure or need the traffic to never expire.

One practical note on the IP-based side: the Today List feature lets you reuse IPs from the previous 24 hours without paying for them again, which a partner integration guide estimates at a 20–30% saving on IP spend. Automatic refresh also swaps out offline IPs within about 60 seconds, so a dead exit node doesn't stall a queue overnight.

## Setting up, in the order you'll actually do it

1. Create an account and choose a package. Buying happens through the balance system, so nothing recurs unless you buy again. 👉 [Start with a 9Proxy account and pick a package](https://bit.ly/9-Proxy)
2. Choose your access route. Proxy Program is the Windows client that routes at the OS layer, which is the practical option for software with no proxy settings of its own. Proxy2Web is browser-based with plain user:pass credentials for quick geo-checks. ProxyHub handles mobile device management, and the public API is the route for pipelines you want to control from code.
3. Configure rotation. On IP-based plans you set rotation intervals on selected ports. On GB plans you choose sticky sessions of a fixed duration or a fresh IP per request.
4. Plug it into your stack. SOCKS5 support means anti-detect browsers, proxychains and custom Python scripts connect without protocol gymnastics.

If you'd rather test the pool before committing, 9Proxy runs a limited new-user trial depending on availability — the vendor has described it as 10 free IPs.

## What to check before you commit

- **GB credit expires in 180 days.** Enterprise is the exception, with unlimited validity. If you buy 1,000 GB for a project that gets deprioritised for six months, that's a real risk.
- **Residential IPs are not permanent.** A few hours to about 24 hours is the normal lifespan. Anything needing a fixed address for weeks belongs in the static ISP category, not here.
- **20M+ IPs across 90 countries is mid-tier.** Enterprise networks advertise 100M+ across 195+. If your targets are in a specific city or on a specific ISP in a small market, verify coverage rather than assuming it.
- **Benchmarks are mixed.** ProxyLook's directory puts 9Proxy at roughly 97% success rate and 1,300 ms average response, with a 3.9/5 rating. A budget-tier comparison places providers in this price bracket at 99%+ on tier-1 targets, 90–95% on tier-2, and 70–85% on tier-3. Reasonable for the price; not the success rates you'd get paying four times as much.
- **Support is human and 24/7** via Telegram, email and tickets, but there's no dedicated account manager until the enterprise tiers.

## Quick answers

**Is unmetered the same as unlimited speed?** No. Unmetered means traffic isn't counted. Throughput still depends on the exit node's connection and your concurrency. Some providers sell speed tiers explicitly for this reason; 9Proxy's constraint is that your IP-based sessions burn through exit nodes as they go offline naturally.

**Do unused IPs expire?** Per 9Proxy's own documentation, no. Unused IPs stay in your balance until you consume them. GB credit is a different story: 180 days, or unlimited on Enterprise.

**Do I need to install anything?** Only for IP-based plans. GB-based proxies run straight from the dashboard.

**Can I mix both models?** Yes, and that's what the bundle packages are for. A single account holds IP balance and traffic balance side by side.

**Is there a free tier?** Not a permanent one. 9Proxy's pricing page offers account creation without a card, and a limited trial on request, described by the vendor as 10 free IPs.

## The short version

Unmetered residential proxies solve a specific problem: a bandwidth bill that scales with something you can't forecast. If that's your problem, 9Proxy's IP-based model answers it directly — $24 for 100 IPs with traffic that never gets counted, dropping to $0.018 per IP at the highest volume, with unused IPs that don't rot in your account. If your workload is light per request and needs constant rotation, the unmetered pitch isn't for you, and a GB package will cost less. 👉 [Compare the plans and pick the model that matches your traffic](https://bit.ly/9-Proxy)
