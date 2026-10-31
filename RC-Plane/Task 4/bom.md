# Problem 4: Bill of Materials for an Electric Single-Motor RC Aircraft

**Aircraft:** high-wing trainer/sport model, wingspan 1.2 m, wing area ≈ 0.22 m² (chord ≈ 0.18–0.20 m), 4 servos, hand or ground launch. No parts purchased.

## How to read the price columns
- **V** = price I saw on a retailer page while preparing this (date: 20 Oct 2026). Stock and price change often. Re-check before submitting.
- **E** = my estimate for the Indian market. I did not find a page to cite, so **confirm before using it**.
- Where a link is listed, it is the page where I saw the price. Some of the pages found were retailer mirror or marketplace pages; if a link does not open, search the product name on the retailer's site.

## Part A and B: Components and alternatives

| Component | Recommendation 1 (budget) | Recommendation 2 (performance) | Key specifications | Qty | Est. cost, R1 (₹) |
|---|---|---|---|---:|---:|
| **Motor** | A2212 1000 KV brushless. **₹375–459 (V)** [Robu](https://robu.in/?p=5908), [IndiaMART listing](https://m.indiamart.com/hatchnhacksolutions/stepper-motor.html) | 2212-class 900–1000 KV with better bearings (e.g. SunnySky X2212 type), ~₹1,800 (E) | 1000 KV, ~12 A rated, 3S, 10×4.5 prop. Shaft diameter: **sellers list 3.17 mm and 3.7 mm, so check against the prop adapter** | 1 | 375 (V) |
| **ESC** | SimonK 30A, **₹342 (V)** [Robu](https://robu.in/?p=61241) (no connectors, so solder) | Hobbywing Skywalker 30–40 A with 5 V BEC, ~₹1,500 (E) | Continuous ≥ 25 A, 3S, BEC for servos (check BEC current rating) | 1 | 342 (V) |
| **Propeller** | 1045 (10×4.5) | APC-type 10×4.7 slow-flyer | 10 in diameter, 4.5–4.7 in pitch. Carry a spare | 2 | 150 (E) |
| **Battery** | 3S 2200 mAh LiPo 40/80C, **₹1,599 (V)** [Probots](https://probots.co.in/11-1v-2200mah-40-80c-3s-lipo-battery-lithium-polymer.html) (was out of stock). Alternative: Orange 3S 2200 30C on [Robu](https://robu.in/product-category/batteries/battery/lithium-polymer-li-po) (price not seen) | Branded 3S 2200–3000 mAh 35–45C, ~₹2,200 (E) | 11.1 V, 2200 mAh, ≥ 30C, XT60 | 1 | 1,599 (V) |
| **Transmitter + receiver** | FlySky FS-i6 + FS-iA6B. **₹4,459 (V)** [Robu](https://st.robu.in/?p=33422), ₹4,999 [Probots](https://probots.co.in/fs-i6-2-4-ghz-6-channel-remote-radio-controller-for-fpv-quadcopter-tx-rx-mode-2.html), ₹3,437 + GST [Evelta](https://evelta.com/drones-and-rc-parts/?page=32) | FlySky FS-i6X + FS-iA10B (10 ch, telemetry) [Probots](https://probots.co.in/flysky-fs-i6x-10ch-rc-transmitter-ia10b-receiver.html) (price not seen, ~₹5,500 E) | 6 ch, AFHDS 2A, 2.4 GHz, receiver 4–8.4 V | 1 | 4,459 (V) |
| **Servos** | TowerPro-type MG90S metal gear, **₹130 (V)** [Robogears](https://robogearsin.odoo.com/shop/6466799-mg90s-metal-gear-servo-motor-180-degree-rotation-3317) (not for sale when seen); [Robu](https://robu.in/product/mg90s-9g-servo-metal-gear/) (out of stock when seen) | Digital metal-gear 9 g (e.g. Emax ES08MD class), ~₹450 each (E) | ~1.8–2.2 kg·cm at 4.8–6 V, ~13 g. Sellers warn of clones, so test the gears | 4 | 520 (V) |
| **Airframe** | 5 mm foam board / Depron sheet, with 6 mm carbon rod spar, ~₹800 (E) | EPP or balsa and film, ~₹2,500 (E) | Wing 1.2 m, rod through wing | 1 set | 800 (E) |
| Landing gear | Wire struts and foam wheels, ~₹250 (E) | Aluminium gear and rubber wheels, ~₹400 (E) | Can be omitted for hand launch | 1 set | 250 (E) |
| Connectors, wire, heat-shrink | XT60 pair, 3.5 mm bullets, silicone wire, ~₹300 (E) | Same, better quality, ~₹500 (E) | XT60 for battery, soldering | 1 set | 300 (E) |
| Adhesives | Foam-safe CA or UHU Por, hot glue, tape, ~₹400 (E) | Same plus epoxy, ~₹500 (E) | Check: normal CA and some glues melt foam | 1 set | 400 (E) |
| Control hardware | Pushrods, horns, hinges (tape), ~₹250 (E) | Clevises and pre-made hinges, ~₹400 (E) | 4 linkages | 1 set | 250 (E) |
| Charger (essential) | Balance charger for 2S/3S, e.g. IMAX B3 Pro type, ~₹1,500 (E) | Higher-power charger, ~₹3,000 (E) | **Never charge LiPo without balance charging** | 1 | 1,500 (E) |

## Part C: Technical rationale

### C1. Motor and propeller match, and thrust check
- Chosen: A2212 1000 KV on 3S (11.1 V), 1045 propeller. No-load speed ≈ 1000 × 11.1 ≈ 11,100 rpm. Loaded speed is lower (assume ~80%, ≈ 8,900 rpm).
- Propeller pitch speed = rpm/60 × pitch ≈ 8,900/60 × 0.114 m ≈ **17 m/s**. That is comfortably above the aircraft's 11–13 m/s cruise, so the prop can still produce thrust in flight.
- Expected static thrust ≈ 600–700 g (the Robu listing for this motor and a 1045 prop quotes about 700 g). This is an assumption to verify.
- **Check available thrust:** (1) run motor on a kitchen scale or luggage scale test stand, measure thrust, (2) read current and watts with a wattmeter, (3) compare to a propulsion calculator such as eCalc, (4) keep current within the motor's rating (~12 A) and watch motor temperature after a 30 s full-throttle run.

### C2. ESC rating and margin
- Expected maximum current ≈ 12–14 A (motor listing: 12 A rated). With a 1.5–2× safety margin → 20–28 A, so a **30 A ESC** gives ≈ 2× margin.
- Need 3S support, and a BEC that can feed 4 servos plus receiver (budget ESC BEC rating is not stated, so check it; add a separate UBEC if unsure). Servos can stall at ≈ 250 mA each.

### C3. Battery
- 3S matches the motor's design voltage. Discharge needed ≈ 14 A ÷ 2.2 Ah ≈ 6.4C, so a 30C pack has ≈ 4–5× margin.
- Weight ≈ 185 g (about 27% of the aircraft).
- Trade-offs: 2S is lighter but cannot power this motor and prop. 4S gives more power but needs a different motor, ESC and prop. A bigger pack (3000+ mAh) gives longer flights but increases wing loading and weight.
- Endurance estimate: about 2.2 A at steady cruise (≈ 25 W electrical) gives ~45 min, but realistic mixed flying at ~6–8 A gives **12–15 min**. Never discharge below 3.5 V per cell under load.

### C4. Servos and control surfaces
**4 servos:** 2 ailerons (one each), 1 elevator, 1 rudder. (A single servo with a Y-lead is a cheaper option for ailerons but is less controllable.) The ESC takes the throttle channel. 5 of the 6 FS-i6 channels are used. MG90S torque (~2 kg·cm) is suitable at these speeds. Verify by testing under load.

### C5. Structural material

| Material | Strength / mass | Cost | Repairability | Verdict |
|---|---|---|---|---|
| Foam board / Depron + carbon spar | Light, adequate | Lowest | Easy, cut and glue | **Budget choice** |
| EPP | Very crash-tolerant, slightly heavier | Medium | Good | Performance choice |
| Balsa + film | Lightest, stiffest, good finish | Medium | Harder, needs skill | Best for experienced builders |
| Plywood (firewall, motor mount) | Strong | Low | Moderate | Use locally in high-load spots |

### C6. Compatibility checks
- **Radio:** FS-i6 and FS-iA6B both use AFHDS 2A, so they are compatible and bind with a button/loop. Check the failsafe and range test (walk test with reduced power).
- **Electrical:** battery 11.1 V = ESC limit (3S, 30 A); XT60 connectors must match; ESC to motor 3.5 mm bullets (robu says ESC male and motor female); receiver supply 4–8.4 V from the BEC; servo voltage 4.8–6 V matches the 5 V BEC.
- **Mechanical:** motor shaft size matches prop adapter; prop clearance from the fuselage and ground (10 in prop needs ≥ 5 in of ground clearance in hand launch); motor mount hole pattern; battery fits in the bay and allows moving it to set CG; servo sizes fit.
- **Procedure:** ESC calibration (throttle endpoints), check the motor spins the correct way, **remove the prop for first bench power-up**.

## Part D: Budget

### Configurations

| Item | Budget (₹) | Performance (₹) |
|---|---:|---:|
| Motor | 375 | 1,800 |
| ESC | 342 | 1,500 |
| Propellers | 150 | 250 |
| Battery | 1,599 | 2,200 + second pack 2,200 |
| Transmitter and receiver | 4,459 | 5,500 |
| Servos ×4 | 520 | 1,800 |
| Airframe | 800 | 2,500 |
| Landing gear | 250 | 400 |
| Connectors, wire | 300 | 500 |
| Adhesives | 400 | 500 |
| Control hardware | 250 | 400 |
| Charger | 1,500 | 1,500 |
| **Total** | **≈ 10,950** | **≈ 21,050** |

(Mixed verified and estimated prices, see the legend above, so treat totals as ±15%.)

### Safe cost-saving opportunities
- Share one transmitter among the team (saves ~₹4,500 per additional aircraft).
- Use foam board and a carbon rod instead of balsa or EPP.
- Buy bullets and XT60 connectors in bulk and solder yourself.
- Use SG90 (₹60–90 listed) for the rudder and elevator only. **Do not save money on the battery, charger, or ESC**: they are the fire and crash risks.

### Choice for the competition: **Budget configuration plus a spare battery (≈ ₹12,500)**
Justification: the problem says money is limited, and the budget configuration gives a thrust-to-weight of ≈ 0.9 (below), enough for a stable trainer-class aircraft. The extra money goes to one safety item, a second battery, which doubles flying time per charge cycle and gives a backup. If the thrust test shows less than ~550 g, move to the performance motor and ESC.

## Bonus: Takeoff mass and propulsion sufficiency

| Item | Mass (g) |
|---|---:|
| Airframe and spar | 250 |
| Motor | 52 |
| ESC | 25 |
| Battery 3S 2200 | 185 |
| Servos ×4 | 52 |
| Receiver | 15 |
| Propeller | 12 |
| Wiring and connectors | 30 |
| Landing gear | 30 |
| Glue, hardware | 45 |
| **Total** | **≈ 696** |

Assumptions: typical masses for these components, air density 1.225 kg/m³, wing area 0.22 m², assumed CLmax ≈ 1.0–1.2, assumed static thrust 650 g.

- Weight = 0.696 × 9.81 ≈ 6.8 N. Wing loading ≈ 31 N/m² (≈ 32 g/dm²).
- Stall speed ≈ √(2W/(ρ S CLmax)) ≈ **6.5–7.1 m/s**.
- **Thrust-to-weight** = 650/696 ≈ **0.93**: good for hand launch (≥ 0.5–0.6 is the usual minimum).
- At 12 m/s: CL ≈ 0.35, assumed L/D ≈ 6.7, drag ≈ 1.0 N. Estimated thrust at 12 m/s (static thrust scaled linearly with airspeed against 17 m/s pitch speed) ≈ 1.85 N, so excess thrust ≈ 0.8 N and **climb ≈ 1.5 m/s**. This is a conservative estimate: it is enough for level flight and gentle climb, and acceptable for a trainer.
- Cruise power ≈ 25 W electrical (≈ 2.2 A).

**Conclusion:** propulsion is sufficient under these assumptions. The real check is the static thrust test. If the aircraft grows above ~850 g (T/W < 0.75), reduce mass or change the motor and prop.

## Deliverable status
- BOM table with alternatives: done (above). Verified prices and links are marked **V**.
- To do before submitting: confirm every V and E price and link on the day, and replace E entries with real listings.

## References
1. Robu.in, Probots, Evelta, IndiaMART product pages linked above (accessed 20 Oct 2026).
2. eCalc (ecalc.ch), propulsion calculator.
3. FlySky FS-i6 / FS-iA6B specification sheets (AFHDS 2A).
4. Raymer, D., *Aircraft Design: A Conceptual Approach*.
