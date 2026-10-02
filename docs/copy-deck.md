# Linksoon copy deck

**Status:** final draft for the Google Play launch in the week of December 14, 2026. It merges the research report (`docs/reports/Link Bucket positioning and copy.md`), Fable's review (`docs/reports/Fable review of positioning and copy.md`) and the owner's decisions below. Where they conflict, the owner's decisions win, then Fable's fixes, then the report.

**How to use it:** every asset is ready to paste. Each asset shows its character count and limit, counted with a Python script (`len()` over the exact text; fenced blocks joined with `\n`; the Apple keyword field counted in UTF-8 bytes). "Hard limit" is enforced by the store. "Target" is a pixel-truncation guideline. "Self-imposed" is a house rule for readability. `{price}` is the final Play price. The name appears only as "Linksoon", so a find/replace swaps it if the trademark check fails. If the name changes, recount the 30-character items: the Play title and the Apple name have zero slack. The same script checks every asset for banned terms: "bucket"; "no cloud", "never leaves" or "nothing leaves"; "Free to start"; widget-finishing claims ("tick", "✓", "check off", "mark done", "finish links from", "without opening the app"); Android, Google, competitor names and prices in Apple metadata; and "free" or "Pocket" in the Play title and short description.

## Decisions

1. **Name: Linksoon.** Pending a trademark check. Play title "Linksoon: Save Links for Later" (30 / 30). Assumed domain linksoon.app, privacy policy at https://linksoon.app/privacy. The domain is planned, not registered; linksoon.com is taken.
2. **"Lists", never "buckets".** The user-facing word is "lists". The default list is still called Inbox.
3. **Android Auto Backup stays on.** The copy never says "nothing leaves your phone" or "no cloud". The framing is "No account. No servers of ours. Your links live on your phone." An FAQ and the privacy policy explain that Android's own phone backup (Google) can include the app's data, the same as other apps, and that the app also backs up to a folder you choose. Data safety stays "No data collected / No data shared"; the rationale is under Google Play > Data safety.
4. **No widget ✓ button.** The owner removed it from the app. The widget shows the current list's queue with titles and thumbnails; tapping a row opens the link; arrows switch lists; + adds a link; on wider widgets a gear opens widget settings; rows are Comfortable or Compact, the background is Solid, Tinted or Glass, and it follows the app theme. Links are cleared in the app: after you open a link from inside the app, a "Done with <title>?" snackbar offers Delete (with Undo), and you can swipe a link to delete it. The copy never says links can be ticked off, finished or marked done from the widget or the home screen. The story is: the widget keeps your queue in sight and one tap opens a link; you clear it in the app with one tap when you're done.
5. **Accuracy fixes from Fable.** The share sheet shows your first three lists in your list order (not the most-used ones). Waiting links do not move in on their own on the free plan: when a slot frees up (after a delete in the app), the app offers to add the next waiting link (one tap). Pro places all waiting links. The widget gear only appears on wider widgets, and the copy says so where it mentions the gear at all.
6. **Positioning fixes from Fable.** The 3-link free limit is in the first paragraph of the Play full description. The FAQ answers "If a short list is the point, why sell unlimited?": the widget and the queue keep what's next in view on either plan; Pro removes the storage cap for people who keep more. No "Free to start" or other trial-like language. The competitor claim is corrected (see Research corrections).
7. **Policy constraints from the report still apply.** No competitor names in the Play title, the Play short description or any Apple metadata. No "free", "best", ranking claims or prices in titles. "Pocket" appears only as a factual import mention on the website (with a third-party marks line in the footer) and, optionally, in the Play full description via the swap line below. No testimonials, no ratings in structured data. Use `MobileApplication` JSON-LD with `offers.price` 0 and no `aggregateRating`.

## Open items

| Item | Why it matters | When |
|---|---|---|
| Trademark check for "Linksoon" | Run exact and phonetic searches in Nice classes 9 and 42 on USPTO (tmsearch.uspto.gov), EUIPO/TMview and WIPO Global Brand Database. Nobody has run it yet. All copy depends on it. | Before buying the domain |
| Register linksoon.app | RDAP showed no record, which is not a registrar quote. The privacy URL in the app, in Play Console and on the site must match and be live at submission. | Before the first Play upload |
| In-app privacy link | The app still points to the temporary `https://mattieab.github.io/linkbucket-site/privacy`; the copy assumes `https://linksoon.app/privacy`. Switch the app link once the domain is live, or redirect one to the other, and never let either 404. | Before the first Play upload |
| Package ID | The app is still `com.mattie.linkbucket`. Users don't see it, but it is permanent once the app is on Play. Decide whether to keep it or change it. | Before the first Play upload |
| App Store search on a device | The iOS collision check used web-indexed pages only. Search "Linksoon" on an iPhone before the iOS listing. | Before the iOS listing |
| Play closed-test requirement | If the developer account is a personal account created after November 13, 2023, Play requires a closed test with at least 12 opted-in testers for 14 continuous days before production. For a December 14 launch the test must be running by late November. Confirm the account type now. | Now |

