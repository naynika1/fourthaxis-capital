# Fourth Axis Capital — website

This is a simple static website designed to be hosted for free on GitHub Pages.

## Files
- `index.html` — the website
- `CNAME` — tells GitHub Pages to use `fourthaxis.capital`
- `fourth-axis-logo-dark-bg.png` — logo to use on dark backgrounds
- `fourth-axis-logo-light-bg.png` — logo to use on light backgrounds
- `README.md` — setup instructions

The page automatically uses the correct logo depending on the viewer's light/dark color scheme.

## Publish with GitHub Pages

1. Create or sign in to a GitHub account.
2. Create a **new public repository**. A simple name such as `fourthaxis-capital` is fine.
3. Upload all files in this folder to the repository root.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Choose branch **main** and folder **/(root)**, then save.
7. In the **Custom domain** field, enter `fourthaxis.capital`.
8. After the DNS change below has propagated, enable **Enforce HTTPS**.

## GoDaddy DNS change

Important: do not delete or alter MX, TXT, SRV, or CNAME records used by your email.

For the root domain (`@`), remove the GoDaddy website-builder A record(s) and add these four A records:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

For `www`, add a CNAME after you know your GitHub username:

| Type | Name | Value |
|---|---|---|
| CNAME | www | YOUR-GITHUB-USERNAME.github.io |

## Editing the site later

You can edit `index.html` directly in GitHub for free:
1. Open `index.html`.
2. Click the pencil/edit icon.
3. Change the text or layout.
4. Commit the change.

GitHub Pages will republish the updated page automatically.

## Notes

- The site defaults to a very restrained institutional look.
- The logo automatically switches between the dark-background and light-background versions.
