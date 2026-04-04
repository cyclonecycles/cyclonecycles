# Cyclone Cycles Website

Single-page static site for Cyclone Cycles, 4215 Bellaire Blvd, Houston TX 77025.

## Files

```
index.html        ← The entire website (HTML + CSS embedded)
photos/           ← Drop shop photos here (see photos/README.md)
README.md         ← This file
```

---

## Deploy to Netlify (drag-and-drop, no account setup needed)

1. Go to **https://app.netlify.com/drop**
2. Drag the entire `cyclonecycles/` folder onto the page
3. Netlify gives you a live URL instantly (e.g. `https://random-name-123.netlify.app`)
4. Done — share that URL with Mark

To redeploy after edits: drag the folder again to the same Netlify site (or use the Netlify UI).

### To use a custom domain (e.g. cyclonecycles.com)
1. Create a free Netlify account at netlify.com
2. Go to your site → **Domain settings** → **Add custom domain**
3. Point the domain's DNS to Netlify's nameservers (they walk you through it)
4. This requires access to the domain registrar — see "Domain mystery" below

---

## One-time setup tasks

### Google Maps embed (fix the map)
The iframe in `index.html` uses a placeholder coordinate. To get the exact embed:
1. Go to maps.google.com and search `4215 Bellaire Blvd Houston TX 77025`
2. Click **Share** → **Embed a map** → copy the `<iframe>` code
3. Replace the `<iframe>` in the `#location` section of `index.html`

### Google Review link (fix the CTA)
The "Leave a Google Review" button uses `PLACE_ID_HERE` as a placeholder.
1. Go to: https://developers.google.com/maps/documentation/javascript/examples/places-placeid-finder
2. Search for **Cyclone Cycles** at the new address
3. Copy the Place ID (looks like `ChIJ...`)
4. In `index.html`, replace `PLACE_ID_HERE` with the real ID

### Domain mystery — who controls cyclonecycles.com?
Run this in your terminal to find the registrar:
```
whois cyclonecycles.com
```
Look for the `Registrar:` and `Registrant Email:` lines.
- If it's GoDaddy / Namecheap / Network Solutions, Mark can likely recover it via email
- The contact email on Nextdoor was `donate@opencart.com` — suggests someone scaffolded
  the site from an OpenCart template years ago and may have forgotten about it
- Once Mark has registrar access, point the domain to Netlify (free SSL included)

---

## To update content later

Everything is in `index.html` — it's one file with embedded CSS. Search for:
- `4215 Bellaire` — address references
- `(713) 668-2104` — phone
- `10am–7pm` — hours
- `#sunday` — Sunday events section
- `#gallery` — photo gallery section (see photos/README.md)
