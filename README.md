# Torridonia SOPs — Staff Operations Manual

Interactive Standard Operating Procedures for Torridonia Highland Hostel volunteers.

## 📋 Available SOPs

| SOP | Tasks | Time | Languages |
|-----|-------|------|-----------|
| **Breakfast Service** | 22 | 7:00 AM - 12:00 PM | 🇬🇧 EN, 🇧🇷 PT-BR |
| **Guest Check-In** | 18 | On arrival | 🇬🇧 EN |
| **Housekeeping (B&B)** | 22 | Ready by 4 PM | 🇬🇧 EN |
| **Cottages Cleaning** | 25 | Full day | 🇬🇧 EN |
| **Laundry Service** | 17 | All day | 🇬🇧 EN |

## 🚀 Quick Start

### For Volunteers (WhatsApp/Mobile)

1. Open the link shared by your manager
2. The SOP opens in your browser (works offline after first load!)
3. Tap checkboxes to mark tasks as complete
4. Progress saves automatically
5. Use "Reset" button to start fresh

### For Managers (Deployment)

**Option 1: GitHub Pages (Recommended)**
```bash
# Clone this repo
git clone https://github.com/jorgeibanezhostack/sopbreakfasttorridonia.git
cd sopbreakfasttorridonia

# Copy all SOPs to repo
cp index.html breakfast-sop-*.html checkin-sop-en.html housekeeping-sop-en.html cottages-sop-en.html laundry-sop-en.html .

# Push to GitHub
git add .
git commit -m "Add all SOPs with index"
git push

# Enable GitHub Pages in repo settings
# Access at: https://jorgeibanezhostack.github.io/sopbreakfasttorridonia/
```

**Option 2: Direct File Sharing**
- Send HTML files directly via WhatsApp/Email
- Volunteers open in any browser
- Works immediately, no server needed

## 📱 Features

✅ **Mobile-first design** — Optimized for smartphones  
✅ **Progress tracking** — Automatic save via localStorage  
✅ **Offline capable** — Works without internet after first load  
✅ **Dark mode support** — Auto-adapts to system preference  
✅ **Collapsible phases** — Organized workflow steps  
✅ **Touch-friendly** — Large tap targets (44px+)  
✅ **Multilingual ready** — Easy to translate

## 🏗️ Architecture

### File Structure
```
index.html                    # Master hub (all SOPs)
breakfast-sop-en.html         # Breakfast (English)
breakfast-sop-pt-br.html      # Breakfast (Portuguese)
checkin-sop-en.html           # Guest Check-In
housekeeping-sop-en.html      # B&B Rooms
cottages-sop-en.html          # Cottages
laundry-sop-en.html           # Laundry
README.md                     # This file
```

### Technical Stack
- **Pure HTML/CSS/JS** — No dependencies
- **LocalStorage API** — Progress persistence
- **CSS Grid** — Responsive layout
- **CSS Variables** — Dark mode theming

### Progress Keys (localStorage)
- `torridonia_breakfast_progress` (EN)
- `torridonia_breakfast_progress_pt` (PT-BR)
- `torridonia_checkin_progress`
- `torridonia_housekeeping_progress`
- `torridonia_cottages_progress`
- `torridonia_laundry_progress`

## 🎨 Design System

**Colors:**
- Primary: `#004F59` (Teal)
- Background: `#f8f7f4` (Warm white)
- Text: `#1a1a19` (Near black)

**Typography:**
- Font: System defaults (`-apple-system, BlinkMacSystemFont, "Segoe UI"`)
- Sizes: 14px (body), 16px (titles), 18px (headers)

**Interactions:**
- Phase toggle: 0.3s ease
- Checkbox: 0.2s scale + color
- Touch targets: Minimum 44px

## 🔄 Integration with Lovable (Future)

To integrate into Hostack Staff App:

```typescript
// src/pages/SOPs.tsx
export default function SOPs() {
  return (
    <div className="sop-container">
      <iframe 
        src="/sops/breakfast-sop-en.html" 
        className="w-full h-screen border-0"
        title="Breakfast SOP"
      />
    </div>
  );
}

// Add routes
<Route path="/sops" element={<SOPs />} />
<Route path="/sops/breakfast" element={<BreakfastSOP />} />
<Route path="/sops/checkin" element={<CheckInSOP />} />
<Route path="/sops/housekeeping" element={<HousekeepingSOP />} />
<Route path="/sops/cottages" element={<CottagesSOP />} />
<Route path="/sops/laundry" element={<LaundrySOP />} />
```

## 📊 Metrics

| SOP | File Size | Load Time (4G) |
|-----|-----------|----------------|
| Index | 8.5 KB | <1s |
| Breakfast (EN) | 14.9 KB | <2s |
| Breakfast (PT-BR) | 14.9 KB | <2s |
| Check-In | 14.5 KB | <2s |
| Housekeeping | 15.2 KB | <2s |
| Cottages | 14.8 KB | <2s |
| Laundry | 13.9 KB | <2s |

## 🌍 Translation Guide

To add a new language (e.g., Spanish):

1. Copy an existing SOP file (e.g., `breakfast-sop-en.html`)
2. Rename to target language code (e.g., `breakfast-sop-es.html`)
3. Translate text content (keep HTML structure intact)
4. Update localStorage key (e.g., `torridonia_breakfast_progress_es`)
5. Add link to `index.html`

## 📝 Content Source

All SOPs extracted from:
- **Torridon Guidebook** (Google Docs)
- **Live Rota** (Google Sheets)
- **Audio transcriptions** (Check-In workflow)
- **Staff feedback** (Continuous improvement)

## 🤝 Contributing

To update an SOP:

1. Edit the HTML file directly
2. Test on mobile device (Chrome/Safari)
3. Verify localStorage persistence
4. Commit with descriptive message
5. Push to main branch

## 📞 Support

- **Manager:** Jorge Ibáñez
- **Location:** Torridon House, Torridon, Achnasheen IV22 2HA
- **GitHub:** [jorgeibanezhostack/sopbreakfasttorridonia](https://github.com/jorgeibanezhostack/sopbreakfasttorridonia)

---

**Built with ❤️ for the Torridonia volunteer community**  
*Last updated: May 2026*
