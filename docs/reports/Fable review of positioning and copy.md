# Fable review: "Link Bucket positioning and copy"

Review date: 2026-10-02. Reviewed: the report, the five research notes, and the Android source at `linkbucket-android` (HEAD `1b6cb01` plus the uncommitted working tree, which differs in ways that matter; see finding 12). Spot-checks were run against Google Play, RDAP, Google Search Central, Play Console Help, Apple's App Store Connect reference, the Partner Marketing Hub and Wiktionnaire. Every copy-deck character count was recounted with a script (78 items, 0 mismatches).

## Verdict: ship with fixes

The research is better than most indie launch research: it is honest about what it could not measure, it separates evidence from inference, and most conclusions follow from the notes. The copy deck is clean, policy-aware and correctly counted. It is not shippable as-is for three reasons. First, five feature claims do not match the code (share-sheet buckets, Waiting-list behaviour, the "Done with it?" prompt, "no cloud", the widget gear). Second, the report's single strongest competitive claim ("no Android link saver leads with the widget") is false as written; two apps literally have "Widget" in the name. Third, the positioning has an unaddressed contradiction at its centre: the brand name and headline promise a small queue, the paid tier removes the small queue, and the Waiting list is a graveyard by another name. None of this needs a rework. It needs roughly a day of copy edits, two product decisions (what to call "buckets", whether widget taps go through the app) and a deliberate answer on three launch items the report left open.

Queuelet is an acceptable name, not an obviously best one. The report missed that "queue" is common vulgar French for penis, so "Queuelet" reads as "little dick" to French speakers, and that Play's fuzzy search already surfaces Quizlet for the query. Neither is fatal. Both should be a conscious choice.

## Findings, prioritized