**Build status.** The "lists" wording and the Linksoon rename are implemented in the app: the app name, the share-menu label "Save to Linksoon", Linksoon Pro, backups in `Downloads/Linksoon` as `linksoon-backup.json` and `linksoon.txt`, and the User-Agent `Linksoon/<version>`. The widget ✓ button was removed, and the copy no longer mentions it. The only remaining app-side gap the copy depends on is the privacy link (see Open items).

## Research corrections (for the research notes, not the copy)

- Widget-first link apps exist on Android: "Links Widget" (98 Soft; 5K+ installs, 2.0 stars, ads and in-app purchases) and "LinkFold: Save Links Widget" (Codekyt). Both are link launchers, not read-later lists, and neither has traction. The corrected claim: no Android link app with traction pairs a home-screen widget with a short list and no account.
- The default alternative most people already have is Chrome's built-in reading list (free, pre-installed). It belongs in the research notes and in our own thinking. It is not named in any store or site copy.
- Fable's French-language objection applied to "Queuelet" and no longer applies.

## Messages hierarchy

**Primary message.** *The read-later list you'll actually finish.* Save links from any app into a short list that stays in sight on your home screen. One tap on the widget opens a link; one tap in the app clears it when you're done. No account, no servers of ours.

**Pillar 1: a queue, not a graveyard.** The list stays short by design, the widget keeps it in sight, and the app makes clearing it quick.
- Proof: the free plan holds 3 links at a time, across all lists.
- Proof: the widget shows the current list's queue with titles and thumbnails; tap a row to open the link.
- Proof: after you open a link from inside the app, it asks if you're done with it; one tap deletes it, with Undo. You can also swipe a link to delete it.
- Proof: extra saves wait in a Waiting list (up to 50); when a slot frees up, the app offers the next one.

**Pillar 2: save from any app in one tap.**
- Proof: works from any app's Share button; shared text that contains a link; Process text on selected text.
- Proof: your first three lists show up in the share sheet, in your list order. New links go to Inbox otherwise.
- Proof: titles and preview images filled in automatically; search; five sort orders (your own order, newest, oldest, title, site).

**Pillar 3: yours, on your phone.**
- Proof: no account, no sign-up, no servers of ours, no analytics, no ads.
- Proof: titles and images are fetched by your phone directly from the page.
- Proof: automatic JSON and plain-text backups to Downloads or a folder you choose; restore; bookmarks HTML export.
- Proof: Pro is a one-time purchase. No servers to pay for is what makes a one-time price sustainable.
- Honesty line: Android's own phone backup can include the app's data, the same as any app; we can't see it, and you can turn it off.

**Objection handling**

| Objection | Answer |
|---|---|
| "Three is useless. It's a trial." | It isn't a trial and has no time limit. Three at a time is the point: a short list is one you get through. Every other feature is free, including the widget, lists, previews, search, themes and backups. |
| "If a short list is the point, why sell unlimited?" | The list you see and the list you keep are different things. The widget and the queue keep what's next in view on either plan. Pro removes the storage cap for people who want to keep more than three links. |
| "I'll lose links." | No. Extra saves wait in the Waiting list (up to 50). When a slot frees up, the app offers to add the next one in one tap. If Waiting fills up, it tells you. Pro places every waiting link. |
| "I collect thousands of links." | Pro removes the limit, with one payment and no subscription. Import from other apps' export files is part of Pro. |
| "No account means no backup." | Backups are automatic, to files you can open, in Downloads or a folder you choose. Android's own phone backup can also include the app, like any app. |
| "Will it disappear like other read-later services?" | There's no Linksoon server to switch off. The app and your files keep working on your phone. |

Rules: never call the free plan a trial, never hide the cap. It appears in the hero microcopy, the queue section, the pricing block, the FAQ and the first paragraph of the Play description.

## Keyword map

No measured search volumes exist; priorities are inferred from autocomplete and from who ranks (see the report). Play has no keyword field and weights title, then short description, then full description. Apple indexes name, subtitle and the keyword field.

