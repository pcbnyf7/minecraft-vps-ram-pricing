# Best VPS for Minecraft: How much RAM you need, what 32 GB costs at three providers, and the renewal price nobody quotes

A server for ten friends running vanilla or Paper fits comfortably in 4 GB of RAM. Add a modpack and 8 GB is the realistic floor. Apex Hosting's own guidance backs the second number up: 6 GB for Java and 4 GB for Bedrock, sized for about 20 concurrent players.

Below you'll find the sizing rules, what the same RAM tier costs across four hosting companies, the gap between the advertised price and the renewal price, and the hardware that makes no difference to Minecraft at all. RackNerd's self-managed KVM VPS line, which is what most small servers should be shopping in, starts at $26.99/year for the 512 MB tier and scales up to 12 GB of RAM and 7 vCPU.

> **Most readers:** a 4 GB KVM VPS with full root access, Paper installed, whitelist on. That handles roughly 10 players with light plugins, and you skip the game-panel markup entirely.
> 👉 [See RackNerd's current KVM VPS plans and pricing](https://bit.ly/RacKnerd)

## RackNerd KVM VPS plans

RackNerd sells through rotating "VPS specials," so the tiers in the middle of the range change with each promotion. Two points on the ladder are published: the entry plan and the top of the standard range.

| Plan | RAM / vCPU | Storage / Transfer | Price & billing | Order |
| --- | --- | --- | --- | --- |
| Entry KVM VPS | 512 MB / 1 vCPU | 30 GB RAID-10 SSD / 500 GB | $26.99/year | [Order the entry plan](https://bit.ly/RacKnerd) |
| Top of standard range | 12 GB / 7 vCPU | 300 GB SSD-cached / 6 TB | Shown at checkout | [Check the current 12 GB price](https://bit.ly/RacKnerd) |

Every plan in the line is KVM with full root SSH access, a 1 Gbps port, one dedicated IPv4, and RackNerd's own `ctrl` panel for reboots, OS reinstalls, an HTML5 VNC console, one-click app installs and inbound firewall rules. You pick CentOS, Rocky Linux, AlmaLinux, Fedora, Debian or Ubuntu at checkout, and custom ISOs are available by ticket. RackNerd runs these out of Los Angeles, San Jose, Seattle, Dallas, Atlanta, Chicago, New York, Ashburn, Amsterdam, France and Dublin, which matters more than any spec sheet for a game server: pick the location closest to your players.

## How much RAM does your Minecraft server actually need?

Sizing tables from server calculators and from hosts don't agree exactly, so treat any figure as a floor rather than a ceiling:

| Players | RAM | What's running |
| --- | --- | --- |
| 1–5 | 1–2 GB | Vanilla |
| 5–15 | 2–4 GB | Light plugins such as Essentials |
| 15–30 | 4–6 GB | Heavier modpacks (Forge, All The Mods) |
| 30+ | 6–8 GB+ | Full modded servers |

The pattern behind those numbers is simple. Vanilla and Paper are frugal. Modpacks are not, because each mod carries its own world-gen and entity load. A Pixelmon or All The Mods server with six regulars can want more memory than a 25-player vanilla server.

Host guidance skews generous. Apex recommends 6 GB on Java for 20 concurrent players, while BisectHosting suggests 4 GB covers 6 players and most calculators say the same 4 GB handles 10. The spread comes from how each one weighs plugins and view distance. If you're between two tiers, buy the smaller one and watch your server's memory graph for a week; upgrading a VPS later is a reboot and an invoice, not a migration project.

## Java or Bedrock changes what you install

Decide this before you order anything. Java Edition runs on Windows, macOS and Linux only, and it's the edition with the server-side ecosystem: Paper, Spigot, Purpur, Forge, Fabric, plus the plugin and modpack libraries. Bedrock covers Windows, Xbox, PlayStation, Switch, iOS and Android, and needs less memory for the same headcount, which is why Apex quotes 4 GB rather than 6 GB for 20 players.

A Linux VPS handles either, but what you install, how you back it up and which plugins exist all differ. Mixed friend groups usually end up running both, and a VPS with root access is one of the few places you can do that on a single bill.

## What "self-managed" means in practice

RackNerd's VPS specials are explicitly unmanaged. You get root and a control panel, not a game panel with a one-click Minecraft button. The work you're taking on:

- Installing Java and the server jar (Paper for performance, Forge or Fabric for modpacks), then keeping it updated
- Writing a start script and keeping the process alive after a reboot
- Backups. Nobody does these for you on an unmanaged VPS, and a corrupted world with no snapshot is the most common way small servers die
- Firewall rules and fail2ban, or at least a whitelist so strangers don't find your port

In exchange you get to run whatever you want on the box. A Discord bot, a small website, a Valheim server for the off-season, a VPN. Per-slot pricing disappears too: ten friends and forty friends cost the same.

Setup is quick. RackNerd provisions right after payment, usually within 5 to 15 minutes, and `ctrl` gives you a browser console if you lock yourself out of SSH. Support is 24/7, and RackNerd's own ordering guide claims an average first response under 10 minutes. On a $27/year box, that's the realistic ceiling of what you should expect from anyone.

👉 [Compare RackNerd's KVM VPS plans and pick a datacenter](https://bit.ly/RacKnerd)

## Same 32 GB, three very different monthly prices

Once you move up to game-panel hosting, price stops tracking specs. All three of these give you 32 GB of RAM:

| Provider & plan | RAM / vCPU | Effective monthly | How you pay |
| --- | --- | --- | --- |
| Hostinger Game Panel 8 | 32 GB / 8 vCPU | $27.99 | $671.76 upfront for 24 months; renews at $49.99/mo |
| BisectHosting 32 GB | 32 GB | $76.80 | $921.60 billed annually |
| Apex Hosting 32 GB | 32 GB | $104 | Monthly, or $280.77 per quarter |

Hostinger's figure only exists if you prepay two years, and it runs on AMD EPYC with NVMe storage, DDoS protection and a panel covering 2,000+ modpacks. BisectHosting charges nearly three times as much per month and includes 21 datacenters, daily backups and a 2,300-modpack library. Apex sits at the top on price with monthly billing and no annual discount, which is the trade you make for flexibility.

What you're paying for in that spread is the panel: automated backups, modpack installers, support that will fix a broken Forge install for you. What you give up is root access, and with it the ability to run anything that isn't Minecraft.

## The renewal price is the number that matters

Hostinger's Game Panel 1 lists at $6.99/mo on a 24-month term, which comes to $167.76 paid today. The same plan renews at $11.99/mo for the next term, or $287.76. Game Panel 8 goes from $671.76 for two years to $1,199.76 on renewal, a 79% jump. Apex's entry plan runs $3 for the first month and $4/mo after, so the discount there is one dollar.

Run the arithmetic before you commit:

| Plan | First term | Renewal term | Difference |
| --- | --- | --- | --- |
| Hostinger GP1 (24 mo) | $167.76 | $287.76 | +$120 |
| Hostinger GP8 (24 mo) | $671.76 | $1,199.76 | +$528 |
| Apex entry (monthly) | $3 first month, then $4/mo | $4/mo | +$1 in month one |

A "from $6.99/mo" headline that turns into $11.99 in year three is still a fine deal if the panel saves you an hour a month. It's a bad deal if you budgeted for the headline. BisectHosting doesn't raise its rate on renewal, which is worth something on a server you plan to keep for years.

## Hardware you don't need for Minecraft

The dedicated-server threads on r/VPS are full of people building for a 200-player Towny server, and the numbers there are useful mainly as a ceiling. One operator running a large multithreaded Towny/Civ setup wanted a Ryzen 9 9950X, 64 GB DDR5, 1 TB of storage and a 10 Gbps port for $200–250/mo. Replies pointed out that a 7950X3D is only about 4% faster than a 7950X in benchmarks, that 3D V-Cache does nothing for Minecraft, and that a 7950X dedicated box runs around $130/mo at Hetzner in Finland or Germany, around $150/mo at Server4You in the US. Advinservers sells a 9950X with 128 GB DDR5 and 4 TB of NVMe for $179.99/mo.

That's the right conversation for a community of several hundred. For ten to thirty players it's money burned on idle cores. A 4 GB or 8 GB KVM VPS at a fraction of those prices will hold 60 tick with a sane view distance and a pregenerated world. Spend the difference on a second VPS for backups instead.

## Before you pay

- **Edition and software.** Paper for performance on Java, Forge or Fabric for modpacks, and confirm the version your friends actually play matches.
- **Root access.** Without it you can't switch server jars, install plugins from source, or fix a broken config yourself.
- **Backups.** On an unmanaged VPS this is your job. A weekly rsync to another box or a storage bucket costs almost nothing.
- **DDoS protection.** Ask before you buy. RackNerd's `ctrl` panel includes inbound firewall rules, which is not the same thing as network-level mitigation, and any host's policy is worth confirming in writing for a public server.
- **Location.** Pick the datacenter nearest your players. Dublin for Europe, Dallas or Ashburn for the US east, Los Angeles for the west coast and Asia.
- **Billing term and renewal price.** Note both, in writing, before checkout.

👉 [Start with RackNerd's VPS specials and confirm the current per-plan pricing](https://bit.ly/RacKnerd)

## Which one should you buy?

- **Two to ten friends, vanilla or Paper:** the 2–4 GB tier. Anything larger is idle memory.
- **Around 20 players with plugins, or a mid-size modpack:** 8 GB, and pregenerate your world before opening it up.
- **A public server past 50 players with heavy mods:** 16 GB, and at that point compare a game panel's backups and support against the hours you'd spend administering a VPS yourself.
- **Anything at 32 GB or a dedicated box:** only if you're running multiple servers or a large multithreaded setup. A single Minecraft world won't use it.

Two things to confirm at checkout: the billing term you're actually signing, since annual pricing is where the low monthly figures come from, and the datacenter, because a fast server on the wrong continent plays worse than a slow one next door.

👉 [Pick a RackNerd KVM VPS plan and choose your datacenter](https://bit.ly/RacKnerd)
