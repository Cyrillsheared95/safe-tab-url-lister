# Safe Tab URL Lister

A minimal, privacy-first Chrome extension that lists and copies all open tab URLs locally — no servers, no tracking.

## Features

- List URLs from the current window or all open Chrome windows
- Optionally include page titles alongside each URL
- **4 output formats:** Plain URLs, Markdown links, JSON, CSV
- One-click copy to clipboard
- Dark mode support (follows system preference)
- Fully accessible (WCAG 2.1 AA)

## Privacy

- Only the `tabs` permission — nothing else
- No `host_permissions`, no `content_scripts`, no background service worker
- No network requests whatsoever
- No cookies, no storage, no analytics
- All data stays on your device

## Installation (unpacked)

1. Download or clone this repository
2. Open `chrome://extensions/`
3. Enable **Developer mode** (top right)
4. Click **Load unpacked** → select this folder

## Chrome Web Store Listing Copy

### Short description (132 chars)
```
List and copy all tab URLs locally. Zero tracking, no servers, minimal permissions. Plain, Markdown, JSON, CSV.
```

### Long description
```
Safe Tab URL Lister instantly lists every open tab URL in your current Chrome window — or all windows — so you can copy and paste them wherever you need.

OUTPUT FORMATS
• Plain URLs — one URL per line
• Markdown links — [Page Title](https://url)
• JSON — structured array for developers
• CSV — spreadsheet-ready with optional titles

PRIVACY FIRST
This extension requests only the "tabs" permission. There are no background processes, no data collection, no external servers, no cookies, no analytics, and no host permissions. Your browsing data never leaves your device.

FEATURES
• Include or exclude page titles
• Cover current window or all Chrome windows
• One-click clipboard copy
• Dark mode support
• Keyboard accessible

IDEAL FOR
Developers saving research sessions, writers collecting references, teams sharing resource lists, and anyone who values minimal, auditable browser extensions.

Open source — you can read every line of code.
```

## Chrome Web Store Submission Checklist

- [x] Extension zip: `safe-tab-url-lister-v1.0.0.zip` (Desktop klasöründe)
- [x] Icons: 16×16, 48×48, 128×128 PNG (`icons/`)
- [x] Manifest V3
- [x] i18n: English + Turkish (`_locales/`)
- [ ] Developer account: https://chrome.google.com/webstore/devconsole ($5 one-time fee)
- [ ] Screenshots: min 1 × 1280×800 or 640×400
- [ ] Store listing filled (use text above)
- [ ] Submit for review

## Store Upload Steps

1. `chrome.google.com/webstore/devconsole` adresine git
2. Giriş yap (Google hesabı) — ilk kez $5 developer ücreti gerekir
3. **"New item"** → `safe-tab-url-lister-v1.0.0.zip` dosyasını yükle
4. **Store listing** sekmesinde:
   - Description: yukarıdaki "Long description" metnini yapıştır
   - Category: **Productivity**
   - Language: English
5. **Graphics** sekmesinde:
   - Promotional tile (440×280) — opsiyonel ama önerilir
   - Screenshots (en az 1): popup'ı açık haldeyken ekran görüntüsü al (1280×800)
6. **Privacy** sekmesinde: "This extension does not collect user data" seç
7. **Submit for review** — inceleme genellikle 1-3 iş günü sürer

## Development

```bash
# İkonları yeniden üret (tasarım değişirse)
node generate-icons.js

# Store zip paketi oluştur
zip -r ../safe-tab-url-lister-v1.0.0.zip . \
  --exclude "*.DS_Store" \
  --exclude "generate-icons.js" \
  --exclude "node_modules/*"
```