| # | Severity | Area | Finding | Fix |
|---|---|---|---|---|
| 1 | High | Copy accuracy | "Your three most-used buckets appear in the share sheet." Code publishes the first three buckets by position (`BucketShortcuts.publish` sorts by `position`); nothing tracks usage. At HEAD the constant is 4; "3" exists only in the uncommitted diff. | Change to "your first three buckets" everywhere (S1 step 1, S4, Play description, What's new). Commit `MAX_SHORTCUTS = 3`. |
| 2 | High | Copy accuracy | "New saves wait their turn and move in as room frees up" / "the next one moves in". For free users nothing moves automatically. After a delete the app shows a snackbar "There's room for the next waiting link" with an Add action (`MainViewModel.offerNextWaiting`). Auto-placement happens only on Pro unlock. | Say "Queuelet offers the next one" (S2, S8 free card, A2, Play and Apple FREE AND PRO). Replacement copy below. |
| 3 | High | Copy accuracy | "Come back from a link and Queuelet asks: Done with it?" fires only when the link was opened from inside the app (`openUrl(countsAsReading = true)`). Widget rows launch `ACTION_VIEW` directly, so the headline flow (widget -> read -> clear) never shows the prompt. | Product fix preferred: route widget taps through `MainActivity` so the prompt fires. Otherwise, copy must say "open a link from Queuelet". |
| 4 | High | Honesty | "No cloud" (hero, meta, Play and Apple first paragraph) and "never leaves your phone" while `android:allowBackup="true"` with rules that back up the database, thumbnails and settings to the user's Google account by default. A privacy-minded visitor who reads the policy will feel misled. | Replace "no cloud" with "no Queuelet server" / "no server". Add the Android-backup sentence to A4 and the privacy policy. Keep Auto Backup; it is a real user benefit. |
| 5 | High | Research | "No Android link saver found leads with the widget" is false. "Links Widget" (98 Soft, `com.nesoft.mlw`: "save unlimited links to your home screen widget", 5K+ installs, 2.0 stars, ads + IAP) and "LinkFold: Save Links Widget" (Codekyt, `com.codekyt.linkpro`) both lead with it. Neither has traction and both are link launchers, not read-later queues, so the lane is still open. | Reword to "no Android link saver with traction leads with the widget, and none pairs a widget with a finite queue and no account". Add both to competitors.md. |
| 6 | High | Positioning | The brand promise ("a little queue") is the free-tier limit, and Pro removes it. The Waiting list (50) means the graveyard is renamed, not removed. Buckets are near-useless at 3 links total. The report never confronts these. | Reframe: the queue is what the widget shows, not what you store; applies to Pro too. Add FAQ Q10 ("If a short list is the point, why does Pro remove the limit?"). Make the free cap visible in the Play description's first paragraph. |
| 7 | High | Play listing | The 3-link cap is only in the FREE AND PRO block ~1,900 characters down the Play description, below "Read more". Play visitors will discover it in-app and say so in reviews. The report's own rule says never hide it below the fold. | Put one sentence in paragraph one: "Free keeps 3 links at a time; Pro removes the limit with a one-time purchase." Replacement description below (2,485 / 4,000). |
| 8 | High | Launch | No privacy policy exists yet (the site repo contains only docs). The app's in-app URL in the working tree is `https://mattieab.github.io/linkbucket-site/privacy`; the report assumes `queuelet.app/privacy`. Play requires an active, matching URL in Console and in-app at submission. | Decide the canonical URL before the first upload. If GitHub Pages ships first, make the final domain redirect to it (or vice versa) and never let either 404. |
| 9 | High | Naming | French: Wiktionnaire lists "queue" as vulgar for "pénis, sexe de l'homme"; "-let" is a diminutive. Play search for "queuelet" returns Quizlet (#7), so misspellings ("quelet", "queulet") will hit a giant brand. Notes checked EN/DE/FI/ES only. | Accept knowingly, or pick from the clean pool below. If kept, never let discoverability depend on the brand word: keep the descriptor in the Play title permanently. |
| 10 | Medium | Naming | "Bucket" is Link Bucket's metaphor. After the rename, every screen, the widget description ("A bucket of saved links"), the share sheet and the whole copy deck still say "buckets". With "Queuelet" it is an orphaned word. | Decide now: keep "bucket" as a deliberate quirk, or rename to "lists" in app strings and copy. The deck assumes "buckets" with no discussion. |
| 11 | Medium | Launch / Data safety | Google's own In-App Review page now carries a Data safety section: "Data collected on usage: User-entered data (rating and free-text review)… shared… in a public review on the Play Store", followed by "you are solely responsible for deciding how to respond". The report says this was not researched. | Decide and document. The dialog is Play's own UI and the app never sees the text, so "No data collected" is defensible, but write the reasoning down in case of a Console query. |
| 12 | Medium | Report currency | The report's claims about the User-Agent and privacy URL are already stale: the working tree drops `+https://linkbucket.app` from the UA and changes the privacy URL. The widget settings gear (`ic_settings.xml`, `fitsSettingsButton`) and the 3-shortcut limit are also uncommitted. | Commit or discard before copy is final. Copy must describe the build that ships, not the diff. |
| 13 | Medium | Copy accuracy | "The gear on the widget opens its settings" is true only when the widget is wide enough (`fitsSettingsButton`: 4 header buttons plus 72 dp of name). On the default 4x3 size it fits; on narrow placements it does not. | "on wider widgets a gear opens the widget's settings". |
| 14 | Medium | Rename checklist | The report lists UA, app label and Play listing. The code has more user-visible surfaces: backup folder `Downloads/LinkBucket`, files `linkbucket-backup.json`, `linkbucket.txt`, `linkbucket-bookmarks-*.html`, text backup header "Link Bucket — ", `msg_import_own_backup`, `pro_name`, `pro_why`, `share_process_text_label`, `widget_description`, `settings_backup_folder_default`, `AppLinks.PRIVACY_POLICY_URL`. | Full list in section 2. Restore must keep accepting old filenames (it does; detection is by `schemaVersion`). |
| 15 | Medium | Launch | If the Play developer account is a personal account created after 13 Nov 2023, Google requires a closed test with at least 12 opted-in testers for 14 continuous days before production access. For a 14 Dec 2026 launch the test must be running by late November. | Confirm account type now. Start the closed track by the last week of November at the latest. |
| 16 | Medium | Tone | "Free to start." reads as a trial, which the report forbids three paragraphs earlier. | "Free for a small queue." |
| 17 | Medium | Tone | "Clear your read-later list for good." is ambiguous (delete everything?). "Imports that bring you in." is meaningless. | "Get to the bottom of your read-later list." / "Imports that bring your links along." |
| 18 | Low | Research | "Every Android competitor with real traction… needs an account" includes Paperspan, whose account requirement the notes never verified. "Some widgets would be nice though" (Raindrop) is a search snippet and is used as evidence in the report body. | Soften to "the four largest" and drop the Raindrop quote from the report body or mark it inline. |
| 19 | Low | Research | Missed or unprofiled: Linkora (Saketh Pathike, open source, surfaced in Play search), Link Saver (`com.fidluc.linksaver`, in keywords.md but not competitors.md), Chrome's built-in Reading list (free, zero-install, the real default alternative). | Add a line each. Chrome's reading list is the objection "why not just use Chrome?" and deserves an FAQ answer. |
| 20 | Low | Limits | Now verified (the report marked them unverified): Play release notes 500 Unicode characters per language; Apple description 4,000, What's New 4,000, promotional text 170, keywords 100 bytes (bytes, not characters); badge minimum height 28 px, clear space one quarter of badge height, no modification; FAQ rich results gone 7 May 2026. | Remove the "unverified" flags for these. |
| 21 | Low | Copy | Website meta description says "no cloud"; Apple keyword field is fine; Apple promo text fine; What's new says "top 3". | Covered by replacement copy. |

## 1. Research quality

### What holds

I re-ran the load-bearing checks and the notes are accurate on every one I could reproduce:

- Domains. RDAP today: queuelet.app 404, queuelet.com 404, queuelet.io 404, queuelet.dev 404, linksill.app/.com 404/404, tidyqueue.app/.com 404/404. A 404 still is not a registrar quote; the report says so.
- Stores. Play search for "queuelet" returns QueueBee, Queue, Queueless, Quizlet, ParkLet and others; nothing named Queuelet. Web search returns nothing. App Store web search returns nothing. GitHub has "queuelite" (a walk-in queue web app), not "queuelet".
- Pocket and Omnivore dates and the "graveyard" vocabulary are sourced. The user-voice note is upfront that Reddit was unreachable and that quotes came through a summarizing tool. The deck correctly does not quote any of them.
- Keywords. The note is explicit that no volume was measured. The inference (link-centric terms are winnable; "pocket alternative" is a listicle wall) is reasonable and the report does not overstate it.
- Policy. The Play metadata policy (answer 9898842) does not explicitly ban competitor names; the best-practices page (13393723) says "Don't include misleading or irrelevant references to other apps or products" and "Don't use words or phrases… that can mislead users about your app's relationship to… another app". The report's "moderate-risk judgment call" framing for a named-import line is right, and defaulting to the generic line is the correct call.
- FAQ rich results: Search Central's update log confirms "This feature will no longer appear in Google Search starting May 7, 2026" (notice added 8 May), with documentation removed 15 June 2026.

### Where it overreaches or is wrong

1. "No Android link saver found leads with the widget" (report, section 2; competitors.md section 4). Play search for "bookmark widget", "links widget" and "save links widget" all return "Links Widget" (98 Soft) first, and "LinkFold: Save Links Widget" second. The note's own gap list admits the Play search was not exhaustive; the report dropped the caveat. The corrected claim is stronger anyway: the only widget-led link apps are a 2.0-star launcher with ads and an app with no visible rating, and neither is a read-later queue.
2. "Every Android competitor with real traction… needs an account and a server." Instapaper, Raindrop and Readwise yes. Paperspan is listed in competitors.md without any account statement. Minor, but the sentence is in the executive summary.
3. The widget-demand evidence is one search snippet and one open-source PR. The report says so in the caveats paragraph but states "Raindrop… one of its own Play reviewers wrote 'Some widgets would be nice though'" as fact in the body before marking it unverified one sentence later. Pick one.
4. The report asserts "Pocket exports ended in late 2025" and "deleted user data after the export window". The notes carry two dates (8 Oct per Mozilla, 12 Nov per Slax/Tabmark). The report should cite Mozilla's date and note the discrepancy, since the import feature's value depends on how many people kept a file.
5. The report does not flag that its Play-search "no exact Queuelet app" check was done through the web store, which fuzzy-matches aggressively. That is why Quizlet appears in the results, and it is the real finding: the fuzzy match that hides collisions also redirects misspellers.

### Missed competitors and objections

- Chrome for Android's Reading list. Free, pre-installed, syncs. It is the honest answer to "why not just use the browser?" and it is absent from both the competitor note and the FAQ.
- Linkora (open source, F-Droid and Play) appears in Play search for "linksoon". Not profiled.
- Link Saver (`com.fidluc.linksaver`) is quoted in keywords.md for its "no mandatory login… stored locally" pitch but is missing from competitors.md.
- Google Keep and Samsung Internet saved pages are listed as unchecked gaps and stay that way.

### Internal consistency

- naming.md suggests Play titles like "Queuelet: Read Later Links"; the deck uses "Queuelet: Save Links for Later". The deck is right (link-centric keyword cluster), but the note was never reconciled.
- store_and_site_rules.md says to avoid "free" in the short description "given the 'no pricing info' guidance"; the deck complies. The report's Pillar 3 says "Pro is a one-time purchase" belongs in the full description only; the deck complies.
- The deck has two headings "### Website (queuelet.app, one page)"; the second should be "Website: closing sections".

## 2. Naming

### Verification

| Check | Result |
|---|---|
| queuelet .app / .com / .io / .dev (RDAP) | 404 / 404 / 404 / 404 |
| Google Play "queuelet" | No exact match. Results include QueueBee, Queue, Queueless, Queue App, Quizlet, ParkLet |
| App Store (web index) | No match |
| Web, GitHub, npm | No product. Nearest: "queuelite" (GitHub) and Queue-it (company) |
| Trademarks (USPTO/EUIPO/WIPO) | Still unverified. The search front-ends are JS-only; I could not query them either. Run `CM:"queuelet"` on tmsearch.uspto.gov and the EUIPO eSearch plus in classes 9 and 42 by hand |
| French | fr.wiktionary.org/wiki/queue lists sense 9: "Pénis, sexe de l'homme" (vulgar). Common slang, not obscure |
| German / Finnish / Spanish | No bad sense found (German "Queue" is a billiard cue) |

### Is Queuelet the best choice?

It is a reasonable choice. I would not call it the strongest, for four reasons the report underweights:

1. Spelling. "Queue" is one of the most misspelled English words. The report counts the cost as word-of-mouth only, but it also applies to typed Play searches, which fuzzy-match toward Quizlet, and to anyone retyping the URL from a screenshot.
2. French. For an app that will be on Play worldwide, a name that reads as "little dick" to ~80 million French speakers is a real cost. It is survivable (plenty of brands carry an unfortunate meaning somewhere) but it should be chosen with eyes open, and the French Play listing, if any, should lean on the descriptor.
3. Pronunciation. English speakers will split between "KYOO-let" and "kyoo-LAY" (the Chevrolet pattern). Mild.
4. Brand-promise mismatch. "-let" means small. The small queue is the free tier. Pro users, the only ones who pay, get an unlimited app named "little queue". The copy can resolve this (section 3), but the name makes it harder.

What the name does well: it is unique, it ranks for itself immediately, it carries "queue" as a semantic keyword, and it fits the product's actual distinctiveness.

Alternatives I checked (RDAP today; Play search where noted):

| Name | .app | .com | Play exact match | Notes |
|---|---|---|---|---|
| Upnext Links | free | free | none ("NextUp" comedy app is nearest) | Clear meaning, no spelling trap, no bad meaning found; generic, weak brand |
| Queue Shelf | free | free | none | Keeps "queue" keyword and spelling trap; two-word brand |
| Linksoon | free | taken | none | Easy to spell in EN/DE/FI/FR/ES; "soon" carries the read-soon promise; .com taken |
| Fewlinks | free | taken | none ("Few Links") | Literal, humble, keyword-bearing; sounds odd aloud |
| Shortqueue, Littlequeue, Tinyqueue | free | taken | not checked | Same "queue" costs as Queuelet, less distinctive |
| Threelinks, Nextlinks, Soonlinks, Readsoon | free | taken | not checked | Descriptive; "Threelinks" brands the free cap even harder |
| Linklet | taken | taken | none | Out |
| Cuelet | free | taken | not checked | Fixes spelling, loses meaning, looks like "cutlet" |

My recommendation: keep Queuelet if the French connotation is acceptable to you, and mitigate the spelling cost by (a) keeping "Save Links for Later" in the Play title forever, (b) registering queuelet.app and queuelet.com, and (c) not relying on word of mouth in the first year. If the French issue is not acceptable, Linksoon is the cleanest replacement I found: trivially spellable in every target language, no bad meanings found, .app free, no Play collision; its cost is a taken .com and a less "designed" feel. LinkSill, the report's fallback, I would drop: "sill" is an obscure word outside the windowsill phrase and "LinkSill" invites "links ill".

Whatever you pick, the trademark search remains the gate, and it has still not been run by anyone.

### The "bucket" question

The report says a find/replace on "Queuelet" swaps the name. It does not swap the metaphor. "Bucket" appears in roughly 40 app strings, the widget description, the share sheet ("Put in bucket"), the import flow ("Keep tags as buckets") and in every section of the deck. With "Link Bucket" gone, "bucket" is a word with no referent. Options: keep it as a deliberate quirk (cheap, slightly odd), or rename to "lists" (one string pass, and the copy reads better: "your first three lists show up in the share sheet"). Decide before the copy is final; the deck has to change either way.

### Rename checklist from the code

The report names three surfaces. The working tree has these user-visible ones:

- `res/values/strings.xml`: `app_name`, `widget_description` ("A bucket of saved links")
- `strings_app.xml`: `share_process_text_label` ("Save to Link Bucket")
- `strings_messages.xml`: `msg_import_own_backup` ("This is a Link Bucket backup…")
- `strings_settings.xml`: `settings_backup_folder_default` ("Default: Downloads/LinkBucket"), `pro_name` ("Link Bucket Pro"), `pro_why` ("…Pro is how Link Bucket gets paid for.")
- `backup/BackupManager.kt`: `FOLDER = "LinkBucket"`, `linkbucket-backup.json`, `linkbucket.txt`, dated prefix, text header "Link Bucket — "
- `backup/BookmarksHtml.kt`: `linkbucket-bookmarks-yyyyMMdd.html`
- `metadata/HttpConfig.kt`: `APP_UA = "LinkBucket/<version> (Android)"` (domain already dropped in the working tree)
- `AppLinks.kt`: `PRIVACY_POLICY_URL`
- Play Console: app name, developer name, in-app product `pro_unlock` title

Internal names (`com.mattie.linkbucket`, `linkbucket.db`, `Theme.LinkBucket`, log tags, share-target category) can stay. Backup restore detects files by `schemaVersion`, so old filenames keep working after the rename.

## 3. Positioning and messages

### The headline and pillars

"The read-later list you'll actually finish" is good: native vocabulary (the notes prove "graveyard" is how people already talk), a benefit rather than a feature, and it sets up the limit as a feature. Keep it. The three pillars are in the right order. Pillar 2 (save from anywhere) is table stakes and should stay a proof-point section, not a headline. Pillar 3 is shared with at least four small Android apps (the notes say so), and the report is right that "nothing to shut down" is the sharper version.

### The 3-link free plan: honest, but not yet persuasive

The report's objection table is the right instinct. It misses the objection a sharp visitor will actually raise:

"If a short list is the point, why do you sell an unlimited one?"

Today's copy has no answer, and the brand name makes the question louder. The answer exists in the product: the widget only ever shows the rows that fit, and the "Done with it?" prompt clears links one at a time regardless of plan. So the honest framing is: the queue is what you see, not what you store. Free users store 3 (plus 50 waiting); Pro users store everything; both see a short list. That framing makes the limit a storage tier, which is what it is, while keeping the philosophy true for everyone. Replacement S2, S8 and a new FAQ Q10 below do this.

Two further tensions the report should name instead of papering over:

- Waiting is a graveyard with a cap. The copy says "a queue, not a graveyard" and then describes a 50-item holding pen. The honest version is that the pen is capped and visible, and that it is where the "I'll get to it" pile goes to be triaged, not forgotten. Say "up to 50" every time; do not say "nothing gets lost" without saying "until Waiting is full" somewhere (the app itself says "Waiting is full (50 links). Delete a link or go Pro").
- Buckets at 3 links. S4 sells named buckets, share-sheet bucket targets and bucket switching on the widget. With 3 links total, a free user with four buckets has one empty one. The copy should not pretend otherwise; the pricing card's "across all buckets" is the right honesty, and the first paragraph of the Play description should carry it too (finding 7).

Is "3" itself persuasive? It is a demo-sized number, and the user-voice note found no competitor with a deliberately tiny free queue to learn from. The copy cannot fix that; only the number can. If early reviews say "3 is a joke", the fallback is to raise it, not to argue harder. Make sure the number lives in one constant (it does: `Limits.FREE_MAX_LINKS_TOTAL`) and in no screenshot.

### A skeptical Play visitor, walked through

Reads the title and short description: fine, clear. Taps "Read more": sees save-from-anywhere, graveyard, widget, buckets, previews, privacy, backups, import. Only at ~1,900 characters learns that free is 3 links. Installs, shares four links, hits Waiting. Writes "3 links free then paywall, uninstalled". That review is avoidable by one sentence in paragraph one. The "In-app purchases" badge on the listing already primes them; the sentence turns surprise into an informed choice.

The second thing they check is the Data safety card. "No data collected" plus a privacy policy that mentions Android backup, the direct page fetch and the review prompt will read as careful. "No data collected" plus marketing that says "no cloud" while Android backs the database up to Drive will read as spin. Fix the words, not the backup.

## 4. Copy deck

### Accuracy against the app

| Claim | Code | Status |
|---|---|---|
| Free holds 3 links total, across buckets | `Limits.FREE_MAX_LINKS_TOTAL = 3`, `canAddLink` counts all links | Correct |
| Waiting up to 50 | `Limits.FREE_MAX_WAITING = 50` | Correct |
| Waiting links "move in as room frees up" | `offerNextWaiting` shows a snackbar with an Add action; nothing automatic | Wrong (finding 2) |
| Pro unlock moves everything waiting in | `LinkCapture.placeAllOnUnlock`, triggered by `isPro` in `App.kt` | Correct |
| "Three most-used buckets" in the share sheet | `BucketShortcuts.publish`: `sortedBy { position }.take(3)`; HEAD has 4 | Wrong (finding 1). Also, Direct Share targets are shown at the system's discretion; "show up" is safer than "appear" |
| "Done with it?" after you come back from a link | `MainActivity.openUrl(countsAsReading = true)` only; widget uses `ACTION_VIEW` | Partly wrong (finding 3) |
| One tap clears it | Snackbar action is Delete | Correct |
| Widget: thumbnails, bucket switching, Comfortable/Compact, Solid/Tinted/Glass, follows app theme | `WidgetStyle`, `WidgetTheme`, Prev/Next actions | Correct (thumbnails default on) |
| Settings gear on the widget | Uncommitted; `fitsSettingsButton` width condition | Conditional (findings 12, 13) |
| Share plain text / Process text | `ShareIntentReader` extracts a URL from text; no URL = "No link found" | Correct, but "share plain text" should be "share text that contains a link" |
| Automatic titles and preview images, fetched by the phone directly | `MetadataFetcher` via OkHttp, og/twitter/title fallbacks; thumbnails stored locally | Correct |
| Search everything; sort by own order, newest, oldest, title, site | `LinkSearch` (title, url, site), `SortMode` 5 values | Correct |
| Accent colour or AMOLED black | `Accent` enum, `amoled` flag (applies in dark mode) | Correct |
| Automatic JSON and plain-text backups to a folder you choose | `BackupManager`: JSON + `.txt`, SAF folder or default `Downloads/LinkBucket`; debounced 5 min + daily | Correct; "a folder you choose" should allow for the default |
| Restore; bookmarks HTML export | `restore(uri)`, `exportBookmarks` (free) | Correct |
| Import is Pro; formats: Pocket CSV/HTML, Raindrop, Instapaper, generic CSV, bookmarks HTML, text lists | `readImport` paywalls non-Pro; `CsvImport` detects by header, `PocketHtmlImport`, `BookmarksImport`, `TextListImport`, zip | Correct |
| No account, no analytics, no ads | Dependencies: AndroidX, Room, WorkManager, Glance, OkHttp, Coil, Ksoup, Play Billing, Play Review; no analytics or ads SDK | Correct |
| No cloud / never leaves your phone | `allowBackup="true"`, rules include db, thumbs, settings | Misleading (finding 4) |
| Pro one-time purchase via Google Play | `PurchaseProcessor`, product `pro_unlock`, local signature verification | Correct |
| iOS: all claims | No iOS code exists | Flagged by the report; correct to flag |

### Policy compliance

- Play title: 30/30, no "free", no claims. Fine.
- Play short description: no pricing, no ranking. Fine.
- Play full description: no testimonials, no comparisons, generic import line by default. "Free plan" and "one-time purchase" are factual model statements; the best-practices page restricts promotional pricing ("10% off", "free for a limited time"), not this. Fine.
- Screenshot captions: no CTAs, no "best". The "20% of image" figure is not on the current best-practices page (it says "keep text to a minimum"); harmless to keep as a self-imposed rule.
- What's new: no promotion. 404/500. Fine.
- Apple: no platform names, no prices, no competitor names in keywords; "In-App Purchase" wording is fine. Keywords are 98 of 100 bytes, all ASCII. Fine.
- Badge: hub rules verified (min 28 px height, clear space one quarter of height, no recolouring, same size or larger than other badges). The attribution line is not on the hub page I could fetch; keep it anyway, it costs nothing.
- Website pricing: showing a price on your own site is fine.

### Character limits

All 78 deck items recount exactly as claimed (script: Python `len()` over the quoted text; fenced blocks joined with `\n`). No item exceeds its limit. The two 30/30 items (Play title, Apple name/subtitle) have zero slack; if "buckets" becomes "lists" or the name changes, recount.

Newly verified limits: Play release notes 500 Unicode characters per language (Play Console Help 9859348). Apple description 4,000, What's New 4,000, promotional text 170, keywords 100 bytes (App Store Connect platform-version reference). Treat the Apple keyword limit as bytes.

### Tone and clarity: the weakest lines

1. "Free to start." (hero microcopy): trial language.
2. "Backups you can read. Imports that bring you in." (S7 H2): second half says nothing.
3. "Clear your read-later list for good." (final CTA): sounds like wiping it.
4. "Save links from any app into a small read-later queue with a home-screen widget" (Play short description): grammatical but the tail hangs; the queue does not "have" a widget. Acceptable; alternative below.
5. "You can also share plain text" (S4, Play): implies notes; the app only keeps the link inside the text.
6. "Pro: {price}, once" (S8 card title): fine as a card, but "once" alone is terse. "Pro: {price}, one time" reads more naturally.
7. The Play description's "A QUEUE, NOT A GRAVEYARD" header is strong; the body under it is the weakest paragraph in the listing because it promises the prompt the widget cannot deliver. Replacement below.

### SEO placement

Website: title tag carries "save links for later" + "Android" + "no account"; H1 carries "read-later"; H2s carry "home screen", "save from any app", "backups", "privacy". Sensible. Two gaps: "bookmark" appears only in S7 body and A4; add "bookmark" to the S4 or S5 H2 if you want the "offline bookmark manager android" long tail. The FAQ is the right home for "Pocket alternative" and for the missing "Why not Chrome's reading list?" answer.

Play: "read-later" x4, "save links"/"save from any app" x3, "widget" x5, "bookmark" x2, "queue" x6. Not stuffed. Good.

## 5. Missing for launch

1. Privacy policy page. Not written. The outline in the report is good. Add: the app sends a desktop-browser User-Agent first and the app UA only on a 403, so sites see "a normal browser visit" (say exactly that); thumbnails are downloaded and stored locally; bucket names are published to the system as share shortcuts (visible to the launcher only); metadata fetches run in the background over mobile data unless the import Wi-Fi-only option is set; the only permissions are Internet and network state; how to turn off Android backup (Settings > Google > Backup) and how to delete the `Downloads/LinkBucket` files. Name the controller (you) and an email. One effective date.
2. Canonical privacy URL (finding 8). In-app, Console and site must agree, and the URL must be live when you submit.
3. Data safety. "No data collected / No data shared" is defensible: no analytics, metadata fetched device-to-site (ephemeral), payments by Play Billing (exempt by Google's own text), Android Auto Backup is an OS feature under the user's account (Google's help does not address it; the nearest analogue, user-directed uploads to Drive the app never touches, is exempt). The open item is In-App Review (finding 11): Google now documents it as collecting the rating and review text. Write a two-line rationale for answering No and keep it with the Console submission.
4. Closed testing (finding 15). Check the account type today.
5. Uncommitted work (finding 12). The copy describes the working tree, not HEAD.
6. Localization. The app is English-only (one `values/` directory). The keywords note suggests a German listing. Not a launch blocker, but the Play title limit is per language and "Queuelet: Links für später" needs its own count. Decide whether v1.0 is English-only and say so in the plan.
7. Play Console content declarations the report does not mention: ads (No), target audience (13+ or 18+; not for children), news app (No), government app (No), financial features (No), content rating questionnaire. Set up the `pro_unlock` product with its price before the closed test, because the paywall shows the live price string.
8. Pre-registration. Play allows pre-registration for unreleased apps. For a December launch with a site live in November, it is a cheap way to convert "Coming to Google Play in December" into a badge that does something. Optional.
9. Testing the share sheet claim on a real device: Direct Share rows vary by OEM. Screenshot 1 should show whatever the Pixel sharesheet actually shows.

## Replacement copy

All counts are Python `len()`; limits in brackets. Items not listed are unchanged.

**Meta description** [158 / 160]

> Save links from any Android app into a small read-later queue on your home screen. No account, no Queuelet server; links stay on your phone. Pay once for Pro.

**Hero subhead** [147 / 180]

> Queuelet saves links from any app into a small queue on your Android home screen. No account and no Queuelet server: your links live on your phone.

**Hero microcopy under CTA** [58 / 60]

> Free for a small queue. No sign-up. Pro is a one-time buy.

**S1 step 1** [110 / 140]

> Share from any app. Tap Share, pick Queuelet, done. Your first three buckets show up right in the share sheet.

**S1 step 3** [112 / 140] (if widget taps are routed through the app, revert to the original line)

> Clear it. Open a link from Queuelet and when you come back it asks: Done with it? One tap and it's off the list.

**S2 body** [392 / 400]

```text
Read-later lists grow until nobody opens them. Queuelet keeps yours short and in sight: the widget shows what's next, and when you come back from a link it asks whether you're done. On the free plan, three links sit in your queue at a time; anything more waits its turn in a Waiting list (up to 50), so nothing is lost. Pro removes the limit, and the widget still only ever shows what's next.
```

**S3 body** [283 / 400]

```text
The Queuelet widget shows what's next, with thumbnails, without opening the app. Flip between buckets on the widget itself. Choose Comfortable or Compact rows and a Solid, Tinted or Glass background. It follows your app theme, and on wider widgets a gear opens the widget's settings.
```

**S4 body** [358 / 420]

```text
Queuelet works wherever Share does: your browser, video apps, social apps, news apps. Sort links into named buckets like Articles, Watch later, Recipes or Trip ideas. Your first three buckets show up directly in the share sheet, so a link lands in the right place in one tap. You can also share text that contains a link, or select text and use Process text.
```

**S6 H2** [44 / 60]

> No account. No server. Nothing to shut down.

**S7 H2** [58 / 60]

> Backups you can read. Imports that bring your links along.

**S8 Free card body** [222 / 260]

```text
3 links in your queue at a time, across all buckets. Up to 50 more wait in your Waiting list; clear a slot and Queuelet offers the next one. Every other feature included: widget, buckets, previews, search, themes, backups.
```

**A2** [196 / 300]

> It waits in your Waiting list, which holds up to 50 links. When you delete a link and free a slot, Queuelet offers to move the next one in. Unlock Pro and they all move into their buckets at once.

**A4** [297 / 300]

> On your phone, in the app's private storage. Queuelet also writes automatic backups, as JSON and plain text, to a folder you choose, and you can export a bookmarks HTML file at any time. Android's own backup may also copy app data to your Google account; you can turn that off in Android settings.

**Q10 (new)** [60 / 80]

> If a short list is the point, why does Pro remove the limit?

**A10 (new)** [209 / 300]

> Because the queue is what you see, not what you store. Pro lets collectors keep everything in buckets, but the widget still shows only what's next, and the Done-with-it prompt still clears links one at a time.

**Q11 (new, suggested)**

> Why not just use Chrome's reading list?

**A11 (new, suggested; write once the answer is honest for you)** Cover: works from any app's share sheet (not only the browser), a home-screen widget with previews, buckets, plain-file backups you own, and the short-queue prompt. Do not claim anything Chrome also does.

**Final CTA H2** [42 / 60]

> Get to the bottom of your read-later list.

**Play short description, alternative** [77 / 80] (the original 79-character line is also acceptable)

> Save links for later in a small queue on your home screen. No account needed.

**Play full description** [2485 / 4000]

```text
Queuelet is a small read-later queue for links. Save from any app, see what's next on your home screen, and clear it one link at a time. No account, no server: your links stay on your phone. Free keeps 3 links at a time; Pro removes the limit with a one-time purchase.

SAVE FROM ANY APP
Tap Share in your browser, a video app, a social app or any app with a Share button, and pick Queuelet. Your first three buckets appear right in the share sheet, so a link lands in the right list in one tap. You can also share text that contains a link, or select text and use Process text.

A QUEUE, NOT A GRAVEYARD
Read-later lists tend to grow until nobody opens them. Queuelet keeps your list short and in sight. Open a link from Queuelet and, when you come back, it asks "Done with it?" One tap clears it.

YOUR QUEUE ON YOUR HOME SCREEN
The widget shows your queue with thumbnails, so you see what's next without opening the app.
• Flip between buckets right on the widget
• Comfortable or Compact rows
• Solid, Tinted or Glass background
• Follows the app theme; wider widgets get a settings gear

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
The free plan keeps 3 links in your queue at a time, across all buckets. Save more and they wait in a Waiting list (up to 50); clear a slot and Queuelet offers the next one.
Pro is a one-time purchase, not a subscription. It unlocks unlimited links and import, and moves everything waiting into its bucket.

MAKE IT YOURS
Pick an accent color or the true-black AMOLED theme.

Queuelet keeps a short list of links you mean to get to, right where you'll see them. Save it, see it, clear it.
```

**What's new (1.0)** [426 / 500]

```text
Welcome to Queuelet 1.0.
• Save links from any app's Share menu, plus shared text and Process text
• Named buckets, with your first 3 right in the share sheet
• Home-screen widget with thumbnails, bucket switching and 3 styles
• Automatic titles and preview images
• "Done with it?" after you open a link from the app
• Automatic local backups, restore and bookmarks export
• Pro: unlimited links and import, one-time purchase
```

**Apple description**: apply the same three edits (first paragraph "No account, no server: your links stay on your iPhone."; "Open a link from Queuelet and, when you come back, it asks "Done with it?""; FREE AND PRO "clear a slot and Queuelet offers the next one"). The share-sheet bucket line is already generic there and needs no change. Recount before submission; the current 1,986 will move by under 40 characters.

**Report sentence (section 2)**, replace:

> No Android link saver found leads with the widget.

with:

> Two Android apps lead with a widget in their name, Links Widget (98 Soft; 5K+ installs, 2.0 stars, ads and in-app purchases) and LinkFold: Save Links Widget (Codekyt). Both are link launchers rather than read-later queues, and neither has traction. No Android app with traction pairs a widget with a finite queue and no account.

## Sources checked for this review

- RDAP: pubapi.registry.google (.app, .dev), rdap.verisign.com (.com), rdap.identitydigital.services (.io), 2026-10-02
- Google Play search pages for: queuelet, read later widget, bookmark widget, links widget, save links widget, linklet, few links, linksoon, queue shelf, up next links
- Links Widget listing: https://play.google.com/store/apps/details?id=com.nesoft.mlw
- fr.wiktionary.org/wiki/queue
- Play metadata policy: https://support.google.com/googleplay/android-developer/answer/9898842
- Play store listing best practices: https://support.google.com/googleplay/android-developer/answer/13393723
- Play store listing limits: https://support.google.com/googleplay/android-developer/answer/9859152
- Play release notes limit: https://support.google.com/googleplay/android-developer/answer/9859348
- Play Data safety: https://support.google.com/googleplay/android-developer/answer/10787469
- In-App Review data safety section: https://developer.android.com/guide/playcore/in-app-review
- Search Central updates (FAQ rich result): https://developers.google.com/search/updates
- Apple platform version field limits: https://developer.apple.com/help/app-store-connect/reference/platform-version-information
- Google Play badge guidelines: https://partnermarketinghub.withgoogle.com/brands/google-play/google-play/lockups-icons-badges/
- Android source: `linkbucket-android` HEAD `1b6cb01` and working tree (`git status`: 9 modified files, 1 untracked)
