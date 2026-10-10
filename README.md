# Veriscan NG

**A link and message risk checker built for the scam patterns targeting Nigerians right now.**

Veriscan NG lets someone paste a suspicious link or message and get back a risk verdict built specifically around Nigerian scam formats like fake BVN verification alerts, CBN refund/palliative texts, bank/Opay/Moniepoint "account blocked" warnings, and fake NYSC messages, alongside general phishing indicators.

> 🚧 **Status: early preview.** The current build runs local keyword-pattern matching in the browser only. Live scanning (domain age, SSL/TLS validation, URL reputation via Safe Browsing/VirusTotal) is in active development see [Roadmap](#roadmap).

---

## Why this exists

Nigeria's digital economy is growing fast, but security awareness for ordinary users and small businesses hasn't kept pace. Nigeria faces a 90.6% cybersecurity workforce gap (NITDA, 2026), and most existing security tooling targets enterprises, not the people actually receiving scam texts every day.

Veriscan NG is a small, focused attempt to close part of that gap: a free, simple tool anyone can use to sanity-check a suspicious link or message before clicking or responding.

## Current features (v0 — demo mode)

- Paste a URL or raw message text
- Pattern-matches against known Nigerian scam formats (BVN, CBN refund, bank-blocked alerts, fake NYSC, lottery/prize scams)
- Flags URL shorteners as a caution signal
- Returns a risk verdict (Low Risk / Suspicious / High Risk) with plain-language reasons
- Zero backend, zero data collection everything runs client-side in the browser

## Roadmap

- [ ] WHOIS-based domain age checks
- [ ] SSL/TLS certificate validation
- [ ] URL reputation lookup (Google Safe Browsing + VirusTotal)
- [ ] Redirect chain analysis
- [ ] Weighted scoring engine combining all signals
- [ ] FastAPI backend to replace client-side demo logic
- [ ] SME security health check mode (website headers, exposed admin panels)
- [ ] Public API for other Nigerian developers/apps

## Tech stack

- **Now:** plain HTML/CSS/JS, no build step, no dependencies
- **Planned backend:** Python + FastAPI
- **Planned checks:** WHOIS API, Google Safe Browsing API, VirusTotal API (all free-tier)

## Running locally

No install needed — it's a single static file.

```bash
git clone https://github.com/umarfaruq-sec/veriscan-ng.git
cd veriscan-ng
open index.html   # or just double-click it
```

## Deployment

Deployed via GitHub Pages directly from this repo. No build process `index.html` is served as-is.

## Disclaimer

This is a student built security awareness tool, not a substitute for official verification. If a message claims to be from your bank, NYSC, CBN, or any government body, always verify through their official channels directly never through a link in the message itself.

## Author

Built by **Abdulkareem Umar Faruq** — Cyber Security student, Nigeria.
Part of a broader portfolio of security tooling see [network-vulnerability-scanner](https://github.com/umarfaruq-sec/network-vulnerability-scanner) for a related project.

## License

MIT
