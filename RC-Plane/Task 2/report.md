# Problem 2: The Paper Plane Challenge (longest airtime)

> **Status:** Parts A, B and the test plan are complete. **Part C trial times are blank because only you can fly and time the plane.** Predicted values below are calculations to compare your results against, not measurements.

## Part A: Design

### Choice: wide-wing "floater" glider (design F) and a dart for comparison (design D, bonus)

| | **F: Floater (final)** | **D: Dart (bonus control)** |
|---|---|---|
| Wingspan | ≈ 190 mm | ≈ 100 mm |
| Wing area | ≈ 190 cm² (0.019 m²) | ≈ 120 cm² |
| Aspect ratio | ≈ 1.9 | ≈ 0.8 |
| Mass (A4, 80 gsm) | ≈ 5.0 g | ≈ 5.0 g |
| Wing loading | ≈ 2.6 N/m² | ≈ 4.1 N/m² |

Why: for airtime, the aim is the **lowest sink rate**, not speed. Sink rate falls with low wing loading, so spread the 5 g over as much wing as possible, keep the nose heavy enough for a stable glide, and keep drag low.

### Construction steps (take a photo at each step; add them to `photos/`)
1. Fold the A4 sheet in half lengthwise, crease hard, open flat (centreline).
2. Fold the top two corners to the centreline (a pointed nose).
3. Fold the new angled edges to the centreline again, then fold the tip back over to lock the nose. This puts 3–4 paper layers at the front, which is the ballast.
4. Fold in half along the centreline, with the folds outside.
5. Fold each wing down about 4–5 cm from the keel, giving the widest wing the sheet allows.
6. Add about 5° dihedral (wing tips slightly up) for roll stability.
7. Cut small trailing-edge flaps (about 15 × 30 mm) in the wing, bend both up 1–2 mm slightly for pitch trim.

**Trim procedure (record this):** glide-test gently, adjust flaps. Dives mean raise the elevator flaps or move weight back. Stalls and then dives mean lower the flaps or add nose weight (more nose folds).

## Part B: Aerodynamics

**1. How lift is generated.** The wing deflects air downward at a positive angle of attack, so by Newton's third law the air pushes the wing up. Equivalently, the pressure on the lower surface exceeds that on the upper. Lift = ½ρV²·S·CL. Thin folded paper behaves like a cambered flat plate. At Re ≈ 15,000–20,000 the flow is laminar and prone to separation, which is why a clean, flat, crease-free wing matters.

**2. Forces.**
- **Launch:** hand throw gives initial kinetic energy and speed. A gentle, upward launch gives height and a short climb. This is the only "thrust": there is no sustained propulsion.
- **Glide:** weight (0.049 N) is balanced by lift and drag. The plane glides down along a path where the component of weight along the path equals the drag. Thrust is zero, so the aircraft trades **height for speed**. Flight time ≈ launch height ÷ sink rate (plus any thermal or launch-climb bonus).

**3. Wing area, wing loading, CG and stability.**
- Wing loading W/S = 0.049 / 0.019 ≈ 2.6 N/m² for F vs 4.1 for D.
- The CG must lie **ahead of the aerodynamic centre** (about 25% of chord): a nose-heavy plane is statically stable because a nose-up disturbance produces a nose-down restoring moment. Too far forward means a steep dive; too far aft means stall and tumbling.
- Dihedral gives roll stability, and a keel and vertical folds give yaw stability.

**4. Why F outlasts a dart, and sink rate vs glide distance.**
Simple model (CD = CD0 + CL²/(π e AR), assumed CD0 = 0.03–0.05, e = 0.8, ρ = 1.225):

| | Max glide ratio (L/D) | Speed at best glide | Sink at best glide | Speed at min sink | **Min sink rate** |
|---|---|---|---|---|---|
| F (AR 1.9) | 4.9–6.3 | 2.9–3.3 m/s | 0.53–0.60 m/s | 2.2–2.5 m/s | **≈ 0.46–0.53 m/s** |
| D (AR 0.8) | ≈ 3.4 | ≈ 5.0 m/s | ≈ 1.5 m/s | n/a | ≈ 1.4 m/s |

- **Best glide** (max L/D) gives maximum *distance*: the flattest path, at CL = √(CD0/k).
- **Minimum sink** gives maximum *time*: it occurs at lower speed and higher CL = √(3·CD0/k). It minimises power required, ∝ CD/CL^1.5.
- Prediction: from about 2 m launch height F stays up on the order of 3–5 s, D 1–2 s. Treat these as rough, because paper at Re ≈ 2×10⁴ is far from ideal airfoil theory.
- A dart is designed for speed and distance: small wings, high loading, high sink.

## Part C: Experiment

### Test conditions (control these)
Indoor, still air (fans and air-conditioning off), the same launch height (mark a spot, e.g. 2.0 m), same launcher, same gentle throw angle, timing by video frame count if possible (phone video at 30 fps, reading frames) or two stopwatch operators averaged.

### Trial table: FILL IN

| Trial | Design F time (s) | Design D time (s) | Notes (launch, trim, crash) |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 (optional) | | | |
| **Mean** | | | |
| Std dev | | | |

Report mean, standard deviation, and say whether F's advantage exceeds the spread. With 5 flights, a difference smaller than about the standard deviation is not conclusive.

### Two modifications and how to test them
| Modification | Expected effect | Controlled test |
|---|---|---|
| **1. Increase span by 15 mm (higher AR) while keeping the same nose folds** | Less induced drag, lower sink | Build F and F+ from sheets of the same paper. Same launch height, thrower, 5+ flights each, alternating F and F+ to cancel drift in the room conditions |
| **2. Trailing-edge flaps up 1 mm vs 3 mm (trim change)** | Moves CL toward min-sink point, and too much causes a stall | Same airframe, only flap angle changed (use a template for the angle), 5+ flights each |

Keep constant: paper type and mass (weigh each plane to 0.01 g if you can), launch height, room, thrower, number of flights.

## Deliverable checklist
- [ ] Photos of each build step (`photos/`)
- [ ] Short video of at least one flight (`flight_video.mp4`)
- [ ] Trial table filled in with **your** measurements
- [ ] Mean and comment on results vs the prediction

## References
1. Anderson, J.D., *Introduction to Flight*, McGraw-Hill (lift, drag, glide, power required).
2. Playlist in the README: lift, induced drag, parasite drag, Reynolds number, "Airplanes and Energy" videos.
3. Mueller, T.J. (ed.), *Fixed and Flapping Wing Aerodynamics for Micro Air Vehicle Applications*, AIAA, 2001 (low-Re flow).
