# Launch checklist — one-time go-live steps

Everything here is done **by you** (Adam) in the GitHub UI and at Namecheap.
Do them roughly in order.

## 1. Push the site to GitHub

```bash
git add -A
git commit -m "Set up academicpages site with custom landing page"
git push origin master
```

## 2. Turn on GitHub Actions deployment

Repo → **Settings → Pages → Build and deployment**:

- **Source:** select **GitHub Actions** (not "Deploy from a branch").

The `Build and deploy` workflow will run on every push to `master`. Watch it under
the repo's **Actions** tab; the first run takes a couple of minutes.

## 3. Point the domain at GitHub (Namecheap)

Log in to Namecheap → **Domain List → Manage** `cardozaresearch.com` →
**Advanced DNS** tab.

**Delete** any default records Namecheap added (a `CNAME` for `www` pointing at
`parkingpage`, and any `URL Redirect Record`).

**Add these records** (Host Records section):

| Type        | Host | Value                    | TTL       |
|-------------|------|--------------------------|-----------|
| A Record    | `@`  | `185.199.108.153`        | Automatic |
| A Record    | `@`  | `185.199.109.153`        | Automatic |
| A Record    | `@`  | `185.199.110.153`        | Automatic |
| A Record    | `@`  | `185.199.111.153`        | Automatic |
| CNAME Record| `www`| `cardoza2.github.io.`    | Automatic |

(Optional, for IPv6 — add these `AAAA` records with Host `@` too:
`2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`.)

Make sure the domain's **Nameservers** are set to **Namecheap BasicDNS** (the
default) so these records take effect.

DNS can take anywhere from a few minutes to a few hours to propagate.

## 4. Confirm the custom domain + HTTPS on GitHub

The repo already contains a [`CNAME`](CNAME) file (`cardozaresearch.com`), so
GitHub should auto-detect the custom domain under **Settings → Pages**.

- Verify **Custom domain** shows `cardozaresearch.com` with a green check.
- Once the check passes, tick **Enforce HTTPS** (the TLS cert may take a few
  minutes to provision after DNS resolves).

## 5. Verify

- https://cardozaresearch.com loads the landing page.
- https://www.cardozaresearch.com redirects to the apex.
- Nav links (Research, Publications, Projects, CV, Resources) all work.

---

### Check DNS from the terminal

```bash
dig +short cardozaresearch.com          # should list the four 185.199.108-111.153 IPs
dig +short www.cardozaresearch.com       # should show cardoza2.github.io
```
