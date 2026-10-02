# Rename to Queuelet and sell the small queue

**Rename the app Queuelet and position it as "a read-later queue you actually finish": a deliberately small list of links that sits on your Android home screen and never leaves your phone.** "Link Bucket" collides with a live bookmark service at linkbucket.app, an Android app called "LinkBucket - Bookmark Manager" and several Chrome extensions. Queuelet is the strongest replacement on the evidence: both queuelet.app and queuelet.com had no registration record, no app by that name turned up on Google Play or in indexed App Store pages, and the "-let" suffix says "small queue", which is the product. The market leaves room for this. Every Android competitor with real traction (Instapaper, Raindrop, Readwise, Paperspan) needs an account and a server. The small apps that offer no account and on-device storage pitch themselves as generic bookmark managers, and none of them leads with a home-screen widget or a one-time price. Users already describe their read-later lists as "a graveyard", and two shutdowns (Omnivore in 2024, Pocket in 2025) taught them that a service can delete their library. Lead with the small queue and the widget, and use "no account, no server, nothing to shut down" as the trust layer. Use the Pocket refugee angle only on the website, as a factual import feature. Trademark status for every candidate name is **unverified**, and the app's HTTP User-Agent string currently advertises `linkbucket.app`, a domain owned by the competitor. The complete, character-counted copy deck is at the end.

## "Link Bucket" is taken, and Queuelet is the cleanest replacement

