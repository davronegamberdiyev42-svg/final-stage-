# IELTS Boost Stage 56 — O‘rnatish qo‘llanmasi

## GitHub Pages

1. `IELTS_Boost_Stage56_UX_Accessibility_Performance.zip` faylini extract qil.
2. ZIP ichidagi **barcha fayl va papkalarni** repository root’iga joyla; ZIP’ni o‘zini repository ichiga joylama.
3. `index.html`, `manifest.webmanifest`, `sw.js`, `assets/`, `data/`, `audio/`, `icons/` root tartibini saqla.
4. GitHub → Settings → Pages → Deploy from a branch → `main` → `/(root)` ni tanla.
5. HTTPS sahifani och. Stage 56 dastlab faqat 672 daily core so‘z bilan yuklanadi; to‘liq 19K vocabulary indeksi Vocabulary Lab ochilganda so‘raladi.

## Stage 56 yangiliklari

- `data/app-data.json` 15,201,551 baytdan 5,938,780 baytga tushdi.
- 19,000 ta vocabulary yozuvi `data/vocabulary-index.json` ichida to‘liq saqlanadi.
- Vocabulary Lab ochilganda to‘liq indeks olinadi; vocabulary-only o‘yinlar indeks tayyor bo‘lguncha kutadi.
- Service Worker katta indeksni install paytida yuklamaydi, talab bo‘yicha cache qiladi.
- Keyboard skip link, focus ring, dynamic accessible names, reduced motion va forced-colors qo‘shildi.

## Full-device backup

Stage 55 backup manager saqlangan. Settings → Full-device Backup & Restore orqali COMPLETE backup export qil. Backup ichida progress va ikkala IndexedDB’dagi audio bo‘lishi mumkin. Faylni xavfsiz va shaxsiy joyda saqla.

## Eski standalone fallback

`standalone.html` Stage 52’dan byte-identical fallback sifatida qoldi. U Stage 56 lazy vocabulary va accessibility yangiliklarini o‘z ichiga olmaydi. Stage 56 uchun `index.html` dan foydalan.

## Cheklovlar

- Public GitHub Pages va Android qurilma hali Stage 57 da qabul sinovidan o‘tadi.
- Native HTTPS digest, microfon/ASR va offline cold-start Stage 57 checklist’da.
- Service Worker natijasi hozircha Node simulyatsiyasi; real Android install sinovi emas.
- `standalone.html` dan foydalanilsa, `audio/` papkasini yonida saqla.
