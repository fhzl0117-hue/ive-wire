# IVE Wire

An independent, unofficial English-language fan hub for IVE/DIVE — news translation, release reviews, official-only video curation, a live tour countdown, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by Starship Entertainment or the members of IVE.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/), [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/), [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/), [aespa Wire](https://fhzl0117-hue.github.io/aespa-wire/), [ENHYPEN Wire](https://fhzl0117-hue.github.io/enhypen-wire/), [SEVENTEEN Wire](https://fhzl0117-hue.github.io/seventeen-wire/), [TWICE Wire](https://fhzl0117-hue.github.io/twice-wire/), [LE SSERAFIM Wire](https://fhzl0117-hue.github.io/lesserafim-wire/), [TXT Wire](https://fhzl0117-hue.github.io/txt-wire/), [(G)I-DLE Wire](https://fhzl0117-hue.github.io/gidle-wire/), [RIIZE Wire](https://fhzl0117-hue.github.io/riize-wire/), and [ZEROBASEONE Wire](https://fhzl0117-hue.github.io/zerobaseone-wire/) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | A live timer that counts down to confirmed future dates, or counts up ("time since") for past ones — auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores (affiliate links go here) |

## A note on accuracy: REVIVE+'s double title track

REVIVE+ is IVE's second full-length album (released February 23, 2026) and, unusually, carries two title tracks rather than one: pre-released "BANG BANG" and the cinematic "BLACKHOLE," which later took first place on Show Champion (March 4, 2026). The album also includes a solo track for each of the group's six members — Gaeul, Yujin, Rei, Wonyoung, Liz, and Leeseo, who remain the full lineup as of this build. One allkpop/Tokyo Dome recap referred to "five members" receiving individual spotlight moments at a June 2026 show; this was checked against multiple 2026-dated member-profile sources and appears to be an article-summary artifact rather than a lineup change — IVE is still a six-member group. Do not add a lineup-change note to this site without a dedicated, corroborated source.

## A note on accuracy: the Show What I Am World Tour

IVE's second world tour, Show What I Am, kicked off at Seoul's KSPO Dome on October 31, 2025, in support of the *Ive Empathy* / *Ive Secret* EPs and, later, REVIVE+. A second Tokyo Dome run followed on June 24, 2026 (roughly 95,000 fans, front-page coverage in Japan's five major sports newspapers). As of this build, Hong Kong (AsiaWorld-Arena, Sept 4–6) and Taipei (Taipei Arena, Sept 11–13) are the next confirmed stops — both still upcoming at time of writing, so the Signal desk's Hong Kong row is a genuine "time left" countdown rather than "time since." Update it to "time since" once that date passes, and don't add further tour stops without a source.

## manifest.json — K-Wire Network auto-discovery

This repo carries a `manifest.json` at its root so it's automatically picked up by [K-Wire Network](https://fhzl0117-hue.github.io/), the directory hub for the whole "Wire" series. No manual edit to the hub repo is needed — its page fetches this file on every visit and lists this site automatically.

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or signal-desk date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown/elapsed timers work if you need to change their logic — the Signal desk timer auto-detects whether a `data-target` date is in the future (shows "time left") or the past (shows "time since"), so it works either way without further edits.

**Before adding new dates or news items,** verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding any new YouTube embed,** verify it against the official channel using the oEmbed check: fetch `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=<ID>&format=json` and confirm `author_name` matches "STARSHIP" on channel `@STARSHIP_official` (IVE's MVs are uploaded through their label's shared channel rather than a group-specific one — the same pattern used for RIIZE and SMTOWN) — a search result titled "Official Music Video" is not proof by itself. During this build, a video titled "IVE 아이브 'BLACKHOLE' MV | Official Music Video 2026" (id cSuBY2S6TmA) was checked and turned out to be uploaded by an unrelated third-party channel ("DeepPulse Studio") despite the official-looking title — it was rejected. Both embeds actually used in this build ("BLACKHOLE" and "After LIKE") were verified against @STARSHIP_official.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
