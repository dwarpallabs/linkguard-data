# LinkGuard data

Scam websites confirmed by [LinkGuard](https://github.com/dwarpallabs/linkguard), the open-source Android app that checks links before they open, for people in India.

A new file is published every day as a [release](https://github.com/dwarpallabs/linkguard-data/releases). Banks, researchers and other apps are welcome to use it.

## Using the data

Always the newest files:

```
https://github.com/dwarpallabs/linkguard-data/releases/latest/download/confirmed.txt
https://github.com/dwarpallabs/linkguard-data/releases/latest/download/latest.json
```

| File | What it is |
| --- | --- |
| `confirmed.txt` | One website per line (`example.com`), sorted. Lines starting with `#` are comments. |
| `latest.json` | The `sha256` of `confirmed.txt`, the number of websites, when it was made, the delay and the expiry. Check the hash before you use the file. |
| `CHANGELOG.md` | The websites added and removed each day, newest first. |
| `reports-summary.json` | How many LinkGuard users reported a scam each week, per brand the scam pretended to be (for example SBI or HDFC Bank, or `other`). Counts only, never websites. |

Please credit the data like this:

> Scam website data: LinkGuard by Dwarpal Labs (ODbL 1.0), including PhishDestroy (MIT).

## What is in it

- Websites that Dwarpal Labs confirmed as scams: added by a maintainer, or confirmed after LinkGuard users reported them.
- The [PhishDestroy](https://github.com/phishdestroy/destroylist) list of phishing and scam websites that are currently online.

**Delay and expiry.** A website appears 48 hours after it was confirmed, as with other public scam feeds, and drops out 30 days after it was last confirmed (or last seen in PhishDestroy's list). A warned website is already known to scammers, so the delay costs little and avoids publishing mistakes.

## What is never in it

- Community reports that nobody confirmed. LinkGuard counts these to show a soft "reported by N people" warning in the app, and keeps them private.
- The links people open. LinkGuard never stores or sends them. Reports send only the website name.
- Websites on LinkGuard's list of well-known safe websites, and websites a maintainer cleared.
- URLhaus data. LinkGuard uses it, but its terms don't clearly allow passing it on, so get it from [abuse.ch](https://urlhaus.abuse.ch) directly.

## A website is listed by mistake

Open an [issue](https://github.com/dwarpallabs/linkguard-data/issues) or write to support@dwarpallabs.com with the website name. Wrongly listed websites are removed from the next day's file.

## Licence

The database is licensed under the [Open Database License (ODbL) 1.0](LICENSE). Entries from PhishDestroy are also covered by its MIT licence; see [NOTICE](NOTICE).
