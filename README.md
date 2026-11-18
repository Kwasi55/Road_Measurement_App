# Bespa Measurement — user guide

The Quantity Surveyor's phone app for measuring road works on site. It records what has been built, by road and chainage, works without signal, and sends the period's measurements to the office as one file. The office values them in the **Bespa Progress and Valuation** app, where the laboratory, the Engineer's Deputy and the Engineer review and approve them.

The app holds **no rates and no money**. It measures quantities only.

---

## 1. Install it on the phone (once)

1. Open the app's address in **Chrome** on the phone, with signal:
   `https://<user-name>.github.io/Road_Measurement_App/`
2. Chrome menu (⋮) → **Add to Home screen**.
3. Open it once from the home screen while you still have signal. From then on it works offline.

GPS stamping needs the app to be opened from this HTTPS address; allow location when the phone asks.

## 2. Load the project (Setup)

1. In the office, the Progress and Valuation app's **Site pack (Measurement app)** button downloads the project's `…_site_pack.json`. Send it to the phone by e-mail, WhatsApp or USB.
2. On the phone: **Setup → Load the site pack** and choose the file.

The pack carries the roads with their lengths, the BOQ items with their units and quantities, and the culverts. Loading a newer pack of the **same** project keeps your records. Loading a **different** project asks before it removes the old project's records.

## 3. Set the dimensions (Items), once per item

Type each item's dimensions once; every record then computes its own quantity.

| Unit of the item | What to type | Quantity of a record |
|---|---|---|
| m (drains, ditches, kerbs, markings) | Size / type (e.g. `600x600`), and whether it is measured per side | length (× 2 for both sides) |
| m² (sub-base, base, clearing) | Width | length × width |
| m³ (fill, concrete) | Width, and thickness (or chipping spread in m³/m²) | length × width × thickness |
| litre (primer, binder) | Width and spray rate (l/m²) | length × width × rate |
| ha | Width | length × width ÷ 10,000 |
| nr, t, sum, m³·km and the like | nothing | the number you enter on the record |

The Items tab also shows, for each item, the BOQ quantity, the quantity measured so far and the percentage.

## 4. Measure (Measure)

1. Check the **date** and **Measured by**.
2. Choose the **BOQ item** and the **road**.
3. For work along the road: **From** and **To** chainage *on that road* (metres from its start) and the **side**: LHS, RHS or B/S.
   For culverts, ramps, signs and other point items: the **chainage** and the **number**.
4. Check the quantity shown. If the work differs from the dimensions (wider at a junction, say), tick *The work differs…*, type the quantity and give the reason.
5. Add **photos** (they are reduced in size on the phone) and press **Stamp GPS** if you want the position recorded.
6. **Save measurement**. The next record starts where this one ended.

### What the app refuses

- Measuring the same stretch of the same item twice (both sides overlap either side).
- A layer ahead of the layer below it: base before sub-base, kerbs or primer before base, seal before primer, over the same chainages.
- A chainage outside the road's length.
- A record without a quantity, without the measurer's name, or a hand-entered quantity without a reason.

It **warns** (and lets you continue) when an item's measured total passes its BOQ quantity.

## 5. Review (Records)

All records on the phone, newest first, filterable by item and road. A record not yet sent can be deleted; a sent record cannot.

## 6. Send to the office (Export)

1. Set **Period ends** (normally the last day of the month).
2. **Export the period file**: every record dated up to that day and not yet sent, with its photos, goes into one file, `…_measurements_YYYY-MM.json`. Those records are then marked *sent*.
3. Send the file to the office. **Export all records** makes a full copy (for a backup or a resend); it marks nothing as sent.

The office imports the file into Progress and Valuation. A file imported twice adds nothing.

## 7. What happens next (in the office)

Every record leaves the phone as *recorded*. In Progress and Valuation:

| Role | Does |
|---|---|
| Surveyor | Survey levels and earthwork quantities for realignment sections |
| Laboratory team | Records each test (field density, concrete cubes, …): pass or fail |
| Engineer's Deputy | Inspects each stretch to be paid and confirms the laboratory result |
| Engineer | Omits failed work, ticks the required documents; the certificate turns from amber to green when all are ticked, and only the Engineer sends it to Head Office |

Work that fails its test counts as progress but is not paid until it is re-tested and passes.

## 8. Good to know

- **Where the data is:** in this phone's browser, under this app's address, until exported. Clearing Chrome's site data, uninstalling Chrome, or moving the app to another address starts empty — **export all records first**.
- **Back up** with *Export all records* at least weekly.
- **One project at a time** on a phone.
- **Updates:** when a new version is published, open the app once with signal; it updates itself.

## Troubleshooting

| Problem | What to do |
|---|---|
| "Load the site pack first" | Setup → load the `…_site_pack.json` from the office |
| Quantity shows "set the width…" | Items tab → type the item's dimensions |
| "A layer cannot be measured ahead of the layer below it" | Measure the lower layer over those chainages first |
| "Already measured" | That stretch is recorded; check Records, delete the wrong one if it is not yet sent |
| GPS not read | Open the app from its https address, allow location, stand in the open |
| The office says the file belongs to another project | Load that project's site pack on the phone and export again |

---

*Bespa Expert Systems — preliminary engineering aid. Measurements are checked and certified by the Engineer.*
