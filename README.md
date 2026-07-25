Cyclospora Outbreak Dashboard: 2026 Multistate Surge

An independent data-visualization project tracking the 2026 U.S. cyclosporiasis surge, built on publicly available CDC, FDA, and state health department data.

What it is

A single-page epidemiological dashboard visualizing the 2026 domestic Cyclospora outbreak:

Timeline ridgeline chart: 2000–2026 seasonal case comparison, showing this year's surge against historical baselines

Geographic cluster map: satellite imagery overlay marking reported outbreak centers, color-coded to distinguish the confirmed multistate lettuce outbreak (red: Michigan, Ohio, Indiana, Kentucky, West Virginia) from North Carolina's separate, unconnected outbreak (purple) and unverified reports (grey, e.g. New York City)

Comparative dashboard: environmental variables (precipitation, turbidity, temperature) modeled as hypothesized contributing factors

Reference briefing panel: a static, CDC-sourced summary (not a live AI/search tool — see Data & Limitations below)

Why I built it

This started as an exercise in taking a real, currently unfolding public health event and figuring out how to make it legible, what a public health analyst or journalist covering an outbreak actually needs to see at a glance, and how to visualize uncertainty (like the ~5,100 cases still pending confirmation) honestly rather than smoothing it away.

Data & Sources

Case figures reflect the CDC Health Alert Network notice below, published mid-July 2026. This is a point-in-time snapshot, not live data — CDC updates its case counts weekly, and totals have already risen since this snapshot was taken.

CDC Health Alert Network. Domestically Acquired Cyclosporiasis Cases in Multiple U.S. States, 2026 (CDCHAN-00531). Published July 14, 2026.

CDC. Surveillance of Cyclosporiasis — current national case totals, updated weekly.

CDC. Cyclospora Outbreak Investigation, July 2026 — details on the confirmed multistate outbreak linked to iceberg lettuce (Indiana, Kentucky, Michigan, Ohio, West Virginia), sourced to Taylor Farms de México and served at Taco Bell locations.

CDC. Where People Got Sick: Cyclospora Outbreak, July 2026 — state-by-state case map.

North Carolina Department of Health and Human Services. North Carolina Seeing Increase in Cyclosporiasis Cases, July 14, 2026 (307 cases, 13 hospitalizations).

NCDHHS. NCDHHS Provides Update on Cyclosporiasis in North Carolina, July 17, 2026 — clarifies North Carolina's case increase is a separate, unconnected event from the confirmed multistate lettuce/Taco Bell outbreak.

Important limitations
Not affiliated with or endorsed by the CDC. This is an independent project built on public data, not an official CDC product.
Case data is a snapshot, not live. Figures reflect reporting as of mid-July 2026; always check the CDC surveillance page linked above for current totals.
North Carolina's cluster is a distinct outbreak. The map marks it in a different color (purple) and labels it explicitly, since health officials have stated it is not currently linked to the confirmed multistate lettuce outbreak (shown in red).
New York City's cluster is unverified. It's marked in grey since I could not confirm its case count or its connection to either outbreak in official CDC or state sources — treat it as a reported-but-unconfirmed data point.
Environmental correlations (precipitation, turbidity, wastewater indices) are illustrative modeling, not established causal findings. They're included to explore how environmental data visualization might support outbreak investigation — not as validated epidemiological conclusions.
The "Reference Briefing" panel returns static, pre-written text, not a live AI or search lookup — earlier drafts of this project called an external AI API directly from the browser, which would have exposed an API key publicly; that was removed for the published version.
Tech

Single HTML file — Tailwind CSS, D3.js (ridgeline chart), Leaflet.js with Esri World Imagery tiles (geographic map), Chart.js, and Font Awesome, all loaded via CDN. No build step; open index.html directly or view the live version via GitHub Pages
