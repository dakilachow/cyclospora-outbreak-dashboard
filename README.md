# Cyclospora Outbreak Dashboard: 2026 Multistate Surge
 
An independent data-visualization project tracking the 2026 U.S. cyclosporiasis surge, built on publicly available CDC, FDA, and state health department data.
 
## What it is
 
A single-page epidemiological dashboard visualizing the 2026 domestic Cyclospora outbreak:
 
- **Timeline ridgeline chart**: 2000–2026 seasonal case comparison, showing this year's surge against historical baselines
- **Geographic cluster map**: satellite imagery overlay marking reported outbreak centers, color-coded to distinguish the confirmed multistate lettuce outbreak (red: Michigan, Ohio, Indiana, Kentucky, West Virginia) from North Carolina's separate, unconnected outbreak (purple) and unverified reports (grey, e.g. New York City)
- **Comparative dashboard**: environmental variables (precipitation, turbidity, temperature) modeled as hypothesized contributing factors
- **Reference briefing panel**: a static, CDC-sourced summary (not a live AI/search tool — see *Data & Limitations* below)
## Why I built it
 
This started as an exercise in taking a currently unfolding public health event and figuring out how to make it legible, understanding what a public health analyst or journalist covering an outbreak actually needs to see at a glance, and how to visualize uncertainty (like the ~5,100 cases still pending confirmation) honestly rather than smoothing it away.
 
## Data & Sources
 
Case figures reflect the CDC Health Alert Network notice below, published mid-July 2026. **This is a point-in-time snapshot, not live data**, CDC updates its case counts weekly, and totals have already risen since this snapshot was taken.
 
- CDC Health Alert Network. [*Domestically Acquired Cyclosporiasis Cases in Multiple U.S. States, 2026* (CDCHAN-00531)](https://www.cdc.gov/han/php/notices/han00531.html). Published July 14, 2026.
- CDC. [*Surveillance of Cyclosporiasis*](https://www.cdc.gov/cyclosporiasis/php/surveillance/index.html) — current national case totals, updated weekly.
- CDC. [*Cyclospora Outbreak Investigation, July 2026*](https://www.cdc.gov/cyclosporiasis/outbreaks/07-26/investigation.html) — details on the confirmed multistate outbreak linked to iceberg lettuce (Indiana, Kentucky, Michigan, Ohio, West Virginia), sourced to Taylor Farms de México and served at Taco Bell locations.
- CDC. [*Where People Got Sick: Cyclospora Outbreak, July 2026*](https://www.cdc.gov/cyclosporiasis/outbreaks/07-26/locations.html) — state-by-state case map.
- North Carolina Department of Health and Human Services. [*North Carolina Seeing Increase in Cyclosporiasis Cases*](https://www.ncdhhs.gov/news/press-releases/2026/07/14/north-carolina-seeing-increase-cyclosporiasis-cases), July 14, 2026 (307 cases, 13 hospitalizations).
- NCDHHS. [*NCDHHS Provides Update on Cyclosporiasis in North Carolina*](https://www.ncdhhs.gov/news/press-releases/2026/07/17/ncdhhs-provides-update-cyclosporiasis-north-carolina), July 17, 2026 — clarifies North Carolina's case increase is a **separate, unconnected event** from the confirmed multistate lettuce/Taco Bell outbreak.
## Important limitations
 
- **Not affiliated with or endorsed by the CDC.** This is an independent project built on public data, not an official CDC product.
- **Case data is a snapshot, not live.** Figures reflect reporting as of mid-July 2026; always check the CDC surveillance page linked above for current totals.
- **North Carolina's cluster is a distinct outbreak.** The map marks it in a different color (purple) and labels it explicitly, since health officials have stated it is not currently linked to the confirmed multistate lettuce outbreak (shown in red).
- **New York City's cluster is unverified.** It's marked in grey since I could not confirm its case count or its connection to either outbreak in official CDC or state sources, treat it as a reported-but-unconfirmed data point.
- **Environmental correlations (precipitation, turbidity, wastewater indices) are illustrative modeling, not established causal findings.** They're included to explore how environmental data visualization might support outbreak investigation, not as validated epidemiological conclusions.
- **The "Reference Briefing" panel returns static, pre-written text**, not a live AI or search lookup, earlier drafts of this project called an external AI API directly from the browser, which would have exposed an API key publicly; that was removed for the published version.
## Reflection
 
In July 2026, while this outbreak was actively unfolding, I built this dashboard to understand it better through data visualization. I've spent most of my career at the crossroads of environmental risk and human health, from landslide hazard mapping in the Philippines to behavioral neuroscience research on stress and the gut microbiome in Massachusetts, and this project let me apply that same instinct to a real time public health event as it happened.
 
I made a deliberate choice early on to build this using real, current CDC data rather than a plausible-looking mock dataset. 
 
**What I learned.** A few things became clear only once I was working directly with real surveillance data, rather than reading about outbreak response in the abstract. The first was how much an outbreak's true scale is always somewhat unknown in real time, CDC reports confirmed cases separately from a much larger pool of cases still under investigation, and at times there have been several times more pending cases than confirmed ones. This reflects how long it takes for a case to move from someone getting sick, to a doctor visit, to a lab test, to a report reaching CDC. The second was how traceback investigation actually works, watching CDC narrow the outbreak from scattered cases across a growing number of states down to a specific product showed me how much patient interview data and shared exposure history underlie a single sentence like "linked to iceberg lettuce."
 
**A mistake I had to correct.** Early in building this, I nearly presented North Carolina's rising case numbers as part of the same multistate outbreak as Michigan and Ohio, because they were reported around the same time and looked, at a glance, like the same pattern. When I went back to primary sources to double-check, I found that NC's own health department had explicitly stated their increase was a separate, unconnected event. I had to re-color and re-label part of my own map to correct it. It was a small error, caught before publishing, but a useful, lesson: two things happening at the same time, in nearby states, are not automatically the same thing, and in public health communication, that distinction matters enormously.
 
This project gave me a concrete sense of what surveillance, traceback, and public health communication actually require, patience with incomplete information, discipline about verifying rather than assuming a pattern, and care in how uncertainty gets presented to the public.
 
I'm still working on a real-time version of this at present, a script that checks CDC's data daily and updates the dashboard automatically, so the numbers stay current rather than reflecting a single snapshot in time. That piece is in progress. I will update it as soon I find time to fix the bug.
 
## Tech
 
Single HTML file: Tailwind CSS, D3.js (ridgeline chart), Leaflet.js with Esri World Imagery tiles (geographic map), Chart.js, and Font Awesome, all loaded via CDN. No build step; open `index.html` directly or view the live version via GitHub Pages.
 
---
*Built by Dakila Aquino Chow — [LinkedIn](https://www.linkedin.com/in/dakila-aquino-chow-082ab178/)*

