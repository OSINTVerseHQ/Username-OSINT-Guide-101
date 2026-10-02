# Username Permutations

Enumeration without permutation only finds the handle you already knew. The useful account is the 2009 LiveJournal they forgot, or the Instagram that dropped the underscore.

Use this with Phase 2 of the [Username OSINT Guide 101](../README.md).

---

## Infer the rule first

If you already have two handles, write the transformation:

```text
GitHub:   jane_kay
Xbox:     JaneKay94
Rule?:    underscore on “serious” sites, CamelCase + year on games
```

Generate from the **rule**, not from a generic wordlist. A generic list is how you drown in `mike87` collisions.

Keep two columns: **confirmed** vs **speculative**. Speculative variants never inherit High confidence.

---

## Separator family

From core `janekay` / `jane` + `kay`:

```text
janekay
jane_kay
jane.kay
jane-kay
jane kay          (search only — many sites reject spaces)
```

Sherlock can expand separators in one token: `jane{?}kay`.

---

## Name-order and initials

```text
janekay
kayjane
jkay
j_kay
jane_k
jk
kjane
```

Reversed order is common when the original script is not Latin (family name first).

---

## Affixes

Taken-name and “brand” padding:

```text
thejanekay
imjanekay
itsjanekay
realjanekay
janekayofficial
janekay_real
janekayhq
janekaytv
janekayyt
xxjanekayxx
_jane_kay_
```

`official` / `real` is also how **impersonators** brand themselves. Check account age.

---

## Numeric tails

```text
janekay1 … janekay9
janekay01
janekay94          (two-digit year)
janekay1994
janekay_94
janekay420
janekay69
janekay123
janekaykay         (doubled token)
```

Years are Medium uniqueness at best. `johnsmith1990` is a crowd.

---

## Leet and lazy typing

```text
jan3kay
j4nekay
jane_k4y
jaynekay           (phonetic)
janekai
jnekay             (dropped vowel)
```

Use these when you have already seen the subject play this way. Do not leet-blast a professional LinkedIn slug.

---

## Platform truncations

Build the truncated form **on purpose**. People hit the cap and stop at the same character.

| Cap | Example from `mothwing-caliper-maps` |
| --- | --- |
| 15 (X) | `mothwingcaliper` (hyphens often dropped first) |
| 20 (Reddit) | `mothwing-caliper-map` |
| 24 (TikTok) | `mothwing-caliper-maps` |
| 30 (Instagram) | usually fits |

Also generate the “drop the hyphen, then crop” version. That is the usual panic move when a signup form rejects the original.

---

## Email and phone cores

The local-part of an email is a username candidate:

```text
jane.kay@acme.com  →  jane.kay, janekay, jkay
```

A phone’s last 4 or 10 digits sometimes become a tail (`jane_2671`). Rare, but cheap to test once.

Then run the [Email](https://github.com/osintverse/Email-OSINT-Guide-101) or [Phone](https://github.com/osintverse/Phone-Number-OSINT-Guide-101) guide on the identifier itself — do not stop at the derived handle.

---

## Locale and era tags

```text
janekay_uk
janekayleeds
janekay_dev
janekay_osu
janekay2k11
```

Pull tags from *known* bios (city, game, graduation). Do not invent a country suffix for every ISO code.

---

## Maigret permute

When you have a first and last name, not a handle:

```bash
maigret jane kay --permute
```

Treat every generated hit as **speculative** until Phase 6.

---

## Batch discipline

1. Cap the first batch at ~15–25 variants.
2. Enumerate.
3. Open the *interesting* hits.
4. Infer a better rule.
5. Only then grow the list.

A 400-line permutation file is not thoroughness. It is how uniqueness dies.

---

## Related pages

- [Main username OSINT guide](../README.md)
- [Tools](tools.md)
- [Dorks](dorks.md)