| Keyword / cluster | Priority | Website | Google Play | Apple |
|---|---|---|---|---|
| save links for later / app to save links | P1 | Title tag, OG title, S4 H2, meta | Title, short description, full description | Name |
| read later / read-later list | P1 | H1, meta, S2, final CTA | Short description, full description (natural uses) | Subtitle |
| home-screen widget / bookmark widget android | P2 | S3 H2 and body, meta | Short description, full description, screenshots 2 and 8 | Subtitle ("widget") |
| no account / private / on your phone | P2 (differentiator, low search) | Subhead, S6, FAQ | Full description, screenshot 6 | Keyword field ("private", "offline") |
| bookmark manager / offline bookmark manager android | P2 | S7 body, FAQ | Full description ("bookmarks HTML"), tag | Keyword field ("bookmark", "manager") |
| pocket alternative / import Pocket | P3 (declining; website only) | S7 body, FAQ, footer marks line | Optional named-import swap line in the full description only | Never |
| use cases: articles, watch later, recipes, video | P3 | S4 body | Full description "LISTS FOR EVERYTHING" | Keyword field ("article", "recipe", "video", "watch") |

Avoid: bare "link saver" (video downloaders), "watch later list" (YouTube), "private bookmark" (fan fiction), "pocket replacement" (windows).

# Copy deck

## Website (linksoon.app, one page)

Section order: hero, how it works, queue, widget, saving and lists, previews, privacy, backups and import, pricing, FAQ, final CTA, footer. The hero CTA is pre-launch text until the Play listing is live; then swap in the official "Get it on Google Play" badge (min height 28 px, clear space a quarter of its height, unmodified) and never retype its text.

**Title tag** [53 / 60 chars, target, fits]

> Linksoon: Save links for later on Android, no account

**Meta description** [153 / 160 chars, target, fits]

> Save links from any Android app into a short read-later list on your home screen. No account, no servers of ours. Pay once for Pro if you want more room.

**Hero H1** [43 / 60 chars, self-imposed, fits]

> The read-later list you'll actually finish.

**Hero subhead** [143 / 180 chars, self-imposed, fits]

> Linksoon saves links from any app into a short list on your Android home screen. No account. No servers of ours. Your links live on your phone.

**Hero primary CTA (pre-launch)** [33 / 40 chars, self-imposed, fits] (replace with the official badge at launch)

> Coming to Google Play in December

**Hero microcopy under CTA** [57 / 60 chars, self-imposed, fits]

> Free for 3 links at a time. No sign-up. Pro is paid once.

