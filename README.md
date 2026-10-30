# Kalori

A tiny, single-file personal tracker: daily calories and steps, body measurements
(weight, waist, chest, neck, biceps, thigh, trouser front measure) and clothing sizes.
Plain HTML/CSS/JS in `index.html`, no build step, installable as a PWA and usable offline.

**Your data stays in your browser.** Everything is stored in `localStorage` on the
device you use; there is no server, account or sync. Clearing site data or switching
browsers/devices means starting empty, so take backups.

**Backups:** *Ayar* tab → *JSON indir* downloads `kalori-yedek-YYYY-MM-DD.json`.
Restore with *Dosyadan içe aktar*, or copy/paste the JSON through the text box.
Imports are validated; an invalid file leaves your current data untouched.

**GitHub Pages:** push to `main`, then in the repository go to
*Settings → Pages → Source: GitHub Actions*. The workflow in
`.github/workflows/pages.yml` deploys the repository root. On a phone, open the
site and use “Add to Home Screen”.

**Local run:** `python3 -m http.server` and open http://localhost:8000
(the service worker needs http(s), not `file://`).

## Türkçe

Kalori; günlük kalori ve adım, vücut ölçüleri ve kıyafet bedenlerini takip eden,
tek dosyalık bir web uygulamasıdır. Tüm veriler yalnızca kullandığın tarayıcıda
(localStorage) tutulur, hiçbir sunucuya gönderilmez. Bu yüzden Ayar sekmesinden
düzenli olarak “JSON indir” ile yedek al; geri yüklemek için “Dosyadan içe aktar”ı
ya da kopyala/yapıştır kutusunu kullan. GitHub Pages için depoda
Settings → Pages → Source: GitHub Actions seçmen yeterli; telefonda siteyi açıp
“Ana ekrana ekle” dersen uygulama gibi ve çevrimdışı çalışır.

## License

MIT
