
### Parts List (vs V0)

NOTE: the parts listed here represent only those which go on T0-specific parts.  The gantry, toolhead, and frame can be kept stock.

#### Required

**Z drive and bed  parts**:

| Category | Part | Qty | Notes |
| - | - | - | - |
| Z Drives | NEMA14 or NEMA17 motors | 3 | For any build size, 52mm NEMA14 or 40mm-48mm NEMA17 1.8-degree steppers are ideal.<p></p> Smaller (33mm NEMA14 or pancake NEMA17) and 0.9-degree steppers will be less likely to hold the bed up when the power cuts out, leading to more time needed for bed leveling, and possibly a failure to auto-level if the tilt exceeds the probing distance.  You can work around this possibility by parking the bedframe at the bottom when not in use, to get away with smaller motors.  <p></p>Mix and match should be fine; use what you've got. <p></p>  [Recommended NEMA17 motors](https://www.amazon.com/STEPPERONLINE-Stepper-63-74oz-Connector-Extruder/dp/B07LCK19D5/) - 39mm depth leave more internal space vs 48mm-length steppers and has plenty of hold.
| Z Drives | GT2 belt | 3x~500mm | Add 100mm for Plus size if adding Z height.
| Z Drives | GT2 16t pulleys | 3 | Z Drive pulleys
| Z Drives | MGN7H 150mm | 2 | Ideally, upgrade to MGN9C on the X carriage, then get only one of these to repurpose for a front Z drive.  See other notes below.
| Z Drives | F623 bearings | 6 | Idlers |
| Z Bed | Metal spacers | 3 | Typically 1/2" (12.7mm) or slightly larger, depending on the height of your bed.  Can be loose; will be fine, once tightened down.|
| Z Bed | Wago 221-412 | 6-8 | 2-position electrical connector

**Frame**

No new extrusions are required, because the original V0 bedframe 100mm extrusions are repuprosed into a new T-shaped bedrame.  Nice, huh?

**Motion**

See above for options: a medium-preload MGN9C with matching carriage is highly recommended, with an MGN7H medium-preload option not far behind.  Why mention this?  Because you don't want toolhead flop to affect bed-probe results or print quality.  

[This V0 carriage](https://github.com/zruncho3d/DuelingZero/blob/main/STLs/Low_Side_X_Carriage_x1.stl) is recommended to match.  

**Electronics**:

Two additional Z-drive stepper ports are needed.  Pretty much anything will work, and the Klipper changes are minimal.

For conversions, an added SKR Pico, SKR E3, ERCF EZ BRD, Fly-RPFmex - taped to the power supply - will work great.  The only downside is the need to update two different boards for Klipper.

If doing a larger build, much more space is available; consider starting with a 6-stepper-minimum board, such as a BTT Octopus, BTT Manta 8p, Fysetc Spider, Mellow Fly, Fysetc S6, or whatever's the latest hotness.  

The most interesting, lowest-cost option: a 5-stepper board (like an SKR 2) with a CAN bus toolhead.

**Fasteners**:

The list below almost certainly over-estimates, because it doesn't factor in screws that are freed up when doing a V0 conversion, especially for Z drives and skirt parts.  Regardless, if you get the amounts below, you should have plenty.  Recommendation: buy 50-packs of the most common screw sizes so you don't have to count or worry about it and can do the next mod without waiting for shipping.

| Category | Part | Qty | Notes |
| - | - | - | - |
| Fasteners | M2x10 self-tapping | 2 | For ZeroClick |
| Fasteners | M2x6 BHCS or SHCS | 22+ | For retaining the Z attachments in rear (2), 6-8 for the rear Z bar, nutbars (2x6), plus one per front idler (2) |
| Fasteners | M2x8 BHCS or SHCS | 4+ | For retaining the Z belt attachments in front (2x2); use this size for rear Z attachment if using printed sliders |
| Fasteners | M2 nuts | 12 | For M2 nutbars
| Fasteners | M3x6 BHCS | 47+ | For skirts (~24), bumps (16), ZeroClick probe-grab screw (1), belt attachment strengthening (6)
| Fasteners | M3x8 BHCS | 24 | bedframe extrusion connections (14), front motor mounts to motors (8?), rear motor mount vertical screws, Rear Z motor mount horizontal screws (2)
| Fasteners | M3x16 BHCS | 3 | For Z bed attachment (vertical), for Z idler tensioning (vertical)
| Fasteners | M3x12 BHCS | 4 | Rear Z belt attachment (horizontal)
| Fasteners | M3x10 BHCS | 4 | rear Z motor attachment
| Fasteners | M3 nuts | Yes | One per most M3 screws
| Fasteners | M3 heatsets | 22+ | For bed joints (3), motor skirts (4x3), rear z belt attachment (4), tensioner (1), fans skirt (2)


#### Optional
| Category | Part | Qty | Notes |
| - | - | - | - |
| Bed | Sexbolt endstop board/kit, **not soldered** | 1 | A sexbolt endstop enables Auto-Z. Optionally, repurpose the original Z endstop and use the ZeroClick probe as a virtual endstop instead. Ensure you get a non-soldered board, as the default presoldered one from DFH comes soldered to the wrong side. |
| Frame | Guitar Feet | 4 | Optional; same as used with Voron Trident.  Can use original V0.1 rubber feet instead.  Just put a nut in the foot, squeeze it, and use an M3 BHCS from the other side
| Skirts | 40mm Fans | 2 | Recommended for airflow down there.

## Build Guide

In this repo are all of the STLs needed to build a Tri-Zero Alpha which are not in another repo (primary V0.1).

All parts should be already be in print-ready orientation, with seam in the +Y dir, and no supports are needed.  Standard Voron settings, or lowered infill and fewer perims, should work fine for most parts:
- 4 perimeters
- 40% infill, depending on the part
- 0.2mm layer height

The MotorSkirts and Rear Corners are happy with 20% infill, for a bit of print speedup.

Note that you will need all the STLs in the top-level STLs folder in the quantities listed at the end of each part name, with a few exceptions:
* Between NEMA14 and NEMA17, you'll need to pick one for each motor.  You can actually mix and match them, though.
  * `Rear_Motor_Mount`
  * `Motor_Corner_Screw_In`
* For the front bed mount, pick between the main and extended one.
  * `Front_Bed_Mount` for usual V0 beds
  * `Front_Bed_Mount_Extended` for MRW-style beds which stick out by 5mm, which means they need to be shifted forwards by 5mm to expose the nozzle endstop to the nozzle.
* Front corner bumps are technically optional, but they're there by default.  You can skip them and directly add a bumper to the farthest-out screw holes with an M3 screw and nut if you'd like.  Don't worry, you won't be judged for it.

Plus, you'll want to consider these optional STLs from a few external repos:
- [No-drop nuts](https://github.com/zruncho3d/f-zero/tree/main/STLs/NoDropNuts)
- [More M2 nutbars from V0](https://github.com/VoronDesign/Voron-0/blob/Voron0.1/STLs/M2_Nut_Adapter_Rotated_x5.stl)
- [ZeroPanels](https://github.com/zruncho3d/ZeroPanels), especially Tecnologic-style ones
- [BoxZero](https://github.com/zruncho3d/BoxZero)
