## Lee Kung

Information Systems student at Ohio State (CS minor). I build systems I actually run — a personal
operating system, two live commerce ventures, and the tooling that keeps them going.

Most of what's here started as a problem I had, not as a tutorial. Some of it is further along than
the rest, and I'd rather it be readable than pretend to be finished.

---

### ⭐ [Ascension](https://github.com/leekung125/ascension) — a personal operating system

Habits with a rank that can *regress*, finances, journal, live business metrics, and a
force-directed dependency graph of its own codebase. Around 20 route groups in one Next.js app with
a visual language that's enforced rather than suggested.

Themed on the Nightmare Spell from *Shadow Slave*, and the theme is load-bearing: a progress bar is
easy to ignore, but a rank that can fall and a codex that counts the days you didn't write are
harder to.

`Next.js 16 · React 19 · TypeScript · Tailwind 4 · Neon Postgres`

---

### [BlackBox Supplies](https://github.com/leekung125/blackbox-supplies) — live gear site

[blackboxsupplies.com](https://blackboxsupplies.com) — utility and readiness gear, routed by
**failure scenario** instead of product category. Dead battery, flat tire, outage, heatwave: start
from the broken thing, decide in two minutes.

Comparison logic is one typed module per product class, because a power station is judged on
watt-hours and surge and a tire inflator isn't — a single generic spec table is how gear sites end
up useless. Content freshness is tracked per page, and the homepage counter reads **0 paid
placements**, which is the actual editorial rule.

`Next.js App Router · TypeScript · Tailwind`

---

### [Maison Noctaura](https://github.com/leekung125/noctaura-publishing-engine) — live jewellery store

[maisonnoctaura.com](https://www.maisonnoctaura.com) — a moissanite jewellery store I run, from
product photography and copy through to the pipeline that schedules content across four channels.

The published modules are the interesting ones: content attribution encoded into `utm_content` so a
single string survives the round trip into Shopify's session analytics and tells you which creative
idea brought someone in, platform limits that were measured rather than read off a docs page, and a
Buffer client built around the fact that an accepted handoff is not a published post.

The orchestrator, claim guard and settings layer are withheld — they carry supplier identity and
unit costs, and there's no version of publishing those that doesn't hand a competitor the cost
structure.

---

### Data tooling

[**apify-data-actors**](https://github.com/leekung125/apify-data-actors) — six Python scrapers
published on the [Apify Store](https://apify.com/leekung125). None run a headless browser, which is
the point: the largest competing scraper in one of these niches loses **24.4% of 22,102 runs to
timeouts**, and a process without a browser can't fail that way.

[**web-data-toolkit-mcp**](https://github.com/leekung125/web-data-toolkit-mcp) — the same data
behind one hosted endpoint, in the Model Context Protocol registry so MCP clients can call it as a
tool. [web-data-toolkit.vercel.app](https://web-data-toolkit.vercel.app)

---

### How these get built

I use AI coding tools heavily, Claude Code mainly, and I'd rather say so than have anyone infer it.
I'm a student and still early — I'm not claiming I hand-wrote every line. What I decide is what
each thing should be, how it behaves when something upstream breaks, and which of my own ideas to
throw out. Happy to talk through any of it.

`Python · C++ · TypeScript / JavaScript · SQL · HTML / CSS · Git · Docker · Linux`
