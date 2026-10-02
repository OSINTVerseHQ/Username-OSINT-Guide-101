# Username OSINT Investigation Checklist

Print this or copy it into your case file. One sheet per *core* handle. Variants stay on this sheet. A second unrelated cluster gets a new sheet.

Back to the [Username OSINT Guide 101](../README.md).

---

## Case header

```text
Case / ticket: ________________________________
Analyst: _____________________________________
Lawful basis / authorization: _________________
Date opened (UTC): ____________________________
Handle as seen: ______________________________
Normalized key: ______________________________
Source platform / URL: _______________________
Display name (if any): _______________________
Uniqueness:  [ ] High  [ ] Medium  [ ] Low  [ ] collision-by-design
Do-not-do list: no login, no impersonation, no reset, no contact
```

---

## Phase 1 — Collect

- [ ] Copied the handle exactly (`@`, case, homoglyphs)
- [ ] Display name stored separately
- [ ] Real-name / email-local-part candidates labeled as hypotheses
- [ ] Uniqueness scored with a one-line reason

---

## Phase 2 — Permutations

Confirmed handles:

```text
1.
2.
```

Speculative variants (do not inherit confidence):

```text
1.
2.
3.
4.
5.
```

- [ ] Separators (`.` `_` `-` none)
- [ ] Numeric tails / years
- [ ] Affixes (`real`, `official`, `the`, `im`)
- [ ] Leet / dropped vowels
- [ ] Name-order swaps
- [ ] Platform truncations (X 15, Reddit 20, TikTok 24)

---

## Phase 3 — Enumeration

- [ ] WhatsMyName (or skipped)
- [ ] Sherlock — raw output saved
- [ ] Maigret — raw + HTML if used
- [ ] Important sites checked **by hand** (GitHub, Reddit, X, Instagram, TikTok…)
- [ ] “Not found” not treated as proof

| Tool | Handle | “Found” count | Output file |
| --- | --- | --- | --- |
| | | | |

---

## Phase 4 — Search and archives

- [ ] Quoted Google / Bing / Yandex on confirmed handles
- [ ] `site:` GitHub, Reddit, relevant communities
- [ ] `inurl:` and forum signatures
- [ ] Wayback on every load-bearing URL
- [ ] archive.today if Wayback misses
- [ ] Reddit `.json` / other structured endpoints as needed

| URL | What it shows | Date seen | Archive | Cluster |
| --- | --- | --- | --- | --- |
| | | | | |

---

## Phase 5 — Profile cards

Fill one card per load-bearing account.

```text
Platform:
URL:
Archive:
Handle / display name:
Created / last active:
User ID:
Avatar file:
Bio (verbatim):
Outbound links:
Language / location:
Notes:
```

- [ ] Avatars reverse-imaged (Lens, Yandex, TinEye)

---

## Phase 6 — De-confliction

| Account A | Account B | Shared non-handle signals | Splitters | Merge? | Confidence |
| --- | --- | --- | --- | --- | --- |
| | | | | Y/N | |

- [ ] At least one cluster explicitly **rejected** or marked unresolved
- [ ] What would disprove the main merge: _______________________

---

## Phase 7 — Pivots

| Identifier | Value | Next guide / action | New sheet? |
| --- | --- | --- | --- |
| Email | | Email OSINT Guide 101 | |
| Phone | | Phone OSINT Guide 101 | |
| Domain | | WHOIS / CT / email guide | |
| SteamID / snowflake / other | | Platform playbook | |

---

## Phase 8 — Report

- [ ] Every claimed link has sources
- [ ] Every claimed link has a confidence score
- [ ] Rejected collisions are written down
- [ ] No password or impersonation attempt in the file
- [ ] Next step is explicit (or “stop”)

### Claim log

| Claim | Sources | Confidence | Caveat |
| --- | --- | --- | --- |
| | | High / Med / Low | |

### Analyst conclusion

```text




```

---

## Evidence pack

- [ ] Screenshots with UTC timestamps
- [ ] SingleFile / WARC of key profiles
- [ ] Wayback / archive.today links
- [ ] Sherlock / Maigret raw output
- [ ] Avatar files
- [ ] This checklist, filled

Retain according to your organization’s policy. Delete what you have no lawful basis to keep.
