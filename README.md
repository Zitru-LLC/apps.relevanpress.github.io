# Zitru LLC — apps site

Static landing pages for the Zitru LLC apps, plus the shared Terms of Service and
Privacy Policy that every app links to. No build step — plain HTML/CSS, serve the
repo root from GitHub Pages (Settings → Pages → deploy from branch, root).

```
index.html        all apps
hot-gossip.html   com.saucy.hotgossip
techly-news.html  com.relevanpress.techly
atomo-news.html   com.relevanpress.atomo
anynews.html      com.relevanpress.anynews  (unreleased — see below)
terms.html        shared, all apps
privacy.html      shared, all apps
style.css         one stylesheet; each app page sets --brand / --brand-dark inline
assets/           icons from the Android flavors, screenshots from the store listings
```

Preview locally: `python3 -m http.server 8000`

## Notes

- **Store links.** Every page links to both stores. Verified live: Hot Gossip
  (`id6450760456`), Techly News (`id6466743266`), Atomo News (`id6466743335`) and
  all three Play listings. **AnyNews is not published yet** — its Play listing and
  `id6792874694` both 404 today; the links are pre-wired to the expected
  destinations and start working the moment it ships.
- **Store badges** are plain CSS buttons — Google and Apple no longer allow
  hotlinking their badge images. Swap in the official artwork if brand compliance
  is needed.
- **Legal copy** is carried over from `atomo.relevanpress.com/news/tos/`, generalised
  from one app to all four and re-attributed to Zitru LLC. The "laws of Europe"
  governing-law clause is verbatim from the original and worth a lawyer's look.
- No `CNAME` is committed — add one if this should serve a custom domain.
