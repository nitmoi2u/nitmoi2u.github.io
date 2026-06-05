# stocktap
**by nitmoi** · necessity is the mother of invention

**Status:** v1 built
**Category:** Stock management
**Privacy:** All data stored locally — product lookups via Open Food Facts API only, nothing else ever leaves the device

---

## Origin
Named by Claude. Built because every bar and restaurant still does stock counts on clipboards or spreadsheets. Scan it, tap the count, done.

---

## How the cache works
- First scan: hits Open Food Facts API (free, no key needed) — pulls name, brand, size, category
- Every subsequent scan: instant, fully offline — served from localStorage cache
- Stale threshold: 30 days — products tab flags stale items, one-tap refresh
- Manual entry: unknown products added by hand are saved permanently and never refreshed (source = manual)

---

## What it does (v1)
- Scan tab: barcode entry → product lookup → quantity +/− → add to count
- Count tab: live count with category filter, named counts, save to history
- History tab: all saved counts, per-count CSV export, full JSON backup
- Products tab: full cache view, stale indicators, bulk refresh, clear cache

## Export formats
- CSV: product, brand, size, category, quantity, barcode — opens in Excel/Sheets
- JSON: full backup including cache, importable to new device

---

## TODO before launch
- [ ] Add camera barcode scanning (ZXing or QuaggaJS)
- [ ] Write Gumroad listing copy
- [ ] Write Reddit launch post (r/bartenders, r/restaurantowners, r/smallbusiness)

---

## v2 Roadmap
- Camera barcode scanning (no manual typing)
- Variance report — compare two counts, flag losses
- Par level per product (alert when below threshold)
- Supplier notes per product
- Multi-location support
