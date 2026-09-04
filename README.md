# porchpopcollective-apex

GitHub Pages site that forwards the bare domain `porchpopcollective.com` to `https://www.porchpopcollective.com`, preserving path and query.

Why this exists: the domain is registered at Wix, which does not allow changing name servers and allows only an `A` record at the root; the site itself runs on Railway, which provides only `CNAME` targets. GitHub Pages publishes fixed A-record IPs and free HTTPS, so it can hold the root while `www` points at Railway.

DNS at Wix (Manage DNS Records):

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | the Railway custom-domain target for `www.porchpopcollective.com` |

Repo settings → Pages → Source: Deploy from a branch, `main` / `(root)`; custom domain `porchpopcollective.com`; Enforce HTTPS once the certificate is issued.

Phase 1: transfer the registration to Cloudflare Registrar (after Wix's 60-day lock) and point the root at Railway with CNAME flattening; then this repo retires.
