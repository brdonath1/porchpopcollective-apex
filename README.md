# porchpopcollective-apex — retired

This former GitHub Pages redirector was retired on September 18, 2026. Its Pages
site is unpublished, and the obsolete redirect pages and `CNAME` file have been
removed. The repository is retained as a read-only historical archive.

The live routing verified at retirement is:

- `porchpopcollective.com` uses redirect.pizza, which returns a permanent HTTP 301
  redirect to `https://www.porchpopcollective.com`, preserving the path and query.
- `www.porchpopcollective.com` serves the application on Railway.
- Application development and operations belong in
  [brdonath1/porch-pop-collective](https://github.com/brdonath1/porch-pop-collective).

Both authoritative Wix DNS servers and the Cloudflare and Google public resolvers
agreed on this routing. No current application code or workflow depended on this
repository. The public domain's DNS records and its working redirect were preserved.

Do not re-enable GitHub Pages or point the domain at GitHub Pages using the old
setup instructions. Any future routing change needs a fresh review of the live
DNS and customer-facing behavior. The original implementation remains in Git
history for reference; it is not the current production configuration.
