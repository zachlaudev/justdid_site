# justdid_site

Static marketing / legal site for the **JustDid** app, served at
[justdidapp.com](https://justdidapp.com).

## Pages

- `index.html` — landing
- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Service
- `support.html` — Support

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy (GitHub Pages)

1. Push this repo to GitHub.
2. **Settings → Pages**: source = `Deploy from a branch`, branch = `main`,
   folder = `/ (root)`.
3. **Settings → Pages → Custom domain**: enter `justdidapp.com` and save.
   (The `CNAME` file in the repo will keep this set on every deploy.)
4. At your DNS provider, add records pointing `justdidapp.com` to GitHub Pages:
   - `A` records on the apex (`@`) to:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - `CNAME` record on `www` pointing to `<your-github-username>.github.io`
5. Back in **Settings → Pages**, enable **Enforce HTTPS** once the cert
   provisions (can take ~15 min after DNS resolves).

