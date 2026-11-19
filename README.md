# Bespa Measurement — user guide

The Quantity Surveyor's phone app for measuring road works on site. It records what has been built, by road and chainage, works without signal, and sends the period's measurements to the office as one file. The office values them in the **Bespa Progress and Valuation** app, where the laboratory, the Engineer's Deputy and the Engineer review and approve them.

The app holds **no rates and no money**.

It works in one of two ways, decided by the site pack:

- **Bills from the Road BOQ Estimator (version 2 site pack).** You record the **work done**: which activity, from where to where, and which culverts are finished. You type no dimensions. In the office, the Estimator's own two engines work out every item from your records, using the design: materials, concrete, formwork, reinforcement, pipes, binder, chippings and haulage. See sections 3 and 4.
- **Bills from any other source (version 1 site pack).** You measure each BOQ item by its dimensions. See sections 3b and 4b.

---

## 1. Install it on the phone (once)

1. Open the app's address in **Chrome** on the phone, with signal:
   `https://kwasi55.github.io/Road_Measurement_App/`
2. Chrome menu (⋮) → **Add to Home screen**.
3. Open it once from the home screen while you still have signal. From then on it works offline.

GPS stamping needs the app to be opened from this HTTPS address; allow location when the phone asks.

## 2. Load the project (Setup)

1. In the office, the Progress and Valuation app's **Site pack (Measurement app)** button downloads the project's `…_site_pack.json`. Send it to the phone by e-mail, WhatsApp or USB.
2. On the phone: **Setup → Load the site pack** and choose the file.

The pack carries the roads with their lengths, the BOQ items with their units and quantities, and the culverts. Loading a newer pack of the **same** project keeps your records. Loading a **different** project asks before it removes the old project's records.

## 3. Estimator bills: what the site pack holds

The pack carries the design of each road: the **activities** with the stretches where the design has them, the **culverts and structures** with their size and design length, and any **Other items**. Other items are bill items that the engines do not produce, and they are measured by dimensions as in 3b.

The **Measure** tab has five parts. In the first three, the QS picks a line from the design list; each line is one design stretch with its type, value, side and chainages.

| Part | The design list holds | Recorded as |
|---|---|---|
| **Formation** | Clearing (by vegetation class), Blading, Reshaping, Scarifying, Raise road (fill height), Cut to widen and Fill to widen (height and width), Retaining walls | From – To inside the stretch |
| **Pavement** | Sub-base and base (thickness), Prime coat, First seal, Second seal, Road furniture and markings | From – To inside the stretch |
| **Drains** | U-drains by size (e.g. *U-4, 600 × 900 mm, item K492.7, left*), trapezoidal drains, side ditches, kerbs, scour checks | From – To inside the stretch |
| **Culverts** | Each design culvert or structure | Completed (as-built length), or in progress (% constructed) |
| **Other** | Bill items the engines do not produce (shown only when there are any) | By dimensions, as in 3b |

Cut and fill to widen appear only where the design has them. Any other work needs a variation BOQ.

Widths, thicknesses, drain types, vegetation class and haul distances come **from the design**. The phone cannot change them. Work that differs from the design is paid only under an approved variation BOQ.

## 4. Estimator bills: record the work (Measure)

1. Check the **date**, **Measured by** and the **road**.
2. **Formation**, **Pavement** or **Drains**: pick the line from the design list, for example *Raise road (fill 45 cm) · 5+850–5+900* or *U-drain U-4 (600 × 900 mm, item K492.7), left · 7+500–8+300*. The hint shows the design stretch and what is paid so far. Enter **From** and **To** inside that stretch.
   The card shows what will be paid after the record. Payment is in **whole 50 m stations, rounded down**: records of the same item are joined, then each stretch is cut back to whole stations. A part station is paid once it is complete. For example, 0+000–0+275 pays 0+000–0+250, and the next record, 0+275–0+620, makes it 0+000–0+600.
   A record outside its design stretch is refused, because different work or a different size there is paid only under a signed variation order.
4. **Culverts**: choose the culvert from the design list.
   - **Completed** with the as-built length. It is paid up to the design length; a longer culvert needs the Engineer's approval and a variation order for the excess.
   - **In progress** with the percentage constructed. This is for the progress report only; a culvert is paid on completion.
