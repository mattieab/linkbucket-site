# Store and site text-asset rules for Link Bucket (as of Oct 2026)

Labels used below: **[POLICY]** = hard rule from Google/Apple policy or a field limit enforced by the console; **[GUIDANCE]** = official recommendation, not enforced; **[BEST PRACTICE]** = third-party/industry convention.

## Google Play: field limits, banned words and claims, categories, Data safety

### Takeaway
Play enforces 30 / 80 / 4000 characters for title / short / full description and 500 characters for release notes. Title, icon and developer name may not contain emojis, ALL CAPS (unless it's the brand), "free", "no ads", rankings or price/promotion text. Descriptions may not include unattributed testimonials, comparisons to competing apps, or misleading references to other apps. "Pocket alternative" is a comparison/competitor reference and risky. A plain factual "import from Pocket export file" is the only defensible form, and only if the feature actually exists. A local-only app that only does ephemeral network fetches can truthfully declare "No data collected / No data shared", but it still needs a privacy policy.

### Cited Findings

**Field limits**
- [POLICY] App name: 30-character limit, one localized name per language. Short description: 80 characters. Full description: 4000 characters. "Character limits apply to both full-width and half-width characters." — [Play Console Help: Create and set up your app / store listing](https://support.google.com/googleplay/android-developer/answer/9859152)
- [POLICY] "Repetitive or irrelevant use of keywords in the app name, description, or promotional description can create an unpleasant user experience and result in an app being suspended on Google Play." — [same](https://support.google.com/googleplay/android-developer/answer/9859152)
- [POLICY] "What's new in this release" (release notes): 500 characters per language. Uploads via fastlane fail if over. — [deku.posstree.com](https://deku.posstree.com/en/share/google-play/release-notes-character-limit/), [releasepad.io](https://www.releasepad.io/blog/mobile-app-release-notes/) (secondary sources; the Play Console UI enforces this limit, but I did not find an official Help page stating it)
- [POLICY] Feature graphic: 1024 x 500 px, JPEG or 24-bit PNG. Icon: 512 x 512 px, 32-bit PNG with alpha, max 1024 KB. Screenshots: minimum 2 and maximum 8 per device type. 1080 px or more recommended for large-format recommendation eligibility. Preview video: YouTube, public or unlisted, ads off, embeddable. — [Play Console Help: Add preview assets](https://support.google.com/googleplay/android-developer/answer/9866151)

**Metadata policy (Developer Program Policy, "Metadata")**
- [POLICY] Title ≤30 chars. "Don't use emojis, emoticons, or repeated special characters in these metadata elements. Avoid ALL CAPS unless it is part of your brand name." This applies to title, icon and developer name. — [Play Policy: Metadata](https://support.google.com/googleplay/android-developer/answer/9898842)
- [POLICY] The following are prohibited in title, icon and developer name:
  - Store-performance indicators: "'App of the year,' '#1,' 'Best of Play 20XX,' 'Popular,' award icons"
  - Price/promotion: "'10% off,' '$50 cash back,' 'free for limited time only'"
  
  — [Play Policy: Metadata](https://support.google.com/googleplay/android-developer/answer/9898842)
- [POLICY] Descriptions: "Unattributed or anonymous user testimonials" are prohibited. So are competitor data comparisons, unauthorized celebrity/brand references, and "excessive length, detail, improper formatting, or repetition". — [Play Policy: Metadata](https://support.google.com/googleplay/android-developer/answer/9898842)
- [POLICY] Icons must not use misleading symbols, e.g. a new-message dot when there are no new messages. — [same](https://support.google.com/googleplay/android-developer/answer/9898842)
- [GUIDANCE/POLICY] Store listing best-practice page:
  - Title must not include "Free," "No Ads," or performance claims like "#1" / "App of the year".
  - Title must not falsely imply a connection to other companies.
  - Short description: "Summarize clearly: Explain your app's core purpose"; no pricing info or ranking claims.
  - Full description: "provide an attributed or clear source for any endorsements"; no repetitive keyword blocks.
  - "Don't include misleading or irrelevant references to other apps or products"; do not compare to competing applications.
  
  — [Play Console Help: Store listing best practices / metadata guidelines](https://support.google.com/googleplay/android-developer/answer/13393723)
- [GUIDANCE] Screenshots:
  - "Taglines should not take up more than 20% of the image."
  - Avoid calls to action ("Download now"), ranking claims and small unreadable fonts.
  - Must depict the actual app experience. Avoid device frames, people holding devices, and third-party trademarked content.
  - Provide localized versions.
  
  — [Add preview assets](https://support.google.com/googleplay/android-developer/answer/9866151); [13393723](https://support.google.com/googleplay/android-developer/answer/13393723)
- [GUIDANCE] Feature graphic: keep the tagline minimal. Avoid "Best"/"#1", promotional language and outdated content. Keep key elements centered so edges can be cropped. — [Add preview assets](https://support.google.com/googleplay/android-developer/answer/9866151)
- [GUIDANCE] Preview video: show core features in the first 10 seconds, keep it under 30 seconds for autoplay, and make 80%+ of it actual UX. — [same](https://support.google.com/googleplay/android-developer/answer/9866151)

**Promotional content (LiveOps)**
- [POLICY] Promotional content taglines: 80 characters. Descriptions: 500 characters. Content must describe the specific event or offer, with no generic CTA text. — [AppTweak LiveOps guide](https://www.apptweak.com/en/aso-blog/what-are-google-play-liveops-best-practices-examples); [Google promotional content guidelines PDF](https://services.google.com/fh/files/helpcenter/google_play_promotional_content_guidelines.pdf)
- [POLICY] Promotional content is part of the "Premium Growth Tools" and only available to apps meeting performance/eligibility criteria. A brand-new app is unlikely to qualify at launch. — [same](https://www.apptweak.com/en/aso-blog/what-are-google-play-liveops-best-practices-examples); [Play content quality guidelines](https://support.google.com/googleplay/android-developer/answer/12929944?hl=en)

**Categories and tags**
- [POLICY] Category descriptions:
  - Productivity: "Notepad, to-do list, keyboard, printing, calendar, backup, calculator, conversion".
  - Tools: "Tools for Android devices".
  - News & Magazines: "Newspapers, news aggregators, magazines". Apps in the News category need a special declaration and must meet extra requirements.
  
  — [Play Console Help: categories and tags](https://support.google.com/googleplay/android-developer/answer/9859673)
- [POLICY] Up to 5 tags. "Choose tags most obviously relevant"; avoid tangential features. Change tags only on significant functionality changes. Optional accessibility tags exist. Changes take up to 24 hours. — [same](https://support.google.com/googleplay/android-developer/answer/9859673)

**Pocket context**
- Pocket went read-only on July 8, 2025. Mozilla disabled export and deleted all account data on Nov 12, 2025; the API third-party importers used is offline. — [Stashr blog](https://stashr.me/blog/pocket-shutdown-alternatives); [tabmark.dev migration guide](https://tabmark.dev/blog/pocket-migration-guide/); [AlternativeTo news](https://alternativeto.net/news/2025/5/after-17-years-mozilla-is-shutting-down-the-popular-bookmarking-tool-pocket-and-fakespot) (secondary sources; consistent with each other)

**Data safety**
- [POLICY] "'Collect' means transmitting data from your app off a user's device." "User data accessed by your app that is only processed locally on the user's device and not sent off device does not need to be disclosed." — [Play Console Help: Data safety](https://support.google.com/googleplay/android-developer/answer/10787469)
- [POLICY] Ephemeral exception: "accessing and using it while the data is only stored in memory and retained for no longer than necessary to service the specific request in real-time" need not be disclosed. Google's example is a weather app sending location to fetch conditions. — [same](https://support.google.com/googleplay/android-developer/answer/10787469)
- [POLICY] Google Play Billing: if your app never accesses the payment info and the payment service collects it directly under its own terms, you don't declare that financial data. — [same](https://support.google.com/googleplay/android-developer/answer/10787469)
- [POLICY] "Even developers with apps that do not collect any user data must complete this form and provide a link to their privacy policy." Libraries/SDKs that transmit data count as collection, regardless of destination. — [same](https://support.google.com/googleplay/android-developer/answer/10787469)

### Inferences
- **Title.** "Link Bucket" is 11 chars. A descriptor like "Link Bucket: Save Links Later" (29) fits. Do not use "Free", "No Ads", "Best", "#1", emojis or caps-lock words. "Pocket" in the title would imply a relationship or trade on a trademark; avoid it.
- **"Pocket alternative".** In the short or full description this is a direct competitor reference/comparison, which the metadata guidelines say not to make. Rejection risk is moderate; keep it to the website.
  - "Import links from a Pocket export (CSV/HTML)" is a factual feature statement. It is lower risk if the feature exists, but since Pocket exports ended Nov 2025, only users who saved a file benefit. "Import from a bookmarks/HTML/CSV file" is safer and broader.
  - This is a judgment call, not an explicit rule; Google's text targets "misleading or irrelevant" references.
- **Pricing words.** "Free plan of 3 links" and "one-time Pro purchase" are fine in the full description as a factual explanation of the model; Google bans price/promotional claims in title/icon/dev name. Avoid "free" in the short description too, given the "no pricing info" guidance. Never use "lifetime deal" or "% off" language.
- **Category.** Productivity fits best: read-later/bookmarking sits beside notepad and to-do. Tools is defined as device utilities. News & Magazines triggers the News declaration requirements and fits aggregators, not personal link savers.
- **Tags.** Pick up to 5 that match Play's predefined list. In Console, check for options such as bookmarks, read later, productivity and note-taking.
- **Data safety.** Two conditions:
  - When the app fetches a URL's HTML to extract OG title/image, the requested URL goes to the third-party site the user chose. It is not sent to the developer, and nothing is retained server-side by the developer. That is arguably not "collection" by the developer, and at most ephemeral. If no analytics/crash SDK (e.g. Firebase Crashlytics) is included, "No data collected / No data shared" is defensible.
  - Autobackup: if it uses Android Auto Backup to the user's Google Drive, that is Google's OS service, not the developer's. Cloud backup to a developer server would change the answer.

### Gaps
- I found no official Help page text giving the 500-char release-notes limit; it comes from secondary sources and is enforced in the Console UI.
- I could not retrieve the full current list of Play's predefined tag names; check it in the Console.
- I found no Google statement that explicitly allows or forbids naming a defunct competitor like Pocket for import purposes.
- Developer name: there is no separate char limit in sources fetched, and the metadata rules on emojis/caps/"free" apply.

## Apple App Store: field limits, competitor names, privacy labels

### Takeaway
Limits:

| Field | Limit |
|---|---|
| Name | 30 |
| Subtitle | 30 |
| Keywords | 100, comma-separated |
| Promotional text | 170, editable without a release; doesn't affect search |
| Description | 4000 (per Apple's long-standing App Store Connect limit) |
| What's New | 4000 (per secondary source) |

Competitor app names and unauthorized trademarks are explicitly banned from keywords and metadata. Prices and mentions of other mobile platforms (e.g. "Android") are banned from metadata. If nothing leaves the device, the app qualifies for "Data Not Collected".

### Cited Findings
- [POLICY] Name 30, subtitle 30, keywords 100 total (comma-separated), promotional text 170, IAP name 35, IAP description 55. Up to 10 screenshots, up to 3 app previews of 30 s each. — [Apple: Creating your product page](https://developer.apple.com/app-store/product-page/)
- [POLICY] Keywords: don't include plurals of words already present, category names, the word "app", duplicates, "unauthorized trademarked terms or celebrity names", or "competing app names". — [same](https://developer.apple.com/app-store/product-page/)
- [GUIDANCE] Promotional text "does NOT affect search ranking". Use it for time-limited news. — [same](https://developer.apple.com/app-store/product-page/)
- [GUIDANCE] Description: the first sentence is most critical. No keyword stuffing, no specific prices, and put accolades at the end. What's New: list changes by importance. — [same](https://developer.apple.com/app-store/product-page/)
- [POLICY] Guideline 2.3.7: "don't try to pack any of your metadata with trademarked terms, popular app names, pricing information, or other irrelevant phrases… App names must be limited to 30 characters… subtitles… should not include inappropriate content, reference other apps, or make unverifiable product claims." — [App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- [POLICY] 2.3.10: "don't include names, icons, or imagery of other mobile platforms or alternative app marketplaces in your app or metadata". So no "Also on Android" in the iOS listing. — [same](https://developer.apple.com/app-store/review/guidelines/)
- [POLICY] 5.2.1: don't use third-party trademarks without permission; avoid "misleading, false, or copycat representations, names, or metadata". — [same](https://developer.apple.com/app-store/review/guidelines/)
- [POLICY] 5.1.1: a privacy policy link is required both in App Store Connect and in-app. The policy must:
  - identify what data is collected, how, and all uses;
  - confirm that third parties provide equal protection;
  - explain retention/deletion and how to revoke consent or request deletion.
  
  — [same](https://developer.apple.com/app-store/review/guidelines/)
- [POLICY] Privacy label: "Collect" means "transmitting data off the device in a way that allows you and/or your third-party partners to access it for a period longer than what is necessary to service the transmitted request in real time". Data processed only on-device is not collected. Purchases via Apple's payment system where you never see payment info are not collected. A privacy policy URL is mandatory. — [Apple: App privacy details](https://developer.apple.com/app-store/app-privacy-details/)

### Inferences
- Do not put "pocket" in the keywords field. Apple's guidance names competing app names explicitly, and Apple "may modify inappropriate keywords".
- The iOS description must drop any "Android"/"Google Play" mention and any price, e.g. "one-time purchase" is OK but "$4.99" is not.
- The subtitle should be a functional phrase without "best" or unverifiable claims (e.g. "Save links, read them later" = 27).

### Gaps
- The 4000-char description and What's New limits were not on the fetched Apple page. They are long-standing App Store Connect limits; verify in ASC at iOS launch.

## One-page website SEO: title/meta, headings, structured data, OG, badge, CWV

### Takeaway
Google sets no character limit on titles or meta descriptions; it truncates by device width. The practical targets are about 50–60 chars (~600 px) for the title and 150–160 chars (~920 px desktop) for the description.

FAQ rich results are gone:
- deprecated Sept 2023 for non-gov/health sites;
- removed from Search on May 7, 2026;
- docs removed June 15, 2026.

FAQPage markup gives no SERP benefit now, so an FAQ section is for users and on-page content only.

SoftwareApplication rich results require a rating or review. A new app with no reviews won't qualify, and self-written reviews violate guidelines.

### Cited Findings
- [GUIDANCE] Titles have no technical limit but are "truncated in Google Search results as needed, typically to fit the device width". Be descriptive and concise, avoid "Home", and avoid keyword stuffing. Put the site name at the start or end with a delimiter. — [Google Search Central: Title links](https://developers.google.com/search/docs/appearance/title-link)
- [GUIDANCE] Meta description: "no limit on how long a meta description can be, but the snippet is truncated… typically to fit the device width". It should be unique and descriptive, with no keyword strings. Google often generates snippets from page content instead. — [Google Search Central: Snippets](https://developers.google.com/search/docs/appearance/snippet)
- [BEST PRACTICE] Title ~580–600 px ≈ 50–60 chars. Meta description ~920 px desktop ≈ 155–160 chars. Truncation is by pixels, not characters. — [Screaming Frog pixel-width post](https://www.screamingfrog.co.uk/blog/page-title-meta-description-lengths-by-pixel-width/); [xmlschemata.org](https://xmlschemata.org/title-tag-length-characters-vs-pixels/)
- [POLICY] FAQ rich result: "This feature will no longer appear in Google Search starting May 7, 2026" (notice added May 8, 2026). On June 15, 2026 the docs were removed because the feature "is no longer shown in Google Search results". Before that it was limited to "well-known, authoritative government and health websites" (since 2023). — [Search Central FAQPage doc](https://developers.google.com/search/docs/appearance/structured-data/faqpage); [Search Central updates log](https://developers.google.com/search/updates)
- Other rich-result types were also retired in 2025–26: practice problem (Jan 2026), and course info, estimated salary, learning video, special announcement and vehicle listing (Sept 2025). — [Search Central updates](https://developers.google.com/search/updates)
- [POLICY] SoftwareApplication rich result requirements:
  - Required: `name`, `offers.price` (0 if free; add `priceCurrency`), and one of `aggregateRating` or `review`.
  - Recommended: `applicationCategory` (e.g. `UtilitiesApplication`, `BusinessApplication`) and `operatingSystem`.
  - `MobileApplication` is a supported subtype.
  - "Google does not guarantee" display.
  
  — [Search Central: Software app](https://developers.google.com/search/docs/appearance/structured-data/software-app)
- [POLICY] Google Play badge:
  - Don't modify color, proportions or spacing.
  - Make it equal or larger in size than other store badges.
  - Link it to your app's Play detail page or your developer page.
  - Include the attribution line "Google Play and the Google Play logo are trademarks of Google LLC."
  - The search summary of the Partner Marketing Hub says creative referring to the Google Play trademark must be approved by Google's brand team.
  - The badge text is "Get it on Google Play" (generated per language at the badge generator).
  
  — [Google Play badges page](http://play.google.com/intl/en_us/badges/); [Partner Marketing Hub: Badge guidelines](https://partnermarketinghub.withgoogle.com/brands/google-play/visual-identity/badge-guidelines/?folder=86642); [Partner Marketing Hub: Legal requirements](https://partnermarketinghub.withgoogle.com/brands/google-play/legal-and-trademarks/legal-requirements/). The direct fetch of the hub returned 404, so these details come from search-result summaries and should be verified on the hub before launch.
- [POLICY/GUIDANCE] Core Web Vitals "good" thresholds at the 75th percentile, mobile and desktop separately: LCP ≤ 2.5 s, INP ≤ 200 ms, CLS ≤ 0.1. — [web.dev: Web Vitals](https://web.dev/articles/vitals)

### Inferences
**Title tag:** e.g. "Link Bucket – Save links to read later on Android" (≈49 chars).

**Meta description:** a ~150-char benefit statement mentioning no account, local-only and the widget.

**Headings:**
- One H1 with the value proposition.
- H2 per section: features, widget, privacy, pricing, FAQ.
- Anchor links (#features, #pricing, #faq) give in-page navigation and can earn sitelink-style jump links. This is a convention, not an official rule.

**Structured data:**
- Use `MobileApplication` with name, operatingSystem "Android", applicationCategory, offers price 0, and a link to the Play URL.
- Expect no rich result until genuine ratings exist. Do not fabricate `aggregateRating`.
- FAQPage JSON-LD is harmless but pointless for Google SERPs now. Keep the visible FAQ for users and for answer engines/LLMs.

**Other:**
- hreflang: not needed for a single English page. Add it only if localized pages ship.
- Open Graph/Twitter: og:title ≈ same as the title tag, og:description ≈ 1–2 sentences, and a 1200×630 og:image. These sizes are a common convention; I did not fetch an official spec.
- The privacy policy should be its own URL (e.g. /privacy) with "Privacy Policy" in its title, to satisfy Play's labeling rule below.

### Gaps
- I did not fetch official Open Graph (ogp.me) or X card docs. The 1200×630 and summary_large_image conventions are unverified here.
- I found no authoritative 2026 data on the content length needed for a single page to rank. Google publishes no word-count guidance.
- The exact current badge minimum size and clear-space rules are unverified (hub page 404 on fetch).

## Landing-page copy structure for indie app one-pagers

### Takeaway
Use this order: hero (value proposition readable in ~5 s, app visual, store badge), feature sections with screenshots, pricing/model statement, FAQ (accordion when there are more than 5 questions), and a final CTA. GoodLinks, a well-regarded indie read-later app, uses no testimonials or press quotes and states its one-time-purchase model right in the hero subhead.

### Cited Findings
- [BEST PRACTICE] Hero: a visitor should grasp the value proposition within ~5 seconds. The hero has the headline, an app visual and the primary CTA. — [Framer: landing page best practices](https://www.framer.com/blog/landing-page-best-practices/)
- [BEST PRACTICE] Screenshots, mockups and demo video reduce uncertainty. Friction-reducing microcopy near CTAs ("No credit card required") reduces hesitation. — [Framer](https://www.framer.com/blog/landing-page-best-practices/); [Webflow app landing pages](https://webflow.com/blog/app-landing-page)
- [BEST PRACTICE] Use an accordion FAQ when there are more than 5 questions of varying length, to keep the page scannable and handle objections. — [SeedProd FAQ examples](https://www.seedprod.com/best-faq-pages/); [Landingi FAQ](https://landingi.com/landing-page/faq/)
- GoodLinks.app (fetched Oct 2026):
  - Title "GoodLinks — The Better Way to Save and Read Articles".
  - Hero H1 "Save. Read. Anywhere." with subhead "Buy once, use forever with one year of feature upgrades."
  - CTA is the App Store badge.
  - Feature sections in order: Clean reading, Highlight, Save from anywhere, Organized, Summarize, Actions, Customizable, Themes, then an "And More" grid.
  - No testimonials or press quotes. FAQ is a footer link. Pricing amount is not on the page.
  
  — [goodlinks.app](https://goodlinks.app/)

### Inferences
Suggested Link Bucket order:
1. Hero: H1 value prop, subhead with "no account, stays on your phone", Play badge, phone screenshot.
2. "How it works" in 3 steps: share → bucket → widget.
3. Feature sections: buckets, widget, previews, backup.
4. Privacy section. This doubles as social proof in place of reviews ("no account, no tracking, no server").
5. Pricing: free for 3 links, Pro is a one-time purchase. On the website, unlike in store metadata, stating the price is fine.
6. FAQ.
7. Final CTA.
8. Footer: privacy policy link and the Google Play trademark line.

"Social proof without reviews" options: a founder note or "made by" line, an open changelog, and "as featured" lines only if true.

### Gaps
- I did not fetch Reeder, Things or Instapaper pages; only GoodLinks was verified.
- I found no data on conversion lift for these sections specific to indie Android apps.

## Privacy policy essentials (local-only app, Play Billing, metadata fetching)

### Takeaway
Play and Apple both require a public privacy policy even when nothing is collected. On Play it must be:
- an HTML page (no PDF) at an active, non-geofenced, non-editable URL;
- labelled "Privacy Policy";
- naming the developer entity or app, with a contact point;
- stating data types handled, sharing, security and retention/deletion.

Apple adds requirements to disclose third-party protection and how a user can revoke consent or request deletion.

### Cited Findings
- [POLICY] The Play policy must disclose:
  - "how your app accesses, collects, uses, and shares user data";
  - "Developer information and a privacy point of contact or a mechanism to submit inquiries";
  - the types of personal/sensitive data and any parties it's shared with;
  - "Secure data handling procedures";
  - "The developer's data retention and deletion policy".
  
  — [Play User Data policy](https://support.google.com/googleplay/android-developer/answer/10144311)
- [POLICY] Play also requires:
  - "an active, publicly accessible and non-geofenced URL (no PDFs)", "non-editable";
  - "Clear labeling as a privacy policy (for example, listed as 'privacy policy' in title)";
  - the policy appears both in Play Console and in-app;
  - "The entity… named in the app's Google Play store listing must appear in the privacy policy or the app must be named in the privacy policy";
  - "Apps that do not access any personal and sensitive user data must still submit a privacy policy."
  
  — [same](https://support.google.com/googleplay/android-developer/answer/10144311)
- [POLICY] Apple 5.1.1 requirements are listed in the App Store section above. — [App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- [POLICY] Play Billing payment data handled by Google is not the developer's collection. — [Data safety help](https://support.google.com/googleplay/android-developer/answer/10787469)

### Inferences
The Link Bucket policy should state:
1. Who: developer name as on Play, the app name, and a contact email.
2. Data stored on the device: saved URLs, titles, notes, buckets. These are stored locally only, never sent to the developer, and there is no account.
3. Network requests: when you save a link, the app connects directly to that website to fetch its title, description and preview image. That site sees your IP address and a standard request, as with any browser visit, and its own policy applies. Nothing is routed through developer servers. Also say whether a custom User-Agent is sent.
4. Purchases: processed by Google Play Billing. The developer receives no payment details, only purchase status/entitlement. Google's privacy policy applies.
5. Backups: say exactly how autobackup works. For Android Auto Backup to the user's Google account, data goes to the user's Google Drive under Google's terms. For local file export, say so.
6. No analytics, ads or tracking SDKs. This must be true; check the dependencies, including Play Services and any crash reporting.
7. Retention and deletion: data stays until the user deletes it or uninstalls. Explain how to delete backups.
8. Children: not directed at children.
9. Changes to the policy and an effective date.
10. Security: data is kept in app-private storage.

### Gaps
- GDPR/CCPA-specific wording was not researched here. For a no-collection app the obligations are minimal, but the controller identity and contact are still needed.
- Whether Play Billing's on-device purchase token check counts as collection was not addressed explicitly beyond the payment-info exemption.
