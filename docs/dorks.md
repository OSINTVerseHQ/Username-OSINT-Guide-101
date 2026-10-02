# Google Dorks for Username OSINT

Enumerators find current profile URLs. **Google dorks** find the comment, the PDF, the signature, and the old blog the tools never saw.

Use these as part of the [Username OSINT Guide 101](../README.md). Replace `jane_kay94` with the handle. Always run the serious [permutations](permutations.md) too.

---

## Rules

- Quote the handle. Unquoted search splits on `_`.
- Search with and without `@`.
- Search the **display name** as a separate quoted string.
- Repeat on Bing and Yandex.
- Archive useful hits the same day.

---

## Core

```text
"jane_kay94"
"@jane_kay94"
"jane kay94"
inurl:jane_kay94
intitle:"jane_kay94"
intext:"jane_kay94"
```

---

## Platforms

```text
"jane_kay94" site:github.com
"jane_kay94" site:gitlab.com OR site:bitbucket.org
"jane_kay94" site:reddit.com
"jane_kay94" site:x.com OR site:twitter.com
"jane_kay94" site:instagram.com
"jane_kay94" site:tiktok.com
"jane_kay94" site:youtube.com
"jane_kay94" site:linkedin.com
"jane_kay94" site:steamcommunity.com OR site:steam.com
"jane_kay94" site:discord.com OR site:discord.gg
"jane_kay94" site:t.me OR site:telegram.me
"jane_kay94" site:hackernews.com OR site:news.ycombinator.com
"jane_kay94" site:stackoverflow.com
"jane_kay94" site:keybase.io
```

---

## Documents and signatures

```text
"jane_kay94" filetype:pdf
"jane_kay94" filetype:txt OR filetype:md
"jane_kay94" (resume OR cv OR "curriculum vitae")
"jane_kay94" ("signed," OR signature OR "regards" OR "— ")
"jane_kay94" (steam OR xbox OR psn OR battlenet OR riot)
```

Forum signatures and “add me on…” lines are how gaming tags leak into civilian life.

---

## Link-in-bio and domains

```text
"jane_kay94" (linktr.ee OR carrd.co OR about.me OR bio.link)
"jane_kay94" ("my github" OR "my twitter" OR "follow me")
inurl:jane_kay94 site:linktr.ee
```

---

## Pastes and leaks

```text
"jane_kay94" site:pastebin.com OR site:justpaste.it
"jane_kay94" (password OR combo OR dump OR leaked)
```

Record the URL and the service name. Do not use any password you see.

---

## Homoglyph and lookalike pass

```text
"jane_kay94" OR "jane_kay9l" OR "jane_kay9I"
"jаne_kay94"
```

Use sparingly, when the source was an image or a phishing lure.

---

## Operator cheat sheet

| Operator | Meaning |
| --- | --- |
| `"..."` | Exact string |
| `@handle` | Often how people write it in posts |
| `site:` | One platform |
| `inurl:` | Handle in the path (profile-like URLs) |
| `filetype:` | PDFs, dumps |
| `OR` | Variants in one query |

---

## Related pages

- [Main username OSINT guide](../README.md)
- [Permutations](permutations.md)
- [Checklist](checklist.md)
