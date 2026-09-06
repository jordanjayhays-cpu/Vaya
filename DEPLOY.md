# Vaya — Go-Live Checklist

The site is in this repo (`index.html` = Vaya News home, `manila.html` = Vaya Manila).
Two steps to make it live at **vayanews.com**:

## 1. Turn on GitHub Pages (~30 sec)
Repo → **Settings → Pages**
- Source: **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- **Save**

GitHub will show the live URL and auto-detect the `vayanews.com` custom domain (from the `CNAME` file already in this repo). Then tick **Enforce HTTPS** once it's available.

## 2. Point the domain (at your registrar — Squarespace domain settings)
Add these DNS records for **vayanews.com**:

**4 A records** (apex domain → GitHub Pages):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**1 CNAME record** (for the www version):
```
www  →  jordanjayhays-cpu.github.io
```

Give DNS ~10–60 min to propagate. Then **vayanews.com** loads the site.

## Updating the site later
Just push to `main` — GitHub Pages redeploys automatically. (Claude edits + pushes; nothing manual.)

## The pages
- `/` → Vaya News (home + ecosystem)
- `/manila.html` → Vaya Manila (films, ecosystem map, Starter Kit)
- Add `vayavibes.com` later as a redirect to the same site if you want.
