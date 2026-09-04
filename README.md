<div align="center">

# AWP NETWORK

**A complete Counter-Strike 2 AWP server network — for sale.**

Four running servers · 19 first-party plugins · a full community website · one database.

### → [gonlyxx.github.io/awp-network](https://gonlyxx.github.io/awp-network/)

**Contact on Discord: `gon.lyxx`**

</div>

---

## What this is

AWP NETWORK is a turnkey Counter-Strike 2 AWP server network. Not a plugin pack, not
a folder of scripts — the whole thing, built as one system and handed over so you can
run it under your own brand.

This repository is just the public landing page. **The platform source is private.**
To see it running and get a quote, add **`gon.lyxx`** on Discord.

## The four servers

| # | Server | Map |
|---|---|---|
| AWP 1 | **LEGO** | the classic block map — the network's home |
| AWP 2 | **LEGO CS:GO** | the CS:GO-era LEGO layout |
| AWP 3 | **MINECRAFT** | blocky Minecraft-styled arena |
| AWP 4 | **SHOOTOUT** | tight, fast aim-duel map |

All four run the same plugin suite and share **one** database, economy, rank ladder
and skinchanger — a player's progress follows them across every server. Maps load as
signed Steam Workshop addons (MultiAddonManager). Servers auto-update the CS2 build on
launch, hibernate when empty, and the whole set fits on an **8 GB** box.

## What's in the box

**19 first-party CounterStrikeSharp plugins (.NET 10)**

- **Gameplay** — AWP-only ruleset, round flow, spawn protection, team balance, bots +
  anti-AFK, 1v1 spotlight, special rounds (low-grav / deagle / one-HP / knives / …),
  custom victory messages, team names & logos
- **Progression** — XP, configurable rank tiers, prestige, achievements, level
  rewards, per-map stats, in-scoreboard rank tag, XP anti-abuse
- **Economy** — single-writer credit balance, append-only idempotent ledger,
  trick-shot bonuses, a clean one-line kill feed, per-round point summary, `!pay`
- **Killstreak · VIP · Movement/BHOP · Maps/RTV · Chat tags · Menu + Discord relay**
- **Effects** — beam movement trails, kill / spawn / MVP effects
- **Skinchanger** — server-side weapon finishes, knives, gloves, agents, music kits,
  a 10-slot medal showcase (VAC-safe — no client files touched)
- **Admin** — reports, player flags, ban/mute v2
- **Web-admin bridge** — the site drives the servers through a signed queue, not RCON
- **Anti-cheat** — first-party server-side heuristics (spinbot / aim-snap / reaction /
  HS-streak) that raise review flags; complements VAC, never replaces it
- **Owner assist tools** — owner-only, backend-validated, audit-logged
- plus the shared library, the SDK/contracts, and licence-gated Cosmetics & Licensing
  modules (in the source, not deployed on the reference network)

**A full Next.js 14 community website**

Live server status, the web skinchanger, metric leaderboards, daily/weekly missions,
achievements, a points shop, VIP/Premium, rich player profiles, real Steam OpenID
sign-in, and an admin panel with role-based access, rate limiting and live
observability.

**Everything to run it**

One MariaDB database (schema + additive migrations), the deploy / build / backup
scripts, the multi-server launch tooling, and the docs.

## How it's built

- One shared library: a **write-behind player cache** (one SELECT per session,
  batched flushes, **zero per-tick SQL**), an idempotent credit ledger, a single JSON
  config tree, additive re-runnable migrations.
- The website reads the **same** MariaDB through a swappable data source; a
  signed-token bridge carries privileged actions to the servers.
- Schema validation and server-side authorization on every admin route.
- 31 unit tests, green. Builds clean (`dotnet build` + `next build`).

## How to buy

1. **Add `gon.lyxx` on Discord.**
2. Tell me your player count and what you run today — I'll show the network live and
   quote you.
3. Pay, and I hand over the full source, the database schema, the deploy scripts and
   the docs, and walk you through the first boot.

No cart, no auto-download — a direct hand-over so you get a working network.

---

<sub>Not affiliated with Valve Corporation. "Counter-Strike" is a trademark of Valve
Corporation. Bundled third-party plugins keep their own licenses.</sub>
