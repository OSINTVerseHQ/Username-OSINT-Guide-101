# Username OSINT Tools

A practical directory of **username OSINT tools** used in the [Username OSINT Guide 101](../README.md). Every row answers a specific investigative question.

Tools die. Site-check modules die faster. If a row is stale, [open an issue](https://github.com/osintverse/Username-OSINT-Guide-101/issues).

**Rules**

- A “found” is a lead. Open the URL.
- Prefer local tools when the handle is sensitive (hosted checkers log queries).
- Keep volume low. Record the exact command and timestamp.

---

## Quick picker

| If you need… | Start with |
| --- | --- |
| Results in a browser, now | [WhatsMyName](https://whatsmyname.app) |
| A scriptable baseline | Sherlock |
| Bios, IDs, recursion | Maigret |
| Username *and* email | Blackbird, user-scanner |
| Deleted profiles | Wayback CDX, archive.today |
| A face | Reverse image, not another enumerator |
| One paid pane of glass | Your desk’s licensed platform |

---

## Enumerators

| Tool | Type | Cost | What it is actually for |
| --- | --- | --- | --- |
| [WhatsMyName](https://whatsmyname.app) / [dataset](https://github.com/WebBreacher/WhatsMyName) | Web + JSON | Free | Community detection rules; many other tools sit on this list |
| [Sherlock](https://github.com/sherlock-project/sherlock) | CLI | Free | Fast 400+ site sweep; `{?}` separator fuzz; CSV/XLSX |
| [Maigret](https://github.com/soxoj/maigret) | CLI | Free | 3000+ sites, profile parsing, `--parse`, `--permute`, HTML/PDF |
| [Blackbird](https://github.com/p1ngul1n0/blackbird) | CLI | Free | Username + email; WhatsMyName-backed; PDF/CSV |
| [user-scanner](https://github.com/kaifcodec/user-scanner) | CLI | Free | Combined email/username; bulk lists |
| [socid-extractor](https://github.com/soxoj/socid-extractor) | Library | Free | Pulls stable IDs and fields from a profile page (Maigret uses this idea) |
| Namechk | Web | Free | Visual skim. Not authoritative |

```bash
pipx install sherlock-project
sherlock jane_kay94 janekay94 --csv

pipx install maigret
maigret jane_kay94 --html
maigret --parse https://github.com/jane_kay94
maigret john doe --permute
```

Sherlock’s `{?}` expands `_` / `-` / `.` in one token: `sherlock jane{?}kay94`.

---

## Search and archives

| Tool | Type | Cost | What it is actually for |
| --- | --- | --- | --- |
| Google / Bing / Yandex / DuckDuckGo | Web | Free | Mentions, signatures, PDFs. See [dorks](dorks.md) |
| [Wayback Machine](https://web.archive.org) + CDX | Web / API | Free | Deleted and renamed profile paths |
| [archive.today](https://archive.ph) | Web | Free | Pages Wayback cannot render |
| Reddit `…/user/name.json` | Official JSON | Free | `created_utc`, posts, without a scraper debate |
| twayback-class X archives | CLI | Free | Deleted tweets *if they were archived* |

---

## Images, graphs, caseware

| Tool | Type | Cost | What it is actually for |
| --- | --- | --- | --- |
| Google Lens / Yandex / [TinEye](https://tineye.com) | Web | Free | Avatar reuse; TinEye oldest-first |
| Maltego CE | Desktop | Free / paid | Link analysis *after* you corroborated nodes |
| Hunchly | Browser | Paid | Automatic evidence capture |
| SingleFile | Extension | Free | Save the profile you are about to lose |
| The [checklist](checklist.md) | Paper | Free | Claim log |

---

## Identity pivots (not username tools)

| Tool / guide | When |
| --- | --- |
| [Email OSINT Guide 101](https://github.com/osintverse/Email-OSINT-Guide-101) | Commit author, PGP, bio mailto |
| [Phone OSINT Guide 101](https://github.com/osintverse/Phone-Number-OSINT-Guide-101) | WhatsApp-in-bio, classifieds |
| [GHunt](https://github.com/mxrch/GHunt) | You already have a Google-related email |
| [osgint](https://github.com/hippiiee/osgint) | GitHub username ↔ commit email |

---

## What we deliberately left out

- “Try this list of passwords with the username”
- Impersonation / catfish kits
- Mass followers-scrape malware
- Dating-app stalkerware
- Unofficial Instagram/TikTok private-API dumps

If a product’s demo is “we log into their account,” close the tab.

---

## Related pages

- [Main username OSINT guide](../README.md)
- [Permutations](permutations.md)
- [Platform playbooks](platforms.md)
- [FAQ](faq.md)
