# Torridonia SOPs — Staff Operations Manual

Interactive Standard Operating Procedures for Torridonia Highland Hostel volunteers.

**Live Site:** [https://jorgeibanezhostack.github.io/guidebookstorridon/](https://jorgeibanezhostack.github.io/guidebookstorridon/)

---

## 📋 Available SOPs

| SOP | Tasks | Schedule | Languages |
|-----|-------|----------|-----------|
| **Breakfast Service** | 22 | 7:00 AM - 12:00 PM | 🌍 5 languages |
| **Guest Check-In** | 18 | On arrival | 🇬🇧 English only |
| **Housekeeping (B&B)** | 22 | Ready by 3:00 PM | 🌍 5 languages |
| **Cottages Cleaning** | 25 | Full day job | 🌍 5 languages |
| **Laundry Service** | 17 | All day job | 🌍 5 languages |

**Supported Languages:** 🇬🇧 English | 🇧🇷 Português Brasileiro | 🇪🇸 Español | 🇫🇷 Français | 🇮🇹 Italiano

---

## 🚀 Quick Start

### For Volunteers (Using SOPs)

1. **Open the link** shared by your manager via WhatsApp
2. **Select your language** from the dropdown (top right)
3. **Start checking tasks** as you complete them
4. **Your progress saves automatically** — reopen anytime to continue

**Works offline after first load!** Perfect for areas with poor WiFi.

---

### For Managers (Sharing SOPs)

**Direct Links:**
```
🍳 Breakfast: https://jorgeibanezhostack.github.io/guidebookstorridon/breakfast-sop-multilang.html
🔑 Check-In: https://jorgeibanezhostack.github.io/guidebookstorridon/checkin-sop-en.html
🛏️ Housekeeping: https://jorgeibanezhostack.github.io/guidebookstorridon/housekeeping-sop-multilang.html
🏡 Cottages: https://jorgeibanezhostack.github.io/guidebookstorridon/cottages-sop-multilang.html
🧺 Laundry: https://jorgeibanezhostack.github.io/guidebookstorridon/laundry-sop-multilang.html
```

**WhatsApp Message Template:**
```
Hi [Name]! 👋

Your [TASK NAME] SOP:
🔗 [PASTE LINK]

Select your language from the dropdown at the top!
Your progress saves automatically ✅

— Jorge
```

---

## 📱 Features

### ✅ Mobile-First Design
- Optimized for smartphones (primary device for volunteers)
- Touch-friendly interface (44px+ tap targets)
- Responsive layout adapts to any screen size
- Dark mode support (auto-adapts to system preference)

### ✅ Progress Tracking
- **Automatic save** — progress stored in browser localStorage
- **Persistent** — reopen anytime to continue where you left off
- **Visual progress bar** — see completion percentage at a glance
- **Task counter** — "5/22 tasks completed"

### ✅ Multilingual Support
- **5 languages available** in most SOPs
- **Language selector** — easy dropdown in header
- **Language persistence** — remembers your choice for all SOPs
- **Natural translations** — not Google Translate, human-adapted

### ✅ Offline Capability
- **Works without internet** after first load
- **Perfect for remote locations** with unreliable WiFi
- **No installation required** — just open in browser

### ✅ Interactive Checklists
- **Collapsible phases** — expand/collapse task sections
- **One-click marking** — tap to check/uncheck
- **Color-coded** — completed tasks show with checkmark
- **Reset option** — start fresh when needed

---

## 🏗️ Technical Details

### Architecture
- **Pure HTML/CSS/JavaScript** — No dependencies, no build process
- **Single-file SOPs** — Each SOP is self-contained
- **LocalStorage API** — Progress persistence
- **CSS Variables** — Theming and dark mode
- **GitHub Pages** — Free, reliable hosting

### File Structure
```
guidebookstorridon/
├── index.html                         # Landing page hub
├── README.md                          # This file
├── breakfast-sop-multilang.html       # Breakfast (5 languages)
├── checkin-sop-en.html                # Check-In (English only)
├── housekeeping-sop-multilang.html    # Housekeeping (5 languages)
├── cottages-sop-multilang.html        # Cottages (5 languages)
└── laundry-sop-multilang.html         # Laundry (5 languages)
```

### LocalStorage Keys
Each SOP stores its progress independently:
- `torridonia_breakfast_progress` — Breakfast tasks
- `torridonia_checkin_progress` — Check-In tasks
- `torridonia_housekeeping_progress` — Housekeeping tasks
- `torridonia_cottages_progress` — Cottages tasks
- `torridonia_laundry_progress` — Laundry tasks
- `torridonia_lang` — Selected language (shared across SOPs)

### Browser Support
- ✅ Chrome/Edge (recommended)
- ✅ Safari (iOS/macOS)
- ✅ Firefox
- ✅ Samsung Internet
- ⚠️ Internet Explorer (not supported)

---

## 🎨 Design System

**Colors:**
- Primary: `#004F59` (Teal)
- Background: `#f8f7f4` (Warm white)
- Text: `#1a1a19` (Near black)

**Typography:**
- Font: System defaults (`-apple-system, BlinkMacSystemFont, "Segoe UI"`)
- Base size: 14px
- Line height: 1.5

**Interactions:**
- Phase expand/collapse: 0.3s ease
- Checkbox animation: 0.2s scale + color transition
- Minimum touch targets: 44px (accessibility)

---

## 🔄 Integration

### Embed in Staff App (Lovable/React)

```typescript
// src/pages/BreakfastSOP.tsx
export default function BreakfastSOP() {
  return (
    <iframe 
      src="https://jorgeibanezhostack.github.io/guidebookstorridon/breakfast-sop-multilang.html"
      className="w-full h-screen border-0"
      title="Breakfast SOP"
    />
  );
}

// Add route
<Route path="/sops/breakfast" element={<BreakfastSOP />} />
```

### Direct Link Sharing (WhatsApp/Email)
Simply share the direct URL — no setup needed.

---

## 📊 Analytics

Track usage with Google Analytics (optional):
```html
<!-- Add to each SOP before </head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🛠️ Development

### Local Testing
```bash
# Clone repository
git clone https://github.com/jorgeibanezhostack/guidebookstorridon.git
cd guidebookstorridon

# Serve locally (Python)
python3 -m http.server 8000

# Or with Node
npx http-server -p 8000

# Open browser
open http://localhost:8000
```

### Deployment
Push to `main` branch — GitHub Pages auto-deploys in ~2 minutes.

```bash
git add .
git commit -m "Update SOPs"
git push origin main
```

---

## 🌍 Translation Guide

To add a new language to a multilingual SOP:

1. **Open the SOP HTML file**
2. **Find the `translations` object** in the `<script>` section
3. **Add a new language key** (e.g., `de` for German)
4. **Translate all text strings** maintaining the exact keys
5. **Add language option** to the `<select>` dropdown:
   ```html
   <option value="de">🇩🇪 Deutsch</option>
   ```
6. **Test thoroughly** on mobile and desktop

**Example translation entry:**
```javascript
de: {
  title: "Frühstücksservice SOP",
  reset: "Zurücksetzen",
  tasks: "Aufgaben",
  "total-tasks": "22",
  // ... rest of translations
}
```

---

## 📝 Content Sources

SOPs extracted from:
- **Torridon Guidebook** (Google Docs)
- **Live Operations Rota** (Google Sheets)
- **Audio Transcriptions** (Staff walkthroughs)
- **Volunteer Feedback** (Continuous improvement)

---

## 🤝 Contributing

### Reporting Issues
Found a typo or incorrect instruction? Please create an issue:
```
https://github.com/jorgeibanezhostack/guidebookstorridon/issues
```

### Suggesting Improvements
Have ideas for new features or better wording? Open a pull request or issue.

---

## 📞 Support

**Manager:** Jorge Ibáñez  
**Location:** Torridon House, Torridon, Achnasheen IV22 2HA, Scottish Highlands  
**Email:** jorge@hostack.io  
**GitHub:** [@jorgeibanezhostack](https://github.com/jorgeibanezhostack)

---

## 📄 License

© 2026 Torridonia Highland Hostel. All rights reserved.  
Built with ❤️ for the volunteer community.

---

**Last updated:** May 18, 2026
