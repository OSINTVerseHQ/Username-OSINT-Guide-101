# Username OSINT FAQ

Short answers. The long version is the [Username OSINT Guide 101](../README.md).

---

## What is username OSINT?

Username OSINT is the use of publicly available information to find where a handle exists, decide which of those accounts are the same person, and harvest other identifiers. It is not “Sherlock said found, so it is them.”

---

## How do I find someone from a username?

Score how unique the handle is, generate a short permutation list, enumerate with WhatsMyName / Sherlock / Maigret, then **open** the important profiles and merge only on non-handle evidence (photo, Linktree, email, posting rhythm). Use the [8-phase workflow](../README.md#the-8-phase-username-osint-workflow).

---

## Sherlock vs Maigret vs WhatsMyName?

- **WhatsMyName** — browser, fast, good detection rules
- **Sherlock** — CLI baseline, easy to script
- **Maigret** — more sites, parses the page, can recurse on extracted IDs

Run more than one on a real case. None of them attribute identity. Details: [tools](tools.md).

---

## Does a matching username mean it is the same person?

No. Common handles collide. Platforms recycle names. Impersonators copy strings and avatars. You need two independent signals that are *not* the username. See [confidence scoring](../README.md#confidence-scoring).

---

## How do I find alternate usernames?

Infer the subject’s transformation rule, then generate separators, years, affixes, leet, and platform-length truncations. Do not run a 400-line fantasy list. Cookbook: [permutations](permutations.md).

---

## Can I find a deleted account?

Often the content, rarely the live login. Wayback CDX, archive.today, Reddit JSON, and old news mentions. What was never public or never archived is gone.

---

## Is username OSINT legal?

Collecting public profiles is generally lawful. Building a dossier is personal-data processing. Logging in as them, impersonating them, or using this for stalking / FCRA screening is not. This is not legal advice.

---

## Why did Sherlock say found but the page is empty?

Soft 404s, login walls, rate limits, or a dead module. Believe the browser. Important sites: check by hand.

---

## What about Discord?

Discord usernames are not a public profile URL the way GitHub is. Enumerators are noisy here. Hunt the handle in READMEs, “join my server” links, and screenshots. Snowflake IDs (if you have one) give creation time.

---

## How do I pivot from a username to an email?

GitHub commits and GPG, PGP keyservers, bios, Linktree, Gravatar if you already have a candidate address. Then run the [Email OSINT Guide](https://github.com/osintverse/Email-OSINT-Guide-101).

---

## Can I use this for recruiting or tenant screening?

No. Use a licensed consumer reporting agency.

---

## How do I hide my own handles?

Different cores for different lives (not just a new underscore), different avatars, no shared Linktree, private GitHub email, assume 2009 is still in Wayback. See [Reduce your own username OSINT surface](../README.md#reduce-your-own-username-osint-surface).

---

## Related pages

- [Username OSINT Guide 101](../README.md)
- [Tools](tools.md)
- [Platform playbooks](platforms.md)
- [Checklist](checklist.md)
