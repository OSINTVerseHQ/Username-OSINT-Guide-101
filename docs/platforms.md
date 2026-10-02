# Username Platform Playbooks

A “found” URL is not the end. Each platform leaks different stable IDs and different lies.

Use this in Phase 5 of the [Username OSINT Guide 101](../README.md).

---

## GitHub / GitLab

**Why it matters.** Developers reuse handles and leak emails in commits.

**Do this**

- Profile: display name, bio, blog, Twitter/X field, company, location, avatar
- Pinned repos and README “about me”
- `https://github.com/<user>.gpg` and `.keys` — emails in UIDs
- Public commits: author email (or `noreply`)
- [osgint](https://github.com/hippiiee/osgint) for username ↔ email
- Numeric user ID in API (`https://api.github.com/users/<user>`) survives a rename
- Gists and old pages on Wayback

A GitHub handle plus a personal domain is often enough to start the [email guide](https://github.com/osintverse/Email-OSINT-Guide-101).

---

## Reddit

**Why it matters.** Long post history is a pattern-of-life source.

**Do this**

- `https://www.reddit.com/user/<name>/` and the same URL + `.json`
- `created_utc` is exact
- Subreddit mix is a fingerprint (city + hobby + profession)
- Old usernames sometimes appear in quoted logs and mod notes
- Deleted users: Wayback the user page and individual post URLs

Do not treat a one-off comment in a huge default sub as identity.

---

## X (Twitter)

**Why it matters.** Handles change; snowflake IDs do not.

**Do this**

- Bio, location, website, creation month
- Numeric status/user IDs encode time (snowflake)
- Search the handle in quotes even after a rename — old media and news keep it
- Wayback `twitter.com/<handle>` and `x.com/<handle>`
- Archived-tweet tools only recover what the Internet Archive actually grabbed

Impersonators love `real` / `official` suffixes here. Check the creation date.

---

## Instagram / TikTok / YouTube

**Why it matters.** Photos and video are merge keys — and stolen constantly.

**Do this**

- Handle vs display name vs “Name” field
- Link-in-bio (Linktree, Carrd) — gold
- Reverse-image the avatar *and* a distinctive post
- Story highlights and tagged map pins (if public)
- YouTube: `/@handle` and old `/user/` and `/c/` URLs; About email if shown

A fashion shop that grabbed a recycled handle is the classic false merge. Check language and product shots.

---

## Telegram

**Why it matters.** The **username** is public; the phone is not.

**Do this**

- `https://t.me/<username>`
- Bio, display name, public channels/groups they own
- Usernames change; forwarded-message footers sometimes keep the old one

Phone discovery is a different, ToS-sensitive problem. See the [phone guide](https://github.com/osintverse/Phone-Number-OSINT-Guide-101/blob/main/docs/messaging.md). Do not bulk-sync contacts.

---

## Discord

**Why it matters.** People assume Discord is invisible to username OSINT. The *username* is not a public profile URL.

**Do this**

- You will not get a reliable `discord.com/users/name` page from Sherlock
- Look for the handle in server lists, GitHub READMEs, “join my Discord,” screenshots
- Discriminators (`name#1234`) are legacy; new usernames are unique strings
- Snowflake IDs (if you have one from a message screenshot) decode to creation time
- Treat a Discord hit on WhatsMyName as **especially** in need of a manual check

---

## Steam / Xbox / PSN / Riot / Battle.net

**Why it matters.** Gaming tags often predate the “serious” internet identity.

**Do this**

- Steam vanity URL → SteamID64 (profile page or Web API). Pivot on the **ID**
- Third-party stats, trade, and ban sites index SteamID64
- Xbox / PSN appear in Reddit flairs and “add me” threads
- Same numeric tail across Xbox and Steam is a Medium signal, not High

---

## LinkedIn

**Why it matters.** The public slug is a username (`/in/janekay`).

**Do this**

- Prefer `site:linkedin.com/in "Jane Kay"` over logging in as yourself
- The slug may be `jane-kay-b12a3` — the random tail is not uniqueness
- Do not view the profile while logged in as you

---

## Keybase, Linktree, Carrd, About.me

**Why it matters.** These exist to *announce* other accounts. That is the subject doing your Phase 6 for you.

Still verify each linked account. Compromised Linktrees get rewritten.

---

## Forums, old web, and “long tail”

WhatsMyName’s value is the weird site: a 2012 bike forum, a regional classifieds, a fan wiki.

Open those. The signature block (“Steam: X / email: Y”) is why you ran the tool.

---

## Related pages

- [Main username OSINT guide](../README.md)
- [Messaging / phone](https://github.com/osintverse/Phone-Number-OSINT-Guide-101/blob/main/docs/messaging.md)
- [Email OSINT](https://github.com/osintverse/Email-OSINT-Guide-101)
- [FAQ](faq.md)
