# Search keywords (web SEO + Play/App Store ASO) for Link Bucket, as of Oct 2026

Method note: Google autocomplete was queried directly (suggestqueries.google.com, en/US, 2026-10-02). Google Play search results and listing titles/download counts were pulled from play.google.com (en/US) the same day. Google Trends returned HTTP 429 (blocked) and the legacy Play suggest endpoint (market.android.com/suggest) returns 404, so **no Trends curves and no tool-based volume numbers were obtained**. Everything below about relative demand is inferred from autocomplete presence, SERP composition and app download counts, not measured volume.

## What do people search for around this need?

### Takeaway
Demand clusters into five intents: (1) Pocket refugees ("pocket alternative ..."), (2) generic "read later / read it later app", (3) "save links (for later) app", (4) "bookmark manager / bookmark app android", and (5) feature modifiers (offline, free, open source, self hosted, widget, android). Several of the brief's candidate terms are polluted by unrelated intents ("pocket replacement" = windows, "link saver" = video downloaders, "watch later list" = YouTube, "private bookmark" = AO3).

### Cited Findings
Google autocomplete (en/US, 2026-10-02), raw suggestion lists:
- "pocket alternative" -> pocket alternative free, reddit, android, pocket alternatives 2025, kobo, open source, self hosted, app, offline reading. "pocket alternative 2026" also exists as a suggestion. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=pocket+alternative)
- "pocket replacement" -> dominated by home improvement: pocket replacement windows, window installation, vs full frame, for pants, pool table; only "pocket replacement app" / "pocket replacement kobo" / "pocket replacement reddit" are relevant. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=pocket+replacement)
- "read later app" -> android, free, reddit, self hosted, ios, open source, mac, iphone, chrome. "read later app 2026" -> "best read later app 2026". — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=read+later+app)
- "read it later" -> read it later apps, extension, obsidian, self hosted, pocket, apps android, open source. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=read+it+later)
- "save links app" -> save url app, save links for later app (plus noise: "download links app"). "save links" -> save links app, save links website, save links online, "how can you save a link permanently". — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=save+links)
- "app to save links" -> app to save links for later, for shopping, android, reddit, app to store links, best app to save links, app to save website links, **app to save recipe links**. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=app+to+save+links)
- "save links for later" -> save links for later app, best way to save links for later, save web links for later. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=save+links+for+later)
- "save for later app" -> mostly retail noise (walmart, walgreens, amazon, target); relevant: best save for later app, save links for later app, save for later reading app. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=save+for+later+app)
- "save articles to read later" -> offline, app, best way, best app, how to save articles on substack to read later. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=save+articles+to+read+later)
- "bookmark manager android" -> chrome, best bookmark manager android, bookmark manager app android, google bookmark manager android, firefox, **offline bookmark manager android**, open source bookmark manager android. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=bookmark+manager+android)
- "bookmark app android" -> bookmark manager app android, best bookmark app android, bookmark app download for android. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=bookmark+app+android)
- "bookmark widget" -> bookmark widget iphone, bookmark widget android, bookmark widget chrome, **bookmarks widget for android phone**, ios bookmark widget (first suggestion is an unrelated ArcGIS "experience builder" term). — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=bookmark+widget)
- "link widget android" -> url widget android, family link widget android (noise). Thin suggestion list. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=link+widget+android)
- "link saver" -> download, app, online, instagram, extension, tiktok, youtube: mostly video-downloader intent. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=link+saver)
- "watch later list" -> google, youtube, playlist, movies, google movies: almost entirely YouTube/Google TV intent. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=watch+later+list)
- "private bookmark" -> ao3, safari, chrome, firefox, pixiv, "private bookmark locker": not a link-saver app intent. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=private+bookmark)
- Competitor-alternative queries exist with the same modifiers: "raindrop alternative(s)" -> reddit, open source, self hosted, free; "instapaper alternative(s)" -> free, reddit, open source, kindle, kobo, self hosted, android. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=instapaper+alternative)
- "link manager app" is polluted (tp link, family link, displaylink). — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=link+manager+app)
- Existing small Android apps already pitch the exact "no account, on-device" angle: Link Saver (com.fidluc.linksaver) "no mandatory login... data is stored locally... import or export your links anytime using CSV"; Pocket Links "without internet or an account". — [Link Saver, Google Play](https://play.google.com/store/apps/details?id=com.fidluc.linksaver&hl=en_US); [Pocket Links, Google Play](https://play.google.com/store/apps/details?id=com.nofutureapps.pocketlinks&hl=en_US)

### Inferences
- Search intent clusters:
  - **Switching (Pocket refugees)**: "pocket alternative", "pocket alternative android/free/offline reading/app", "pocket replacement app". Commercial-investigation intent; users compare lists.
  - **Category, generic**: "read later app", "read it later apps", "best read later app 2026", "save articles to read later (app/offline)". Comparison intent; skewed toward article-reading features (reader view, highlights) which Link Bucket does not center on.
  - **Category, link-centric (best fit)**: "save links for later app", "app to save links (android)", "best app to save links", "save web links for later", "save url app", "app to store links". Problem-aware, transactional; matches Link Bucket's share-sheet + buckets model better than "read later".
  - **Bookmark framing**: "bookmark manager android", "bookmark app android", "offline bookmark manager android". Users who think in "bookmarks"; "offline" and "open source" modifiers signal the privacy/local audience.
  - **Use-case long tail**: "app to save recipe links", "app to save links for shopping", "save links from youtube/tiktok/instagram/x" (the latter often mean downloading, so use cautiously).
  - **Widget**: "bookmark widget android", "bookmarks widget for android phone". Low-competition but low-volume niche; a good secondary keyword for the site section on the widget.
- Drop or demote from the candidate list: "pocket replacement" (bare), "link saver" (bare), "watch later list", "private bookmark", "link manager app" — all dominated by other intents. "Watch later" and "recipes" work as bucket examples in copy, not as target keywords.
- "no account" and "private bookmark app" did not surface as autocomplete stems; the privacy intent shows up instead as "offline", "open source", "self hosted" modifiers. Use "offline" and "no account" as supporting copy terms rather than primary targets.

### Gaps
- People-also-ask boxes and Reddit thread titles could not be pulled directly (no SERP scraping beyond the search tool); Reddit appears as an autocomplete modifier ("pocket alternative reddit", "app to save links reddit", "read later app reddit"), confirming people seek Reddit opinions, but specific thread titles were not collected.
- Play Store search autocomplete could not be retrieved (legacy endpoint 404). Needs manual check on a device or an ASO tool trial (AppTweak, AppFollow, Asodesk).

## Relative demand and trend: did "pocket alternative" spike in 2025 and is it still searched in 2026?

### Takeaway
The spike is near-certain in timing (shutdown announced 22 May 2025, read-only 8 July 2025, data deleted Nov 2025) and the term is still alive in Oct 2026: autocomplete offers both "pocket alternatives 2025" and "pocket alternative 2026", and new roundups were still being published in May and Aug 2026. No measured volume numbers were obtainable.

### Cited Findings
- Mozilla announced the Pocket shutdown on May 22, 2025; Pocket went read-only July 8, 2025; data deleted November 12, 2025. — [Tabmark migration guide](https://tabmark.dev/blog/posts/pocket-migration-guide/); [TechCrunch, 27 May 2025](https://techcrunch.com/2025/05/27/read-it-later-app-pocket-is-shutting-down-here-are-the-best-alternatives)
- Export window originally stated until October 8, 2025. — [Medium, M. Bongarts](https://medium.com/@mariusbongarts/pocket-shuts-down-in-july-2025-the-10-best-alternatives-f9420e2b6d99) (conflicts slightly with the Nov 12 deletion date above; both may be true if deletion followed the export window)
- Instapaper "saw a wave of new users" and was chosen by Kobo to replace Pocket on Kobo e-readers. — [Bulkmark blog](https://bulkmark.io/blog/pocket-alternatives-2026) (secondary, vendor blog). This explains the "pocket alternative kobo" / "instapaper alternative kobo" autocomplete suggestions.
- A vendor blog claims Raindrop.io, RibbonLinks and Pinboard consolidated most former Pocket users by Jan-Feb 2026. — [Tabmark blog](https://tabmark.dev/blog/pocket-alternatives) (vendor opinion, no data; treat as unverified)
- "pocket alternative 2026" and "pocket alternatives 2025" both appear in Google autocomplete as of 2026-10-02. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=pocket+alternative)
- Roundups still being published deep into 2026: BuyersPrint (22 May 2026), AllBlogThings (Aug 2026). — [BuyersPrint](https://buyersprint.com/2026/05/22/best-pocket-alternatives-2026/); [AllBlogThings](https://www.allblogthings.com/2026/08/pocket-alternatives.html)
- Google Trends could not be read: API request returned HTTP 429. — (direct test, no URL to cite)
- Searches for public Ahrefs/Semrush volume figures for "pocket alternative" / "read it later" returned no published numbers. — [search results, e.g. HowToGeek](https://www.howtogeek.com/pocket-alternatives/) (no volume data on page)

### Inferences
- "pocket alternative" likely peaked May-July 2025 and has decayed to a long tail, but remains a live query because new roundups are still being written and indexed. It is a declining asset: worth one section/heading on the site, not the site's whole identity.
- Relative demand ranking (inferred from autocomplete breadth and how many publishers target the term; NOT measured): read later app / read it later apps ≈ pocket alternative > bookmark manager android > save links for later app / app to save links > bookmark widget android > link widget android.
- Rate of continued roundup publishing suggests marketers still see traffic on "pocket alternatives"; this is an indicator, not proof.

### Gaps
- No absolute monthly volumes from any tool. To fill: run the list through Google Keyword Planner (free with an Ads account), Ahrefs free Keyword Generator, or Semrush free tier, and open Google Trends in a browser comparing "pocket alternative", "read later app", "bookmark manager android", "save links app" over 5 years.
- No AppTweak/Sensor Tower/AppFollow public data on Play Store search volume for these terms was found.

## Competition: who ranks for the top terms, and what is winnable?

### Takeaway
Head terms ("pocket alternative(s)", "best read later app") are saturated by listicles, most of them written by competing apps' own blogs (Raindrop, Marqly, BeeMind, Readless, Mailist, iLinkVault, SaveThisOne, Supasidebar) plus AlternativeTo and tech press. A new one-page site will not rank there. Winnable territory is Android-specific, local/offline, and use-case long tail. On Google Play, "save links" / "link saver" / "bookmark manager" results are crowded with many small apps (mostly under 10K installs), so the play is relevance + conversion, not exact-match title squatting.

### Cited Findings
- Page 1 for "pocket alternative 2026" (search tool): blog.raindrop.io, alternativeto.net, mailist.app, marqly.com, supasidebar.com, ilinkvault.com, savethisone.com, allblogthings.com, beemind.app — almost all vendor blogs. — [Raindrop blog](https://blog.raindrop.io/pocket-alternatives/); [AlternativeTo](https://alternativeto.net/software/pocket/); [Marqly](https://www.marqly.com/blog/best-pocket-alternatives-2026)
- Page 1 for "best read later app android 2026": linkflare.io, marqly.com, noverload.com, bestoverallapps.com, beemind.app, screvi.com, bestapp.com, readless.app (two pages). — [Linkflare](https://linkflare.io/articles/read-later-app/); [Noverload](https://noverload.com/blog/best-read-it-later-apps-2026); [Readless](https://www.readless.app/compare/best-read-later-apps-2026)
- Tech press also covered the shutdown with alternatives lists: TechCrunch, HowToGeek, Digital Trends. — [HowToGeek](https://www.howtogeek.com/pocket-alternatives/); [Digital Trends](https://www.digitaltrends.com/phones/pocket-alternative/)
- For "save links for later app android", page 1 is Google Play listings (SLink, LaterLinks, Save It Later, Link Saver) and App Store listings, not roundups. — [SLink on Play](https://play.google.com/store/apps/details?id=com.readlater.bookmark.saver&hl=en_US); [LaterLinks on Play](https://play.google.com/store/apps/details?id=com.dci.dev.holdmylink&hl=en)
- Google Play search (en/US, 2026-10-02):
  - "save links": top results LaterLinks: Bookmark Saver (10K+), Save It Later Bookmark Manager (10K+), Link Saver: Bookmark Manager, Linki: Save Links & Videos (100K+), My Link Saver: Bookmarks (100+), Pocket Links: Bookmark Manager (1K+), Pixel Bookmarks (10K+), Savr: Bookmark & Save Links (1K+), followed by ~20 more "link vault/link saver" apps. — [Google Play search](https://play.google.com/store/search?q=save%20links&c=apps&hl=en&gl=US)
  - "read later": Instapaper (500K+), PaperSpan - Read It Later (50K+), Readwise and several small apps. — [Google Play search](https://play.google.com/store/search?q=read%20later&c=apps&hl=en&gl=US)
  - "pocket alternative": Instapaper first, then irrelevant apps (PocketSmith, Pocket FM, Spotify, Pocket Casts, Discord, Reddit). — [Google Play search](https://play.google.com/store/search?q=pocket%20alternative&c=apps&hl=en&gl=US)
  - "bookmark manager" and "link saver": 30+ results, mostly small indie apps (LaterLinks, Save It Later, Pixel Bookmarks, Link Saver variants, Marqly - AI Bookmark Manager 50+). — [Google Play search](https://play.google.com/store/search?q=link%20saver&c=apps&hl=en&gl=US)
  - Download counts above come from the individual listing pages fetched the same day; one parse (com.joo.bookmark "0+") is probably a scraping artifact.

### Inferences
- Web SEO, prioritized for a one-page site (P1 = primary target in title/H1/meta, P2 = H2 sections, P3 = supporting copy/FAQ):
  1. P1 "save links for later app (android)" / "app to save links android" — link-centric intent, SERP made of app listings rather than listicles, so a focused product page can compete.
  2. P1 "pocket alternative for android" with modifiers "offline", "no account", "free" — exact suggestions "pocket alternative android", "pocket alternative offline reading", "pocket alternative free" exist; head term itself is unwinnable, but the Android + offline long tail is weakly served by listicles.
  3. P2 "offline bookmark manager android" / "bookmark manager app android" — autocomplete-confirmed, privacy-leaning audience.
  4. P2 "bookmarks widget for android phone" / "bookmark widget android" — direct match to a distinctive feature; low competition.
  5. P2 "read later app android" — keep in copy for relevance, but don't expect to win "best read later app" against listicles.
  6. P3 use-case terms: "app to save recipe links", "save links from any app", "save youtube links to watch later"; import terms "import pocket export", "instapaper/raindrop import" (factual mentions; competitor names should not be the page's headline).
  7. P3 privacy modifiers: "no account", "local backup", "no cloud", "private".
- A single page can realistically target one primary + a handful of secondary terms; an FAQ section is the natural place for "Is there a Pocket alternative that works offline / without an account?" style long tail.
- On Google Play, title real estate (30 chars) is best spent on "Link Bucket: Save Links Later" or "Link Bucket - Link Saver & Widget"-style pairing of brand + one category term; head terms are crowded but the competitors are small, so ratings and conversion will matter as much as exact keywords.

### Gaps
- No keyword-difficulty scores (Ahrefs KD / Semrush KD) were obtained.
- Whether any page currently ranks for "bookmarks widget for android phone" or "pocket alternative offline reading" was not individually checked.

## How Google Play and App Store index keywords

### Takeaway
Google Play: no keyword field; it indexes title (30 chars, highest weight), short description (80 chars, second), and full description (4,000 chars), with semantic/NLP matching; repeat main terms a few times naturally, never stuff. Policy bans ranking claims, emojis in title, ALL CAPS, repetitive/unrelated keywords and unauthorized brand names. Apple: name 30, subtitle 30, keyword field 100 chars, comma-separated, no competitor names.

### Cited Findings
- Google Play metadata policy: "Your app title must be 30 characters or less"; "Avoid using repetitive or unrelated keywords or references"; no "special characters or all caps to manipulate search ranking"; no store-performance claims such as "#1", "Popular", "App of the year"; "Don't use emojis, emoticons, or repeated special characters" in title/icon/developer name; "Don't use a celebrity's name or a brand's logo without permission"; avoid "free for limited time only"-style promo text. — [Google Play Console Help, Metadata policy](https://support.google.com/googleplay/android-developer/answer/9898842)
- Google Play has no dedicated keyword field; it "scans and analyzes the app's title, short description and long description"; relies on "semantic indexing and advanced Natural Language Processing"; title has "the highest index weight"; short description "carries significant indexing weight"; recommends repeating important keywords "3-5 times naturally" in the long description. — [AppTweak, Google Play keyword research guide 2026](https://www.apptweak.com/en/aso-blog/play-store-keyword-research)
- Weight order title > short description > long description; long description up to 4,000 chars should be written "for humans, not crammed". — [AppRadar academy](https://appradar.com/academy/short-long-app-description); [AppTweak ASO checklist](https://www.apptweak.com/en/aso-blog/app-store-optimization-aso-checklist-for-google-play)
- Apple: app name up to 30 chars; subtitle up to 30 chars; "Keywords are limited to 100 characters total, with terms separated by commas and no spaces"; avoid plurals of words already included, category names or the word "app", duplicate words, special characters; do not use "Competing app names", unauthorized trademarks, or irrelevant terms. — [Apple Developer, Product page](https://developer.apple.com/app-store/product-page/)

### Inferences
- Play: put "Pocket" only as a factual import mention in the long description ("Import from Pocket export files"), never in title/short description; Pocket is a Mozilla trademark and the policy forbids brand use without permission. Same applies to Raindrop/Instapaper.
- Play short description (80 chars) candidate pattern: core verb + object + differentiators, e.g. "Save links from any app into buckets. Home-screen widget. No account needed." (≈77 chars) covers "save links", "widget", "no account".
- Apple keyword field draft (for later; words already in name/subtitle are redundant): `read later,bookmark,bookmarks manager,link saver,url,widget,offline,articles,recipes,watch later,organize,collections,private,import` — trim to 100 chars after the name/subtitle are fixed; no "pocket", "raindrop", "instapaper".

### Gaps
- Google has not published an official statement on keyword density; the "3-5 times" figure is AppTweak's guidance, not Google's.
- Whether Google Play currently indexes developer name, package ID or reviews for search was not confirmed by any primary source found.

## Non-English markets (brief)

### Takeaway
German and Finnish autocomplete for this category is thin; German "lesezeichen app android" and "links speichern app" exist as suggestions; "später lesen app" and Finnish stems returned nothing. Localize the store listing rather than the one-page site at first.

### Cited Findings
- German autocomplete: "lesezeichen app android" and "links speichern app" return themselves as suggestions; "später lesen app" returned no suggestions; "pocket alternative deutsch" returned only unrelated (Pocket Option, Pocket FM). — [Google autocomplete, hl=de](https://suggestqueries.google.com/complete/search?client=firefox&hl=de&q=lesezeichen+app+android)
- Finnish "lue myöhemmin" and "kirjanmerkki sovellus" returned no suggestions. — [Google autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=kirjanmerkki+sovellus)
- AppTweak: "Localization goes beyond translation: it adapts keywords to the cultural specificities and linguistic context of the target audience." — [AppTweak](https://www.apptweak.com/en/aso-blog/play-store-keyword-research)

### Inferences
- German Play listing terms worth testing: "Links speichern", "Lesezeichen", "später lesen", "Lesezeichen-Manager", "Widget". Finnish: "linkit", "kirjanmerkit", "tallenna linkit" (unverified, no autocomplete data). Finnish market is small; low priority unless the developer is Finland-based and wants a home-market listing.
- Non-ASCII queries in the shell test may have been mangled (the echo shows "sp?ter"), so the empty German "später lesen app" result may be an encoding artifact rather than true absence.

### Gaps
- No volume data for any non-English term; recheck "später lesen app" in a browser with correct encoding.