5. **Other items** (only when the pack has some): measured by dimensions as in 4b.
6. Add notes, photos and a GPS stamp, then **Save**.

### What the app refuses

- A stretch of the same item recorded twice.
- An activity where the design has none ("additional work is paid only under an approved variation BOQ").
- A layer ahead of the layer below it, over the stations it would pay: base before sub-base, prime before base, first seal before prime, second seal or road furniture before the first seal.
- A record outside its design stretch (different work or size needs a signed variation order).
- A chainage outside the road, or a culvert recorded completed twice.

It **warns** when part of a record lies outside the design, when a record completes no whole station yet, and when a culvert is longer or shorter than its design.

## 3b. Other bills: set the dimensions (Items), once per item

Every record computes its own quantity: the **From** and **To** chainages give the length, and the item's dimensions do the rest.

| Unit of the item | What to set on the Items tab | Quantity of a record |
|---|---|---|
| m (drains, ditches, kerbs, markings) | nothing | length (× 2 for B/S on drains, ditches and kerbs) |
| m² (sub-base, base, reshaping) | width | length × width |
| ha (clearing) | width | length × width ÷ 10,000 |
| m³ (fill, excavation, concrete, chippings) | width and height of fill, depth or thickness (spread in m³ per m² for chippings) | length × width × height |
| litre (primer, cutter, binder) | width and spray rate (l/m²) | length × width × rate |
| nr, t, sum, m³·km and the like | nothing | the number you enter on the record |

The Items tab also shows, for each item, the BOQ quantity, the quantity measured so far and the percentage.

## 4b. Other bills: measure (Measure)

1. Check the **date**, **Measured by** and the **road**.
2. Choose the **BOQ item**: type part of its code or description in the search box (e.g. `R114`, `drain`, `kerb`) and pick it from the list.
3. For work along the road: **From** and **To** chainage *on that road* (metres from its start) and the **side**: LHS, RHS or B/S.
   For culverts, ramps, signs and other point items: the **chainage** and the **number**.
4. Check the quantity shown. If the work differs from the dimensions (wider at a junction, say), tick *The work differs…*, type the quantity and give the reason.
5. Add **photos** and a GPS stamp if wanted, then **Save**. The next record starts where this one ended.

The app refuses a stretch measured twice, a layer ahead of the layer below it, a chainage outside the road, and a record without a quantity, a measurer's name or (for a hand-entered quantity) a reason. It warns when an item's measured total passes its BOQ quantity.

## 5. Review (Records)

All records on the phone, newest first, filterable by item and road. A record not yet sent can be deleted; a sent record cannot.

## 6. Send to the office (Export)

1. Set **Period ends** (normally the last day of the month).
2. **Export the period file**: every record dated up to that day and not yet sent, with its photos, goes into one file, `…_measurements_YYYY-MM.json`. Those records are then marked *sent*.
3. Send the file to the office. **Export all records** makes a full copy (for a backup or a resend); it marks nothing as sent.

The office imports the file into Progress and Valuation. A file imported twice adds nothing.

## 7. What happens next (in the office)

Every record leaves the phone as *recorded*. In Progress and Valuation, the **Measured work** tab imports the file and values the work to a period end. For Estimator bills, both Estimator engines (the Python port and the LibreOffice master) measure everything recorded to date and must agree. This month's quantities are the total to date less the previous valuation, and they are valued at the contract rates. The Measured BOQ and taking-off sheets come out as Excel, checked by LibreOffice. Then:

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
| "A layer cannot be measured ahead of the layer below it" / "cannot be recorded ahead" | Record the lower layer over those chainages first |
| "The design has no such work here" | The design does not have that activity there; ask the Engineer about a variation BOQ |
| "waits until its 50 m station is complete" | Nothing is wrong: the part station is paid when the rest of it is recorded |
| "Already measured" | That stretch is recorded; check Records, delete the wrong one if it is not yet sent |
| GPS not read | Open the app from its https address, allow location, stand in the open |
| The office says the file belongs to another project | Load that project's site pack on the phone and export again |

---

*Bespa Expert Systems — preliminary engineering aid. Measurements are checked and certified by the Engineer.*
