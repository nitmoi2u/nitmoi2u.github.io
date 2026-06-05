# delivery analyzer
**by nitmoi** · necessity is the mother of invention

**Status:** v1 built
**Category:** Earnings & shift tracking
**Privacy:** All data stored locally — never uploaded, never shared

---

## Origin
Built originally in Android Studio by the founder out of personal necessity as an independent takeaway delivery driver. Rebuilt as a privacy-first browser tool under the nitmoi brand.

---

## What it does

### Core logic (v1)
- Three inputs per delivery: order cost, cash received, delivery charge
- Auto-detects card vs cash payment (blank cash field = card)
- Calculates: restaurant owes you / you owe restaurant
- Tip amount and tip percentage with positive reinforcement labels
  - 15%+ = "Generous tip!"
  - 8–14% = "Solid tip"
  - Below 8% = "Standard tip" (never negative)

### Shift analytics
- Running delivery count
- Total tips and average tip per delivery
- Average tip rate across the shift
- Total cash settlement figure for end of night

### History
- Each shift saved with date, delivery count, earnings, tips, settlement
- All-time stats: total shifts, all-time tips, best shift, average per shift

### Data portability
- Export full history as timestamped JSON backup
- Import JSON on any device — smart merge, no duplicates
- Designed for new device setup without losing history

---

## Files
- `delivery-analyzer.html` — single file, self-contained, no dependencies

---

## Branding applied
- nitmoi wordmark + tagline in header
- Core blue (#185FA5) primary colour
- Privacy badge: "your data never leaves your device"
- Lowercase tool name throughout

---

## TODO before launch
- [ ] Apply finalised nitmoi branding to HTML file
- [ ] Test on Android and iOS browsers
- [ ] Test JSON export/import on mobile
- [ ] Write Gumroad listing copy
- [ ] Write Reddit launch post

---

## v2 Roadmap
- Receipt / summary screenshot scanning to auto-populate entries
- In-app navigation to delivery address
- Multi-platform comparison (Uber Eats, Just Eat, Deliveroo alongside independent)
- Hourly rate calculation (add shift start/end time)
- Weekly and monthly earnings charts
