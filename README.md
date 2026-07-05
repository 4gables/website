# 4gables.com

Public marketing site for **4gables**, served by GitHub Pages.

This is a **separate public repo** on purpose — the product code
(`4gables/matrix`) stays **private**, and GitHub Pages on a private repo needs a
paid plan. A standalone public repo keeps the site free and the code closed.

## Files
- `index.html` — single self-contained page (inline CSS, theme-aware, no deps).
- `CNAME` — binds the custom domain `4gables.com` (GitHub reads this on deploy).

## Publish (one-time)
1. Create the public repo `4gables/website` (or `4gables.github.io`).
2. Commit these files to `main`.
3. Repo **Settings → Pages** → *Deploy from a branch* → `main` / `/ (root)`.
4. Under Pages → **Custom domain**, enter `4gables.com`, then tick
   **Enforce HTTPS** once the cert is issued.
5. **DNS at the registrar** for `4gables.com`:
   - Apex `@` → four **A** records: `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
     (optionally the matching AAAA: `2606:50c0:8000::153` … `8003::153`).
   - `www` → **CNAME** `4gables.github.io`.
   - Add the TXT verification record GitHub shows under Pages → custom domain.

Propagation + cert issuance can take up to ~24h; usually much faster.
