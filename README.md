## Lee Kung

Information Systems student. I build and run small data tools and web services, mostly in Python and TypeScript.

Most of what I work on is operational rather than academic — things that are deployed, have to keep
working, and get measured. I'm more interested in whether something survives contact with real
traffic than in how it looks on a slide.

**Working with:** Python · TypeScript / JavaScript · C++ · SQL · HTML / CSS · Docker · REST APIs · Next.js

### Things I've published

**[Web Data Toolkit](https://web-data-toolkit.vercel.app)** — a hosted REST + MCP service that puts
four public-data endpoints behind one key: YouTube transcripts (single video or a whole channel),
Google Trends, and Google Play reviews. Listed in the official Model Context Protocol registry, so
AI agents can use it as a tool.
→ [`web-data-toolkit-mcp`](https://github.com/leekung125/web-data-toolkit-mcp)

**Six data-extraction Actors on the [Apify Store](https://apify.com/leekung125)** — pay-per-use
scrapers for YouTube transcripts, YouTube channel transcripts, YouTube search, Google Trends,
Google Play reviews and App Store reviews. All HTTP-only with no headless browser, which is a
deliberate design choice: the dominant failure mode in this category is browser timeouts under load.
Each one is priced per result actually delivered, so a run that returns nothing is free.

### How I work

I use AI coding tools heavily — Claude Code in particular — to design, build and operate these
systems. I'd rather be straightforward about that than pretend otherwise: the interesting part of
the work is the architecture, the failure modes, the pricing and the measurement, and that's the
part I own. If you want to talk about any of it, I can walk you through why a decision was made.

### Currently

Learning networking fundamentals, and working on making the data tools reliable enough that someone
would pay for them a second time.
