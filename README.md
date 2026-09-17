## Lee Kung

I build small Python services that pull public data and return it as rows, and I publish them so
other people can use them. Information Systems student at Ohio State, CS minor — most of what's
here is self-taught, and I learn by shipping something and then finding out how it breaks.

### [apify-data-actors](https://github.com/leekung125/apify-data-actors)

Source for six scrapers I publish on the [Apify Store](https://apify.com/leekung125): YouTube
transcripts, whole-channel transcripts, YouTube search with ranking, Google Trends, Google Play
reviews and App Store reviews.

**None of them run a headless browser**, and that's the interesting part. Apify publishes 30-day run
stats for every public Actor. The biggest competing Google Trends scraper reads:

```
22,102 runs    62.4% succeeded
               24.4% TIMED OUT     <- the largest single failure bucket
               10.4% aborted
                2.7% failed
```

Nearly a quarter of its runs die waiting on a browser. If you talk to the JSON endpoints the sites
already serve, that failure mode doesn't exist for you. It's also cheap enough to charge per row
instead of per run — so a call that returns nothing is free.

A few other things I settled on that I'd defend:

- **Failures are rows, not exceptions.** A blocked or caption-less video comes back in the dataset
  with a `status`, so a caller can tell "nothing there" apart from "something broke."
- **A missing field is not a failed filter.** YouTube omits view counts and durations plenty. If you
  set `minViews` and the value is unknown, the row is kept — silently dropping most of a result set
  is worse than a blank column.
- Search results carry **the rank each video held for that query**, which most tools throw away and
  is the only field that matters if you're tracking visibility.

### [web-data-toolkit-mcp](https://github.com/leekung125/web-data-toolkit-mcp)

The same data behind one hosted endpoint, registered in the **Model Context Protocol registry** so
Claude, Cursor and other MCP clients can call it as a tool. Nothing to install — point a client at
one URL. Live at [web-data-toolkit.vercel.app](https://web-data-toolkit.vercel.app).

### Elsewhere

A live affiliate-commerce site, and a fair number of desktop builds and repairs — hardware, BIOS,
Windows and Ubuntu, and the boot failures and driver conflicts that come with them.

### How these get built

I use AI coding tools heavily, Claude Code mainly, and I'd rather say so than have anyone infer it.
I'm not claiming I hand-wrote every line. What I decide is which problems are worth solving, how
the thing should behave when a data source misbehaves, and what it should cost — and I can talk
through any of those.

**Python · C++ · JavaScript / TypeScript · SQL · HTML / CSS · Docker · Git · Linux**