**Hero secondary CTA** [16 / 25 chars, self-imposed, fits] (anchor to #how)

> See how it works

**Nav anchors** [47 / 60 chars, self-imposed, fits] (#how #widget #privacy #pricing #faq)

> How it works | Widget | Privacy | Pricing | FAQ

### S1 How it works (#how)

**S1 H2** [27 / 60 chars, self-imposed, fits]

> Save it. See it. Finish it.

**S1 step 1** [105 / 140 chars, self-imposed, fits]

> Save it. Tap Share in any app and pick Linksoon. Your first three lists show up right in the share sheet.

**S1 step 2** [107 / 140 chars, self-imposed, fits]

> See it. The home-screen widget keeps what's next in view, with titles and thumbnails. One tap opens a link.

**S1 step 3** [94 / 140 chars, self-imposed, fits]

> Finish it. Back in the app, one tap clears a link you're done with. Or swipe it off your list.

### S2 Queue (#queue)

**S2 H2** [24 / 60 chars, self-imposed, fits]

> A queue, not a graveyard

**S2 body** [328 / 400 chars, self-imposed, fits]

```text
Read-later lists grow until nobody opens them. Linksoon keeps yours short and in sight. On the free plan, three links sit in your queue at a time. Save more and they wait in a Waiting list (up to 50); when a slot frees up, Linksoon offers to add the next one. Pro removes the cap, and the widget still keeps what's next in view.
```

### S3 Widget (#widget)

**S3 H2** [38 / 60 chars, self-imposed, fits]

> What's next, right on your home screen

**S3 body** [336 / 420 chars, self-imposed, fits]

```text
The Linksoon widget shows the queue for your current list, with titles and thumbnails. Tap a row to open the link. Use the arrows to flip between lists and + to add a link. Choose Comfortable or Compact rows and a Solid, Tinted or Glass background; the widget follows the app theme. On wider widgets, a gear opens the widget's settings.
```

### S4 Saving and lists (#lists)

**S4 H2** [44 / 60 chars, self-imposed, fits]

> Save links from any app, into the right list

**S4 body** [341 / 420 chars, self-imposed, fits]

```text
Linksoon works wherever Share does: your browser, video apps, social apps, news apps. New links land in Inbox, or make lists like Articles, Watch later, Recipes or Trip ideas. Your first three lists, in the order you set, show up directly in the share sheet. You can also share text that contains a link, or select text and use Process text.
```

### S5 Previews (#previews)

**S5 H2** [44 / 60 chars, self-imposed, fits]

> Titles and preview images, filled in for you

**S5 body** [251 / 380 chars, self-imposed, fits]

```text
Every link gets its page title and preview image automatically, so your list looks like a list of things, not a pile of URLs. Search everything, sort by your own order, newest, oldest, title or site, and pick an accent color or the AMOLED black theme.
```

### S6 Privacy and trust (#privacy)

**S6 H2** [31 / 60 chars, self-imposed, fits]

> No account. No servers of ours.

**S6 body** [420 / 480 chars, self-imposed, fits]

```text
Your links live on your phone. Linksoon has no sign-up, no analytics, no ads and no server of its own, so we never see what you save. To fill in a title and preview image, your phone asks the saved page directly, the way a browser does. There's no Linksoon service in the middle that could shut down and take your list with it. Like any app, Linksoon can be part of your phone's own Android backup; the FAQ explains how.
```

**S6 trust chips** [85 / 100 chars, self-imposed, fits] (render as 4 short chips)

> No sign-up | No analytics or ads | No Linksoon server | Your links live on your phone

### S7 Backups and import (#backup)

**S7 H2** [58 / 60 chars, self-imposed, fits]

> Backups you can read. Imports that bring your links along.

**S7 body (names Pocket)** [358 / 420 chars, self-imposed, fits] (competitor names allowed on the own site as factual import formats; needs the footer marks line)

```text
Linksoon backs up automatically, as JSON and plain text you can open anywhere, to your Downloads folder or a folder you choose. Restore in a tap, or export a bookmarks HTML file any browser can import. Coming from another app? Pro imports Pocket CSV and HTML exports, Raindrop and Instapaper exports, generic CSV, browser bookmarks HTML and plain-text lists.
```

### S8 Pricing (#pricing)

**S8 H2** [40 / 60 chars, self-imposed, fits]

> Free for three links. Pay once for more.

**S8 Free card title** [4 / 20 chars, self-imposed, fits]

> Free

**S8 Free card body** [231 / 260 chars, self-imposed, fits]

```text
3 links at a time, across all your lists. Up to 50 more wait in your Waiting list; when a slot frees up, Linksoon offers to add the next one in one tap. Everything else is included: widget, lists, previews, search, themes, backups.
```

**S8 Pro card title** [22 / 30 chars, self-imposed, fits] ({price} = final Play price)

> Pro: {price}, one time

**S8 Pro card body** [169 / 220 chars, self-imposed, fits]

```text
Unlimited links, plus import from other apps and files. Every waiting link moves into its list when you unlock. A one-time purchase through Google Play; no subscription.
```

**S8 pricing footnote** [50 / 100 chars, self-imposed, fits]

> The free plan isn't a trial. It has no time limit.

### FAQ (#faq)

The FAQ is for readers and answer engines; FAQ rich results left Google Search on May 7, 2026, so no FAQ markup is needed.

**Q1** [38 / 80 chars, self-imposed, fits]

> Why only three links on the free plan?

**A1** [193 / 300 chars, self-imposed, fits]

> Because a short list is one you actually get through. Three links at a time keep it honest. The free plan has no time limit. If you want more room, Pro removes the cap with a one-time purchase.

**Q2** [49 / 80 chars, self-imposed, fits]

> If a short list is the point, why sell unlimited?

**A2** [213 / 300 chars, self-imposed, fits]

```text
Because the list you see and the list you keep are different things. The widget and the queue keep what's next in view on either plan. Pro removes the storage cap for people who want to keep more than three links.
```

**Q3** [39 / 80 chars, self-imposed, fits]

> What happens when I save a fourth link?

**A3** [238 / 300 chars, self-imposed, fits]

```text
It goes to your Waiting list, which holds up to 50 links. When a slot frees up, Linksoon offers to add the next waiting link; one tap does it. If Waiting fills up, delete a link or go Pro. With Pro, every waiting link moves into its list.
```

**Q4** [44 / 80 chars, self-imposed, fits]

> How do I clear a link when I'm done with it?

**A4** [238 / 300 chars, self-imposed, fits]

> In the app. After you open a link from inside Linksoon, it asks if you're done with it: tap Delete, and Undo is there if you change your mind. You can also swipe a link away. The widget keeps your list in sight and opens links in one tap.

**Q5** [21 / 80 chars, self-imposed, fits]

> Do I need an account?

**A5** [87 / 300 chars, self-imposed, fits]

> No. There's no sign-up, no login and no Linksoon server. Open the app and start saving.

**Q6** [26 / 80 chars, self-imposed, fits]

> Where are my links stored?

**A6** [211 / 300 chars, self-imposed, fits]

```text
On your phone, in the app's private storage. Linksoon also writes automatic backups, as JSON and plain text, to your Downloads folder or a folder you choose, and you can export a bookmarks HTML file at any time.
```

**Q7** [40 / 80 chars, self-imposed, fits]

> Does my phone's backup include Linksoon?

**A7** [256 / 300 chars, self-imposed, fits]

```text
It can. If Android backup is on, your phone's backup to your Google account can include Linksoon's links, thumbnails and settings, the same as other apps. Google runs that backup under your account; we can't see it. You can turn it off in Android settings.
```

**Q8** [36 / 80 chars, self-imposed, fits]

> Does Linksoon send my data anywhere?

**A8** [180 / 300 chars, self-imposed, fits]

> Not to us. When you save a link, your phone asks that web page directly for its title and preview image, the way a browser would. Linksoon has no analytics, no ads and no tracking.

**Q9 (names Pocket)** [56 / 80 chars, self-imposed, fits]

> Can I move my links from Pocket, Instapaper or Raindrop?

**A9 (names Pocket)** [205 / 300 chars, self-imposed, fits]

```text
Yes, with Pro. Linksoon imports Pocket CSV and HTML exports, Raindrop and Instapaper exports, generic CSV, browser bookmarks HTML and plain-text lists. You need the export file you saved from your old app.
```

**Q10** [22 / 80 chars, self-imposed, fits]

> Is Pro a subscription?

**A10** [73 / 300 chars, self-imposed, fits]

> No. Pro is a one-time purchase through Google Play. Pay once and keep it.

**Q11** [42 / 80 chars, self-imposed, fits]

> Does it save articles for offline reading?

**A11** [143 / 300 chars, self-imposed, fits]

> No. Linksoon keeps the link, its title and its preview image, and opens the page when you tap it. It's a list for links, not an offline reader.

**Q12** [27 / 80 chars, self-imposed, fits]

> Is there an iPhone version?

**A12** [74 / 300 chars, self-imposed, fits]

> Not yet. Linksoon launches on Android first; an iPhone version is planned.

### Final CTA and footer

**Final CTA H2** [42 / 60 chars, self-imposed, fits]

> Get to the bottom of your read-later list.

**Final CTA body** [120 / 160 chars, self-imposed, fits]

> Save from any app, keep what's next on your home screen, and clear links in one tap when you're done. No account needed.

**Final CTA button** [27 / 40 chars, self-imposed, fits] (only if a text button sits next to the badge; otherwise the badge alone)

> Get Linksoon on Google Play

**Footer line** [68 / 100 chars, self-imposed, fits] (Contact = mailto:{contact email})

> Linksoon. Made by an independent developer. Privacy Policy | Contact

**Footer Google Play trademark line** [66 / 120 chars, self-imposed, fits] (required with the badge)

> Google Play and the Google Play logo are trademarks of Google LLC.

**Footer third-party marks line (names Pocket)** [112 / 140 chars, self-imposed, fits] (needed because S7 and the FAQ name them)

> Pocket, Instapaper and Raindrop are trademarks of their respective owners. Linksoon is not affiliated with them.

**Open Graph og:title** [41 / 60 chars, target, fits]

> Linksoon: Save links for later on Android

**Open Graph og:description** [157 / 200 chars, target, fits]

> A short read-later list on your home screen. Save from any app, open links from the widget, clear them in one tap. No account; your links live on your phone.

### Privacy policy page (`/privacy`)

Publish at https://linksoon.app/privacy as a plain HTML page (not a PDF, not geofenced). Page title: "Linksoon Privacy Policy". Fill `{developer name}` exactly as shown on Play, plus `{contact email}` and `{effective date}`. Keep it in sync with the build: if an SDK or a server is ever added, this page and the Data safety form change first.

**Privacy policy full text** [5231 chars, no limit] (Markdown; convert to HTML for the site)

````markdown
# Linksoon Privacy Policy

Effective date: {effective date}

## Who we are

Linksoon is an Android app made by {developer name}, an independent developer ("we", "us"). This policy explains what happens to your information when you use Linksoon. If you have a question, email {contact email}.

## The short version

- Linksoon has no account, no sign-up and no servers of ours.
- We don't collect, receive, sell or share your links or any other personal data.
- The app contains no analytics, advertising or tracking code.
- Your links live on your phone. Copies exist only where you or your phone's settings put them: your own backup files, and Android's backup if you have it turned on.

## What Linksoon stores on your phone

- The links you save, with their page titles, site names and preview images (thumbnails).
- Your lists, their order, and your Waiting list.
- Your settings, such as theme, sort order, widget style and backup folder.
- Whether you have bought Pro.

This data is kept in the app's private storage on your phone. It is never sent to us.

## Reading titles and preview images

When you save a link, Linksoon connects directly from your phone to that web page to read its title and preview image, and downloads the image so it can be shown in the app and on the widget. This works like opening the page in a browser: the website receives a normal web request, which includes your IP address and the address of the page. Linksoon first presents itself as a regular desktop browser. If the site refuses that request, the app tries once more and identifies itself as Linksoon. The website's own privacy policy applies to these requests. No server of ours is involved, and we never see which links you save.

These requests can run in the background and can use mobile data. When you import links, you can choose to fetch titles and images over Wi-Fi only.

## Share sheet shortcuts

To show your first three lists in Android's share sheet, Linksoon gives their names to Android as sharing shortcuts. They stay on your phone.

## Backups and export

**Automatic backups.** Linksoon regularly saves a backup of your links and lists, as a JSON file and a plain-text file, to your Downloads folder (Downloads/Linksoon) or to a folder you choose. These files are yours. If you choose a folder that syncs to a cloud service, that service's terms and privacy policy apply to the copies it stores.

**Export.** You can export your links as a bookmarks HTML file at any time, to a place you choose.

**Android backup.** Like most apps, Linksoon lets Android include its data in your phone's own backup. If backup is turned on, Android may copy your links, thumbnails and settings to your Google account and restore them when you set up a new phone. Android may also copy them during a direct transfer from your old phone to a new one. This backup is provided by Google under your Google account and Google's privacy policy; we have no access to it. You can turn it off in your phone's settings (usually Settings > Google > Backup, or Settings > System > Backup, depending on your phone).

## Purchases

Linksoon Pro is sold through Google Play. Google Play handles the payment, and we never receive your card or payment details. The app receives only a record from Google Play that Pro was bought, and checks it on your phone. Google's terms and privacy policy apply to the purchase.

## Ratings prompt

Linksoon may occasionally ask Google Play to show its in-app rating prompt. The prompt is part of Google Play. If you leave a rating or a review, it goes to Google Play and is published under your Google Play profile according to Google's terms. Linksoon never receives your rating or review text.

## Permissions

Linksoon asks Android for internet access and network-state access. It uses them to read titles and preview images and to check your connection. It does not ask for your location, contacts, camera or microphone. It opens other files only when you choose them, for example a backup folder or a file to import or restore.

## Keeping and deleting your data

Your data stays on your phone until you delete it. Deleting a link removes it from the app. Uninstalling Linksoon, or clearing its storage in Android settings, removes everything stored in the app. Backup and export files stay in the folder they were saved to until you delete them. To remove Android's backup copy, turn off backup or delete the backup in your Google account.

## Sharing and selling

We don't sell, rent or share personal data, because we don't have any. Linksoon contains no third-party analytics, advertising or tracking libraries.

## Your rights

Because we don't collect personal data, we hold nothing about you to access, correct or delete. Your data is under your control on your phone. If you have a question or a request, email {contact email} and we'll reply.

## Children

Linksoon is not directed at children under 13, and we don't knowingly collect data from anyone.

## Changes to this policy

If this policy changes, we'll update this page and the effective date above. If a change affects how the app handles your data, we'll also say so in the app's release notes.

## Contact

{developer name}
{contact email}
````

## Google Play listing

**Play title** [30 / 30 chars, hard limit, fits]

> Linksoon: Save Links for Later

**Play short description** [73 / 80 chars, hard limit, fits]

> Save links to read later and keep them in sight with a home-screen widget

**Play full description** [2885 / 4000 chars, hard limit, fits]

```text
Linksoon is a short read-later list for links. Save from any app, see what's next on your home screen, and clear links in the app with one tap when you're done. No account. No servers of ours. Your links live on your phone. The free plan keeps 3 links at a time; Pro removes the limit with a one-time purchase.

SAVE FROM ANY APP
Tap Share in your browser, a video app, a social app or any app with a Share button, and pick Linksoon. New links go to Inbox, or straight into one of your lists: your first three lists show up right in the share sheet. You can also share text that contains a link, or select text and use Process text.

WHAT'S NEXT, ON YOUR HOME SCREEN
The widget shows the queue for your current list, with titles and thumbnails. Tap a row to open the link.
• Flip between lists with the arrows
• Add a link with +
• Comfortable or Compact rows
• Solid, Tinted or Glass background
• Follows the app theme; on wider widgets, a gear opens widget settings

A QUEUE, NOT A GRAVEYARD
Read-later lists tend to grow until nobody opens them. Linksoon keeps yours short and in sight. Open a link from inside the app and, when you come back, it asks if you're done with it. One tap deletes it, with Undo if you change your mind. You can also swipe a link away.

LISTS FOR EVERYTHING
Make lists for articles, videos to watch later, recipes, shopping, trips or work. Search across everything and sort by your own order, newest, oldest, title or site.

TITLES AND PREVIEWS, AUTOMATICALLY
Linksoon fills in each page's title and preview image for you. Your phone reads them straight from the page; no server of ours sits in between.

PRIVATE BY DESIGN
• No account or sign-up
• No analytics, no ads, no tracking
• No servers of ours: your links are never sent to the developer
• Your links live on your phone. Like any app, Linksoon can be part of your phone's own Android backup if you have it turned on.

BACKUPS YOU CAN READ
Automatic backups go to your Downloads folder or a folder you pick, as JSON and plain text you can open anywhere. Restore whenever you need to, or export a bookmarks HTML file that any browser can import.

BRING YOUR LINKS (PRO)
Import from export files of other read-later and bookmark apps, CSV files, browser bookmarks HTML and plain-text lists.

FREE AND PRO
The free plan keeps 3 links at a time, across all your lists, with no time limit. Save more and they wait in a Waiting list (up to 50). When a slot frees up, Linksoon offers to add the next one; one tap does it.
Pro is a one-time purchase, not a subscription. It removes the limit, unlocks import and places every waiting link in its list. The widget still keeps what's next in view, so your list stays easy to get through.

MAKE IT YOURS
Pick an accent color or the true-black AMOLED theme.

Linksoon keeps the links you mean to get to right where you'll see them. Save it, see it, finish it.
```

**Play optional named-import line (names Pocket)** [126 / 4000 chars, hard limit, fits] (swap into BRING YOUR LINKS only if you accept the moderate policy risk; the generic line is the default)

> Import Pocket CSV and HTML exports, Raindrop and Instapaper exports, generic CSV, browser bookmarks HTML and plain-text lists.

Screenshot captions: keep text minimal and the 3-link number out of every screenshot. Screenshot 1 must show what a Pixel share sheet actually shows (Direct Share rows vary by device). Screenshot 3 shows the in-app "Done with <title>?" snackbar with Delete, not the widget.

**Play screenshot caption 1** [23 / 32 chars, self-imposed, fits]

> Save links from any app

**Play screenshot caption 2** [32 / 32 chars, self-imposed, fits]

> What's next, on your home screen

**Play screenshot caption 3** [31 / 32 chars, self-imposed, fits]

> Done with it? Clear it in a tap

**Play screenshot caption 4** [21 / 32 chars, self-imposed, fits]

> A list for everything

**Play screenshot caption 5** [30 / 32 chars, self-imposed, fits]

> Titles and previews, automatic

**Play screenshot caption 6** [31 / 32 chars, self-imposed, fits]

> No account. No servers of ours.

**Play screenshot caption 7** [29 / 32 chars, self-imposed, fits]

> Backups you can open and read

**Play screenshot caption 8** [21 / 32 chars, self-imposed, fits]

> Make the widget yours

**Play feature graphic text** [40 / 45 chars, self-imposed, fits] (tagline only, centered, no CTA)

> A read-later list you'll actually finish

**Play What's new (1.0)** [440 / 500 chars, hard limit, fits]

```text
Welcome to Linksoon 1.0.
• Save links from any app's Share menu, plus shared text and Process text
• Lists, with your first 3 right in the share sheet
• Home-screen widget with thumbnails, list switching and quick add
• Automatic titles and preview images
• Done with a link you opened from the app? Delete it in one tap, with Undo
• Automatic local backups, restore and bookmarks export
• Pro: unlimited links and import, one-time purchase
```

**Play category** [12 chars, no limit]

> Productivity

**Play tags (pick the nearest 5 from the Console list)** [66 chars, no limit] (tag names not verified against Play's predefined list)

> Productivity | Bookmark manager | Read later | Widgets | Organizer

### Data safety answers

| Question | Answer |
|---|---|
| Does your app collect or share any of the required user data types? | **No** |
| Resulting label | "No data collected", "No data shared" |
| Encryption in transit / data deletion request | Not asked when nothing is collected (verify in Console) |
| Privacy policy URL | https://linksoon.app/privacy (planned; must be live and match the in-app link at submission) |
| Ads | No |
| Target audience | 13+ (not directed at children) |

**Rationale (keep with the Console submission).** Play defines collection as data the app transmits off the device to the developer or a third party. Linksoon has no analytics, crash-reporting or ad SDK and no server; its dependencies are AndroidX, Room, WorkManager, Glance, OkHttp, Coil, Ksoup, Play Billing and Play In-App Review.

- **Page fetches.** Titles and preview images are fetched by the phone directly from the page the user saved, as a direct result of the user saving it. Nothing goes to the developer, and the site receives only a standard web request.
- **Android Auto Backup.** An operating-system service that runs under the user's own Google account, which the user controls and the developer cannot access. It is Google's backup of the device, not collection by the app.
- **Google Play Billing.** Payment data is handled by Google Play, which Play's Data safety guidance excludes. The app receives only purchase status and verifies it on the device.
- **Google Play In-App Review.** Google's In-App Review documentation now lists the rating and review text as data collected and publicly shared, and says the developer decides how to answer. Decision: answer "No". The dialog is Google Play's own UI, the app never receives the rating or the text, and the review is posted by the user to Google Play under the user's own Play profile. If a Console query or a policy update says otherwise, add "App activity: other user-generated content (shared)" and update the privacy policy in the same release.

**Content declarations to complete in Console:** ads (No), target audience (13+), news app (No), government app (No), financial features (No), content rating questionnaire. Set up the `pro_unlock` product with its price before the closed test, because the paywall shows the live price.

## Apple App Store listing (later)

Every claim assumes an iOS build with the same features: share extension, a widget with list switching that opens links in one tap, a "Done with it?" prompt with Delete and Undo, swipe to delete, folder backups via Files, no SDKs. Verify each claim against the iOS build before submission. No platform names, no prices, no competitor names anywhere in Apple metadata. App Privacy answer: "Data Not Collected", if the iOS build has the same no-SDK design.

**Apple name** [30 / 30 chars, hard limit, fits]

> Linksoon: Save Links for Later

**Apple subtitle** [29 / 30 chars, hard limit, fits]

> Read-later list with a widget

**Apple keyword field** [99 / 100 bytes, hard limit, bytes, fits] (no spaces; no words from the name or subtitle; no competitor names)

> bookmark,manager,url,article,recipe,video,watch,reading,queue,inbox,organize,private,offline,import

**Apple promotional text** [167 / 170 chars, hard limit, fits] (editable without a release)

> Save links from any app into a short list on your Home Screen. Open them in a tap, clear them in a tap. No account. No servers of ours. Your links live on your iPhone.

**Apple description** [2321 / 4000 chars, hard limit, fits]

```text
Linksoon is a short read-later list for links. Save from any app, see what's next on your Home Screen, and clear links in the app with one tap when you're done. No account. No servers of ours. Your links live on your iPhone. The free plan keeps 3 links at a time; Pro removes the limit with a one-time In-App Purchase.

SAVE FROM ANY APP
Tap Share in Safari, a video app, a social app or any app with a Share button, and pick Linksoon. Choose a list, or let it land in Inbox.

WHAT'S NEXT, ON YOUR HOME SCREEN
The widget shows the queue for your current list, with titles and thumbnails. Tap a row to open the link. Switch lists, add a link, and pick Comfortable or Compact rows and a Solid, Tinted or Glass look.

A QUEUE, NOT A GRAVEYARD
Read-later lists tend to grow until nobody opens them. Linksoon keeps yours short and in sight. Open a link from inside the app and, when you come back, it asks if you're done with it. One tap deletes it, with Undo if you change your mind. You can also swipe a link away.

LISTS FOR EVERYTHING
Make lists for articles, videos to watch later, recipes, shopping, trips or work. Search across everything and sort by your own order, newest, oldest, title or site.

TITLES AND PREVIEWS, AUTOMATICALLY
Linksoon fills in each page's title and preview image. Your iPhone reads them straight from the page; no server of ours sits in between.

PRIVATE BY DESIGN
• No account or sign-up
• No analytics, no ads, no tracking
• No servers of ours: your links are never sent to the developer
• Your links live on your iPhone

BACKUPS YOU CAN READ
Automatic backups go to a folder you pick in Files, as JSON and plain text. Restore whenever you need to, or export a bookmarks HTML file that any browser can import.

BRING YOUR LINKS (PRO)
Import from export files of other read-later and bookmark apps, CSV files, browser bookmarks HTML and plain-text lists.

FREE AND PRO
The free plan keeps 3 links at a time, across all your lists, with no time limit. Save more and they wait in a Waiting list (up to 50). When a slot frees up, Linksoon offers to add the next one.
Pro is a one-time In-App Purchase, not a subscription. It removes the limit, unlocks import and places every waiting link in its list.

MAKE IT YOURS
Pick an accent color or the true-black dark theme.

Save it, see it, finish it.
```