The collision is not marginal. linkbucket.app is a live bookmark product with one-click saving, full-text search, backups, Chrome and Firefox extensions and a mobile version ([Linkbucket](https://linkbucket.app/)). An Android app named "LinkBucket - Bookmark Manager" also exists ([APKPure](https://apkpure.com/linkbucket-bookmark-manager/com.kamuk.bookmark)), along with two Chrome extensions named Link Bucket ([Chrome Web Store](https://chromewebstore.google.com/detail/link-bucket-extension/bhglploadpebgakocohocjckndpaamah)). **Both linkbucket.app and linkbucket.com are registered.** The naming research also ruled out the obvious neighbours. "Later…" names collide with LaterLinks, Later, Laterly and above all LaterBox, an iOS "local-first inbox for links" with nearly the same positioning ([App Store](https://apps.apple.com/mx/app/laterbox/id6756787808)). "Stash" names collide with LinkStash and Stash on iOS. "Tote" names fail because "tote Links" means "dead links" in German ([Wikipedia DE](https://de.wikipedia.org/wiki/Toter_Link)).

Of roughly 110 names screened through registry RDAP lookups, only 15 had both .app and .com unregistered. Three of them scored highest on availability, memorability, fit and store keyword value:

| Rank | Name | .app / .com (RDAP 404 = no record) | Store collisions found | Strength | Cost |
|---|---|---|---|---|---|
| 1 | **Queuelet** | free / free | No exact app; nearest is "Queued: Save for Later" ([Play](https://play.google.com/store/search?q=queue%20read%20later&c=apps)) | The name *is* the pitch ("a little queue"); unique, so it ranks for its own name immediately ([web search](https://en.wikipedia.org/wiki/Queue-it)) | Hard to spell from hearing for non-native speakers ("kjulet") |
| 2 | **LinkSill** | free / free | Only "Sillside" photo widget and "Sill Home" ([Play](https://play.google.com/store/search?q=sill%20links&c=apps)) | Most visual widget metaphor (a windowsill where you put things to grab on the way out); easiest to say in EN/DE/FI/ES | Needs explaining; Swedish "sill" = herring; must be camel-cased to avoid reading as "links ill" |
| 3 | **Tidy Queue** | free / free | Many "Tidy…" apps; "TidyQueue" is a game add-on ([GitLab](https://gitlab.com/ror-addons/tidyqueue)) | Self-explanatory; carries "queue" and the get-through-it promise | Weakest brand; generic "Tidy" prefix buries it in store search |

**Recommendation: Queuelet.** The spelling cost is real, but it matters less for an app that is found through store search and share-sheet use than through word of mouth. A unique coined name also gives the website a clean SERP for its own brand. LinkSill is the fallback if a trademark search turns up a conflict for Queuelet, or if spoken word of mouth becomes the main channel.

Before committing, four checks remain, and none of them was performed. First, run exact and phonetic trademark searches for all three names in Nice classes 9 and 42 on USPTO (tmsearch.uspto.gov), EUIPO/TMview and the WIPO Global Brand Database. Second, confirm availability and price for queuelet.app and queuelet.com at a registrar: a 404 from RDAP is strong evidence but does not rule out premium or reserved names. Third, search the App Store on a device, because the iOS check relied on web-indexed pages and can miss new apps. Fourth, rename the in-app identity. The Android app currently sends the HTTP User-Agent `LinkBucket/<version> (Android; +https://linkbucket.app)` when it fetches page metadata, so every request points site owners at the competitor's domain. That string, the app label and the Play listing must all change before launch. The package ID `com.mattie.linkbucket` is invisible to users and can stay, since a package ID cannot be changed after the first Play upload anyway.

## The open lane on Android is small, visible and server-free

The category broke up after the shutdowns. Mozilla closed Pocket on July 8, 2025 and deleted user data after the export window ([Mozilla](https://blog.mozilla.org/en/mozilla/building-whats-next/)). Omnivore shut down in November 2024 after an acquihire, with about three weeks' notice ([MacPowerUsers](https://talk.macpowerusers.com/t/rip-omnivore-omnivore-to-shut-down-on-15-november/38868)). No single app took over. Instead, the big players compete on reading features, highlights and AI, and all of them run on accounts and subscriptions. Instapaper Premium costs **$5.99/month or $59.99/year** and requires sign-in ([Instapaper](https://www.instapaper.com/premium)). Readwise Reader costs **$9.99–12.99/month** and pitches an AI "GPT copilot" ([Readwise](https://readwise.io/read)). Raindrop runs on cloud collections, and one of its own Play reviewers wrote "Some widgets would be nice though" ([Play](https://play.google.com/store/apps/details?id=io.raindrop.raindropio)). The search-summary origin of that review line is **unverified**.

The "no account" claim on its own does not set the app apart. Pocket Links ("without internet or an account… stored on your device"), Save For Later ("No sign-up or account required"), Smarter Bookmarks and Save It Later all make it, usually as a bullet lower in the description ([Pocket Links](https://play.google.com/store/apps/details?id=com.nofutureapps.pocketlinks); [Save For Later](https://play.google.com/store/apps/details?id=app.pleme.saveforlater)). These apps share three traits: fewer than about 520 reviews each, generic bookmark-manager positioning, and subscription or mixed pricing. **No Android link saver found leads with the widget.** Where widgets appear, they are shortcuts to folders ("one-tap access to your favorite folders"), not the place where you actually work through the queue. The apps closest in spirit, GoodLinks (one-time price, no account, widgets) and Anybox ($39.99 lifetime), are Apple-only ([GoodLinks](https://goodlinks.app); [Anybox](https://anybox.app)). That makes GoodLinks the likely rival once the iOS version ships.

The anti-hoarding idea is already in the air, so the idea alone is not the differentiator. The mechanism is. Burn 451 deletes saves after 24 hours, but only on iOS and Chrome ([Burn 451](https://www.burn451.cloud/)). Queuelet does the opposite of punishing: three slots, with overflow held safely in a 50-item Waiting list. That makes the claim "A queue, not a graveyard" calm and credible rather than anxious. Users supply the vocabulary themselves: "Your 'Read Later' list is a graveyard", "I was building a digital cemetery" ([DEV Community](https://dev.to/the_nortern_dev/your-read-later-list-is-a-graveyard-it-is-time-to-stop-hoarding-388g)), and "queues grow until users wipe the whole list in guilt and uninstall" ([Slax](https://slax.com/blog/read-it-later-history/)). The durability fear is just as concrete: "not as likely to disappear on you" ([HN](https://news.ycombinator.com/item?id=44063662)) and "I never trust anyone to delete my data; I'm happier doing that myself" ([MacPowerUsers](https://talk.macpowerusers.com/t/rip-omnivore-omnivore-to-shut-down-on-15-november/38868)). Raindrop already sells durability ("It won't disappear on you") ([Raindrop blog](https://blog.raindrop.io/pocket-alternatives/)). Queuelet can make a stronger version of that claim because **there is no server to switch off**.

Two caveats temper this. Widget demand is a differentiator, not a validated request: only one review snippet and one open-source pull request asked for it, and Reddit could not be searched. The 3-link cap will also alienate archivists who keep tens of thousands of saves ("~37K saves", [HN](https://news.ycombinator.com/item?id=44063662)). The copy therefore has to present the cap as a design choice, with Pro as an honest escape hatch, rather than hide it.

### Messages hierarchy

**Primary message.** *The read-later list you'll actually finish:* save links from any app into a small queue that lives on your home screen and never leaves your phone.

**Pillar 1, a queue, not a graveyard.** The list stays short by design, and the widget keeps it in sight. Proof points: 3 slots on the free plan; the "Done with it?" prompt after reading; a Waiting list (up to 50) so nothing is lost; the widget with thumbnails.

**Pillar 2, save from anywhere in one tap.** Proof points: the share sheet in any app; the top 3 buckets appear directly in the share sheet; shared text and Process text; automatic titles and preview images; named buckets; search; five sort orders.

**Pillar 3, yours, on your phone.** Proof points: no account, no server and no analytics; metadata is fetched directly from the phone; automatic JSON and plain-text backups to a folder you pick; restore; bookmarks-HTML export; Pro is a one-time purchase. Supporting logic: no server costs is what makes a one-time price sustainable. That answers the "I always wondered how this app will survive" distrust ([MacPowerUsers](https://talk.macpowerusers.com/t/rip-omnivore-omnivore-to-shut-down-on-15-november/38868)).

**Objection handling for the 3-link limit.** Each objection gets a stated answer:

| Objection | Answer |
|---|---|
| "Three is useless, it's a trial." | Three is the point: a short list is one you read. Every other feature is free, including the widget, buckets, backups and themes. |
| "I'll lose links." | No. The fourth and later saves wait in the Waiting list (up to 50) and move in as you clear slots. |
| "I'm a collector." | Pro removes the limit, and you pay once with no subscription. |

Never call the free plan a trial, and never hide the cap below the fold. It appears in the pricing block, the FAQ and the Play description.

## Keywords favour "save links for later", not "Pocket alternative"

No measured search volumes were obtainable: Google Trends returned HTTP 429, and no keyword tool data was available. Relative demand below is inferred from Google autocomplete and from who ranks. "Pocket alternative" is still live in October 2026, with "pocket alternative 2026" suggested and roundups still being published ([autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=pocket+alternative)). Vendor-blog listicles saturate the head term, so a one-page site will not win it. On Play, the "pocket alternative" query returns Instapaper and then irrelevant apps ([Play](https://play.google.com/store/search?q=pocket%20alternative&c=apps&hl=en&gl=US)). The winnable term is link-centric: for "save links for later app android", page one is store listings rather than listicles ([Play: LaterLinks](https://play.google.com/store/apps/details?id=com.dci.dev.holdmylink&hl=en)), and autocomplete confirms "app to save links for later", "app to save links android" and even "app to save recipe links" ([autocomplete](https://suggestqueries.google.com/complete/search?client=firefox&q=app+to+save+links)). "Bookmarks widget for android phone" and "offline bookmark manager android" are low-competition secondary terms. Avoid four terms because other intents pollute them: bare "link saver" (video downloaders), "watch later list" (YouTube), "private bookmark" (AO3) and "pocket replacement" (windows).

Play has no keyword field. It weights the title highest, then the short description, then the full description, and it penalises repetition ([AppTweak](https://www.apptweak.com/en/aso-blog/play-store-keyword-research)). Apple indexes name, subtitle and a 100-character comma-separated field, and bans competitor names there ([Apple](https://developer.apple.com/app-store/product-page/)).

| Keyword / cluster | Priority | Website slot | Google Play slot | Apple slot |
|---|---|---|---|---|
| save links for later / app to save links | P1 | Title tag, meta, OG title, S4 H2 | Title ("Save Links for Later"), short description | Name |
| read later / read-later queue | P1 | Meta, H1, S2 | Short description, full description (3–4 natural uses) | Subtitle |
| home-screen widget / bookmark widget android | P2 | S3 H2 + body, meta | Short description, full description, screenshot 2 | Subtitle ("widget") |
| no account / private / stays on your phone | P2 (differentiator, low search) | Subhead, S6, FAQ | Full description, screenshot 6 | Keyword field ("private", "offline") |
| offline bookmark manager android / bookmark manager | P2 | S7 body, FAQ | Full description ("bookmarks HTML"), tag | Keyword field ("bookmark", "manager") |
| pocket alternative android / import Pocket | P3 (declining, website only) | S7 body, FAQ Q6, footer marks line | Not in title or short description; optional named import line (see below) | Never |
| use cases: recipes, watch later, articles, video | P3 | S4 body | Full description "Buckets" | Keyword field ("recipe", "video", "watch", "article") |

## Store and site rules shape every line of copy

Several hard rules drove the copy deck. On Google Play, the title is capped at 30 characters, the short description at 80, the full description at 4,000 and release notes at 500. The title, icon and developer name may not contain emojis, ALL CAPS, "free", ranking claims ("#1", "best") or price or promotion text ([Play Metadata policy](https://support.google.com/googleplay/android-developer/answer/9898842)). The 500-character release-note limit comes from secondary sources and is **unverified** against an official Help page. Descriptions may not compare the app to competitors or make misleading references to other apps ([Play best practices](https://support.google.com/googleplay/android-developer/answer/13393723)). For that reason the deck's Play description uses a generic import line, and the named "Pocket, Raindrop, Instapaper" version is offered as an optional swap. Naming the import formats is a factual feature statement, but Google has given no explicit ruling either way, so treat it as a **moderate-risk judgment call**. It is also worth little: Pocket exports ended in late 2025, so only users who kept their file benefit. "Free plan" and "one-time purchase" appear in the full description only, as factual explanations of the model.

On Apple, the name and subtitle are capped at 30 characters each, the keyword field at 100 and promotional text at 170. Guideline 2.3.10 bans mentioning other platforms, so the iOS copy contains no "Android" or "Google". Guideline 2.3.7 bans prices and other apps' names in metadata ([App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)). The 4,000-character description limit is long-standing but was not on the page fetched, so it is **unverified**.

On the website, Google truncates titles and descriptions by pixel width, so the targets are about 50–60 and 150–160 characters ([Google Search Central](https://developers.google.com/search/docs/appearance/title-link)). FAQ rich results left Search on May 7, 2026 ([Search Central](https://developers.google.com/search/docs/appearance/structured-data/faqpage)), so the FAQ is there for readers and answer engines, not SERP features. Use `MobileApplication` JSON-LD with `offers.price` 0. Never fabricate `aggregateRating`: SoftwareApplication rich results need real ratings ([Search Central](https://developers.google.com/search/docs/appearance/structured-data/software-app)). The Play badge needs the line "Google Play and the Google Play logo are trademarks of Google LLC." ([Google Play badges](http://play.google.com/intl/en_us/badges/)). The badge size and clear-space rules are **unverified**, because the Partner Marketing Hub page returned 404. The page order in the deck follows the research's recommended sequence: hero, how it works, philosophy, widget, saving and buckets, previews, privacy, backups and import, pricing, FAQ, final CTA, footer. GoodLinks, the best-regarded indie comparable, shows that a one-pager without testimonials works ([GoodLinks](https://goodlinks.app/)). That matters because Play policy bans unattributed testimonials and the app has no reviews yet.

### Data safety and privacy: what the codebase says

Both stores define "collect" as transmitting data off the device to the developer or partners beyond what serving the request requires ([Play Data safety](https://support.google.com/googleplay/android-developer/answer/10787469); [Apple privacy details](https://developer.apple.com/app-store/app-privacy-details/)). A check of the Android build shows no analytics, crash-reporting or ad SDK. The dependencies are AndroidX, Room, Glance, OkHttp, Coil, Ksoup, Play Billing and Play In-App Review. That makes **"No data collected / No data shared"** defensible. The metadata fetch goes straight from the phone to the saved site, and Play Billing payment data is exempt. Two details must appear in the privacy policy even though they do not change the Data safety answer. First, the manifest sets `android:allowBackup="true"`, with rules that include the database, thumbnails and settings. Android's own backup therefore copies Queuelet data to the user's Google account under Google's terms. The research treats this as Google's service rather than developer collection, but that reading is **unverified** with Google. Second, metadata requests first use a desktop-browser User-Agent and then an app User-Agent that names the app and its website, so saved sites can see that the request came from Queuelet. Whether the Play In-App Review library needs a Data safety disclosure was **not researched**.

## Conclusion

The rename is more than a cleanup. A name that means "small queue" turns the free plan's hard limit from a liability into the brand's promise, and it matches the product's real distinctiveness on Android: the queue lives on the home screen, and nothing lives on a server. The competitive evidence suggests the durable moat is not "no account", which four small apps already claim, but the combination of a finite queue, a widget as the main interface and a one-time price. No Android app with traction has assembled those three. Work through four gates in order before buying the domain: trademark searches, registrar price, an on-device App Store search, and a renamed User-Agent string. After launch, the biggest unknowns are market questions the desk research could not answer: whether the widget drives installs, and how many people the 3-link cap converts versus drives away. Measure those through Play Console acquisition and conversion data rather than guess.

## COPY DECK

All copy uses the name **Queuelet**, so a find/replace on "Queuelet" swaps the name. Counts are Python `len()` character counts over the exact text shown, and each item's limit and fit are stated. A limit marked as a target is a pixel-truncation guideline, not a hard cap. `{price}` is a placeholder for the final Play price. Two items are pre-launch only: the hero CTA becomes the official "Get it on Google Play" badge once the listing is live (planned for the week of December 14, 2026). Everything on iOS assumes feature parity with Android (share extension, interactive widget with bucket switching and styles, folder backups via Files). **Verify each iOS claim against the iOS build before submitting.**

### Website (queuelet.app, one page)

**Title tag** [53 / 60, fits] (target 50-60 (pixel-truncated, no hard limit))

> Queuelet: Save links for later on Android, no account

**Meta description** [153 / 160, fits] (target 150-160)

> Save links from any Android app into a small read-later queue on your home screen. No account, no cloud: your links stay on your phone. Pay once for Pro.

**Hero H1** [43 / 60, fits] (keep short; readable in ~5 s)

> The read-later list you'll actually finish.

**Hero subhead** [156 / 180, fits]

> Queuelet saves links from any app into a small queue that lives on your Android home screen. No account, no cloud, no server. Your links stay on your phone.

**Hero primary CTA (pre-launch, until Play listing is live)** [33 / 40, fits] (swap for the official 'Get it on Google Play' badge at launch; badge text is generated by Google, do not retype it)

> Coming to Google Play in December

**Hero microcopy under CTA** [48 / 60, fits]

> Free to start. No sign-up. One-time Pro upgrade.

**Hero secondary CTA** [16 / 25, fits] (anchor to #how)

> See how it works

**Nav anchors** [47 / 60, fits] (#how #widget #privacy #pricing #faq)

> How it works | Widget | Privacy | Pricing | FAQ

**S1 H2 How it works (#how)** [26 / 60, fits]

> Save it. See it. Clear it.

**S1 step 1** [107 / 140, fits]

> Share from any app. Tap Share, pick Queuelet, done. Your top three buckets appear right in the share sheet.

**S1 step 2** [92 / 140, fits]

> See it on your home screen. The widget keeps your queue in view, with titles and thumbnails.

**S1 step 3** [95 / 140, fits]

> Clear it. Come back from a link and Queuelet asks: Done with it? One tap and it's off the list.

**S2 H2 Queue philosophy (#queue)** [24 / 60, fits]

> A queue, not a graveyard

**S2 body** [292 / 400, fits]

```text
Read-later lists grow until nobody opens them. Queuelet does the opposite: it keeps your list short and in sight, so saving something means you'll actually get to it. On the free plan, three links sit in your queue at a time. New saves wait their turn in a Waiting list, so nothing gets lost.
```

**S3 H2 Widget (#widget)** [37 / 60, fits] (secondary keyword: bookmark widget android)

> Your queue, right on your home screen

**S3 body** [273 / 400, fits]

```text
The Queuelet widget shows what's next, with thumbnails, without opening the app. Flip between buckets on the widget itself. Choose Comfortable or Compact rows and a Solid, Tinted or Glass background. It follows your app theme, and the gear on the widget opens its settings.
```

**S4 H2 Save from anywhere / buckets (#buckets)** [40 / 60, fits] (primary keyword: save links)

> Save from any app, into the right bucket

**S4 body** [346 / 420, fits]

```text
Queuelet works wherever Share does: your browser, video apps, social apps, news apps. Sort links into named buckets like Articles, Watch later, Recipes or Trip ideas. Your three most-used buckets show up directly in the share sheet, so a link lands in the right place in one tap. You can also share plain text or select text and use Process text.
```

**S5 H2 Previews and tidy-up (#previews)** [44 / 60, fits]

> Titles and preview images, filled in for you

**S5 body** [252 / 380, fits]

```text
Every link gets its page title and preview image automatically, so your queue looks like a list of things, not a pile of URLs. Search everything, sort by your own order, newest, oldest, title or site, and pick an accent color or the AMOLED black theme.
```

**S6 H2 Privacy (#privacy)** [43 / 60, fits]

> No account. No cloud. Nothing to shut down.

**S6 body** [321 / 420, fits]

```text
Queuelet has no account, no server and no analytics. Your links are stored on your phone and never sent to us. To get a title and preview image, your phone asks the saved page directly, just like opening it in a browser. There's no middleman server, so there's nothing that can be switched off and take your list with it.
```

**S6 trust bullets** [85 / 100, fits] (render as 4 short chips)

> No sign-up | No analytics or tracking | No Queuelet server | Data stays on your phone

**S7 H2 Backups and import (#backup)** [48 / 60, fits]

> Backups you can read. Imports that bring you in.

**S7 body** [324 / 420, fits] (competitor names allowed on own site as factual import formats)

```text
Queuelet backs up automatically to a folder you choose, as JSON and plain text you can open anywhere. Restore in a tap, or export to a bookmarks HTML file any browser can import. Coming from another app? Pro imports Pocket CSV and HTML exports, Raindrop, Instapaper, generic CSV, browser bookmarks HTML and plain-text lists.
```

**S8 H2 Pricing (#pricing)** [42 / 60, fits]

> Free for a small queue. Pay once for more.

**S8 Free card title** [4 / 20, fits]

> Free

**S8 Free card body** [204 / 260, fits]

```text
3 links in your queue at a time, across all buckets. Up to 50 more wait in your Waiting list and move in as room frees up. Every other feature included: widget, buckets, previews, search, themes, backups.
```

**S8 Pro card title** [18 / 30, fits] ({price} = final Play price, e.g. local currency; replace before launch)

> Pro: {price}, once

**S8 Pro card body** [123 / 200, fits]

> Unlimited links and import from other apps and files. A one-time purchase through Google Play. No subscription, no renewal.

**S8 pricing footnote** [66 / 100, fits]

> Your Waiting list moves into your queue as soon as you unlock Pro.


### Website FAQ

**Q1** [38 / 80, fits]

> Why only three links on the free plan?

**A1** [153 / 300, fits]

> Because a short list is one you actually read. Three slots keep your queue honest. If you want more room, Pro removes the limit with a one-time purchase.

**Q2** [39 / 80, fits]

> What happens when I save a fourth link?

**A2** [162 / 300, fits]

> It waits in your Waiting list, which holds up to 50 links. When you finish a link and free a slot, the next one moves in. Unlock Pro and they all move in at once.

**Q3** [21 / 80, fits]

> Do I need an account?

**A3** [87 / 300, fits]

> No. There's no sign-up, no login and no Queuelet server. Open the app and start saving.

**Q4** [26 / 80, fits]

> Where are my links stored?

**A4** [189 / 300, fits]

> On your phone, in the app's private storage. Queuelet also writes automatic backups, as JSON and plain text, to a folder you choose, and you can export to a bookmarks HTML file at any time.

**Q5** [36 / 80, fits]

> Does Queuelet send my data anywhere?

**A5** [185 / 300, fits]

> Not to us. When you save a link, your phone contacts that web page directly to read its title and preview image, the same way a browser would. Queuelet has no analytics and no tracking.

**Q6** [56 / 80, fits]

> Can I move my links from Pocket, Instapaper or Raindrop?

**A6** [205 / 300, fits]

```text
Yes, with Pro. Queuelet imports Pocket CSV and HTML exports, Raindrop and Instapaper exports, generic CSV, browser bookmarks HTML and plain-text lists. You need the export file you saved from your old app.
```

**Q7** [22 / 80, fits]

> Is Pro a subscription?

**A7** [73 / 300, fits]

> No. Pro is a one-time purchase through Google Play. Pay once and keep it.

**Q8** [42 / 80, fits]

> Does it save articles for offline reading?

**A8** [144 / 300, fits]

> No. Queuelet keeps the link, its title and its preview image, and opens the page when you tap it. It's a queue for links, not an offline reader.

**Q9** [27 / 80, fits]

> Is there an iPhone version?

**A9** [74 / 300, fits]

> Not yet. Queuelet launches on Android first; an iPhone version is planned.


### Website (queuelet.app, one page)

**Final CTA H2** [36 / 60, fits]

> Clear your read-later list for good.

**Final CTA body** [102 / 160, fits]

> Save from any app, keep the queue on your home screen, and get to the bottom of it. No account needed.

**Final CTA button** [27 / 40, fits] (if a text button is used next to the badge; otherwise the badge alone)

> Get Queuelet on Google Play

**Footer line 1** [68 / 100, fits] (fill developer name as shown on Play)

> Queuelet. Made by an independent developer. Privacy Policy | Contact

**Footer trademark line** [66 / 120, fits] (required with the badge)

> Google Play and the Google Play logo are trademarks of Google LLC.

**Footer third-party marks line** [112 / 140, fits] (only needed because the page names them)

> Pocket, Instapaper and Raindrop are trademarks of their respective owners. Queuelet is not affiliated with them.

**Open Graph og:title** [41 / 60, fits]

> Queuelet: Save links for later on Android

**Open Graph og:description** [136 / 200, fits] (1-2 sentences)

> A small read-later queue on your home screen. Save from any app, clear it one link at a time. No account; your links stay on your phone.


### Google Play listing

**App name (title)** [30 / 30, fits] (hard limit 30)

> Queuelet: Save Links for Later

**Short description** [79 / 80, fits] (hard limit 80)

> Save links from any app into a small read-later queue with a home-screen widget

**Full description** [2378 / 4000, fits] (hard limit 4000)

```text
Queuelet is a small read-later queue for links. Save from any app, see what's next on your home screen, and clear it one link at a time. No account, no cloud: your links stay on your phone.

SAVE FROM ANY APP
Tap Share in your browser, a video app, a social app or any app with a Share button, and pick Queuelet. Your three most-used buckets appear right in the share sheet, so a link lands in the right list in one tap. You can also share plain text, or select text and use Process text.

A QUEUE, NOT A GRAVEYARD
Read-later lists tend to grow until nobody opens them. Queuelet keeps your list short and in sight. When you come back from a link, it asks "Done with it?" and one tap clears it.

YOUR QUEUE ON YOUR HOME SCREEN
The widget shows your queue with thumbnails, so you see what's next without opening the app.
• Flip between buckets right on the widget
• Comfortable or Compact rows
• Solid, Tinted or Glass background
• Follows the app theme, with a settings gear on the widget

BUCKETS FOR EVERYTHING
Make named buckets for articles, videos to watch later, recipes, shopping, trips or work. Search across everything and sort by your own order, newest, oldest, title or site.

TITLES AND PREVIEWS, AUTOMATICALLY
Queuelet fills in each page's title and preview image for you. Your phone reads them straight from the page; no server sits in between.

PRIVATE BY DESIGN
• No account or sign-up
• No analytics, no ads, no tracking
• No server: your links are never sent to the developer
• Everything is stored on your phone

BACKUPS YOU CAN READ
Automatic backups go to a folder you pick, as JSON and plain text you can open anywhere. Restore whenever you need to, or export to a bookmarks HTML file that any browser can import.

BRING YOUR LINKS (PRO)
Import from export files of other read-later and bookmark apps, CSV files, browser bookmarks HTML and plain-text lists.

FREE AND PRO
The free plan keeps 3 links in your queue at a time, across all buckets. Save more and they wait in a Waiting list (up to 50), then move into your queue as room frees up.
Pro is a one-time purchase, not a subscription. It unlocks unlimited links and import, and moves everything waiting into your queue.

MAKE IT YOURS
Pick an accent color or the true-black AMOLED theme.

Queuelet keeps a short list of links you mean to get to, right where you'll see them. Save it, see it, clear it.
```

**Full description: optional named-import line (swap into BRING YOUR LINKS)** [126 / 4000, fits] (moderate policy risk; see report)

> Import Pocket CSV and HTML exports, Raindrop and Instapaper exports, generic CSV, browser bookmarks HTML and plain-text lists.

**Screenshot caption 1** [23 / 32, fits] (keep under 20% of image area)

> Save links from any app

**Screenshot caption 2** [30 / 32, fits] (keep under 20% of image area)

> Your queue on your home screen

**Screenshot caption 3** [23 / 32, fits] (keep under 20% of image area)

> A bucket for everything

**Screenshot caption 4** [30 / 32, fits] (keep under 20% of image area)

> Titles and previews, automatic

**Screenshot caption 5** [31 / 32, fits] (keep under 20% of image area)

> Done with it? One tap clears it

**Screenshot caption 6** [31 / 32, fits] (keep under 20% of image area)

> No account. Stays on your phone

**Screenshot caption 7** [29 / 32, fits] (keep under 20% of image area)

> Backups you can open and read

**Screenshot caption 8** [21 / 32, fits] (keep under 20% of image area)

> Make the widget yours

**Feature graphic text** [40 / 45, fits] (tagline only; centered; no CTA, no 'best')

> A read-later list you'll actually finish

**What's new (1.0)** [404 / 500, fits] (hard limit 500)

```text
Welcome to Queuelet 1.0.
• Save links from any app's Share menu, plus shared text and Process text
• Named buckets, with your top 3 right in the share sheet
• Home-screen widget with thumbnails, bucket switching and 3 styles
• Automatic titles and preview images
• "Done with it?" after you read
• Automatic local backups, restore and bookmarks export
• Pro: unlimited links and import, one-time purchase
```

**Category** [12 chars, no limit, fits]

> Productivity

**Suggested tags (pick from Console list)** [66 chars, no limit, fits] (names unverified against Play's predefined list)

> Read later | Bookmark manager | Productivity | Widgets | Organizer


### Apple App Store listing (later)

**Name** [30 / 30, fits] (hard limit 30)

> Queuelet: Save Links for Later

**Subtitle** [30 / 30, fits] (hard limit 30)

> Small read-later queue, widget

**Keyword field** [98 / 100, fits] (hard limit 100; no spaces, no name/subtitle words, no competitor names)

> bookmark,manager,url,article,recipe,video,watch,reading,list,inbox,organize,private,offline,import

**Promotional text** [150 / 170, fits] (hard limit 170; editable without release)

> Save links from any app into a short queue that sits on your Home Screen. No account, and your links stay on your iPhone. Clear it one link at a time.

**Description** [1986 / 4000, fits] (4000 per long-standing ASC limit (verify))

```text
Queuelet is a small read-later queue for links. Save from any app, see what's next on your Home Screen, and clear it one link at a time. No account, no cloud: your links stay on your iPhone.

SAVE FROM ANY APP
Tap Share in Safari, a video app, a social app or any app with a Share button, and pick Queuelet. Choose a bucket and you're done.

A QUEUE, NOT A GRAVEYARD
Read-later lists tend to grow until nobody opens them. Queuelet keeps your list short and in sight. When you come back from a link, it asks "Done with it?" and one tap clears it.

YOUR QUEUE ON YOUR HOME SCREEN
The widget shows your queue with thumbnails, so you see what's next without opening the app. Switch buckets, pick Comfortable or Compact rows and a Solid, Tinted or Glass look.

BUCKETS FOR EVERYTHING
Make named buckets for articles, videos to watch later, recipes, shopping, trips or work. Search across everything and sort by your own order, newest, oldest, title or site.

TITLES AND PREVIEWS, AUTOMATICALLY
Queuelet fills in each page's title and preview image. Your iPhone reads them straight from the page; no server sits in between.

PRIVATE BY DESIGN
• No account or sign-up
• No analytics, no ads, no tracking
• No server: your links are never sent to the developer
• Everything is stored on your device

BACKUPS YOU CAN READ
Automatic backups go to a folder you pick in Files, as JSON and plain text. Restore whenever you need to, or export to a bookmarks HTML file that any browser can import.

BRING YOUR LINKS (PRO)
Import from export files of other read-later and bookmark apps, CSV files, browser bookmarks HTML and plain-text lists.

FREE AND PRO
The free plan keeps 3 links in your queue at a time, across all buckets. Save more and they wait in a Waiting list (up to 50), then move in as room frees up.
Pro is a one-time In-App Purchase, not a subscription. It unlocks unlimited links and import.

MAKE IT YOURS
Pick an accent color or the true-black dark theme.

Save it, see it, clear it.
```


### Google Play Data safety answers

| Question | Answer | Basis |
|---|---|---|
| Does your app collect or share any of the required user data types? | **No** | No analytics, ads or crash SDKs in the build. Metadata is fetched directly from the saved site (ephemeral, not sent to the developer). Payments are handled by Play Billing ([Data safety](https://support.google.com/googleplay/android-developer/answer/10787469)) |
| Resulting label | "No data collected", "No data shared" | |
| Is all user data encrypted in transit? / Data deletion request | Not asked when nothing is collected | Verify in Console |
| Privacy policy URL | `https://queuelet.app/privacy` (required even with no collection) | [Play User Data policy](https://support.google.com/googleplay/android-developer/answer/10144311) |

Unverified: whether Android Auto Backup to the user's Google account (enabled in the manifest) and the Play In-App Review library change any answer. The research treats Auto Backup as Google's service, not collection by the developer.

**Apple App Privacy (later):** "Data Not Collected", assuming the iOS build has the same no-SDK architecture.

### Privacy policy page outline (`/privacy`, page title "Queuelet Privacy Policy")

The page must be HTML, not geofenced and not a PDF. It needs these sections:

1. **Who we are.** Developer name exactly as shown on Play, the app name Queuelet, and a contact email.
2. **The short version.** No account, no analytics, no ads and no Queuelet server. Your links stay on your device.
3. **What's stored on your device.** Saved URLs, titles, preview images, buckets, the Waiting list and settings. All of it lives in app-private storage and is never sent to the developer.
4. **Network requests.** When you save a link, your device connects directly to that website to read its title and preview image. The site sees your IP address and a standard request, including a User-Agent that identifies Queuelet. That site's own privacy policy applies. No developer servers are involved.
5. **Backups and export.**
   - Automatic JSON and plain-text backups go to a folder you choose. If you pick a cloud-synced folder, that provider's terms apply.
   - Android's system backup may copy app data to your Google account under Google's terms. Say how to turn it off.
   - Bookmarks-HTML export.
6. **Purchases.** Pro is bought through Google Play Billing (later, Apple In-App Purchase). The developer never receives payment details, only purchase status. The store's own privacy policy applies.
7. **Ratings prompt.** The app may show Google Play's in-app review prompt. That prompt is handled by Google.
8. **Retention and deletion.** Your data stays until you delete links or uninstall the app. Explain how to delete backup files and how to clear system backups.
9. **Third parties and your rights.** No data is sold or shared. Explain how to contact the developer, and how to revoke consent (this is an Apple 5.1.1 requirement).
10. **Children.** The app is not directed at children.
11. **Changes and effective date.**

### Claims and quotes flagged as unverified

These items are not confirmed and must be checked before use:

- **Trademarks.** Trademark status of Queuelet, LinkSill and Tidy Queue has not been checked.
- **Domains.** Registrar availability and price for queuelet.app and queuelet.com have not been confirmed.
- **App Store collisions.** These were checked through web index only, not on a device.
- **Play release notes limit.** The 500-character limit comes from secondary sources only.
- **Play badge.** Badge size, clear-space rules and brand-approval requirements are unconfirmed, because the Partner Marketing Hub returned 404.
- **Play tags.** The tag names in the deck are not confirmed against Play's predefined list.
- **Apple text limits.** The 4,000-character description and What's New limits were not on the fetched Apple page.
- **Raindrop review quote.** The line "Some widgets would be nice though" comes from a search snippet.
- **Burn 451 statistic.** The figure that "84% of saved bookmarks are never reopened" is unsourced vendor marketing and is deliberately not used in the copy.
- **Recipe survey.** The "40% of 18–34s find recipes on TikTok/Reels" survey has no identified source and is not used in the copy.
- **Search demand.** All relative keyword demand is inferred, not measured.
- **Widget demand.** Demand for widgets has not been validated with users.
- **iOS copy.** All iOS feature claims (share extension, interactive bucket-switching widget, Files folder backups) assume parity with Android that does not exist yet.
- **"No ads" claim.** This is based on the dependency list in `linkbucket-android/app/build.gradle.kts`. Keep it true.
