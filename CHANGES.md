### 2022-10-16 Update:

Alpha-6.

It's about time.  Plus50, new parts, doc updates.  Details in main page.

#### 2022-04-18 BoxZero is out!

BoxZero is a T0 spinout. It doesn't require T0, but works great with it.  The tagline:

> Simplify, strengthen, and seal your Voron Zero or V0-derived printer (Tri-Zero, Double Dragon) by ditching the tophat and moving to a full-box frame.

[Check it out here](https://github.com/zruncho3d/BoxZero).

#### 2022-02-16 Update: $#!+ Just Got Real

**(1)** We have our first Voron-serial'ed Tri-Zero!  Congrats to Red5, whose black-and-blue Tri-Zero looks great and prints great:

  ![Red5](Images/red5.jpg)

Definitely check out the [serial request video for V0.1382](https://www.reddit.com/r/voroncorexy/comments/simwer/trizero_t0_serial_request_v01_red5_8573/) to see what this T0 looks like, printing.  Red5 reports:

> So far no issues at all with the layers...  I also have printed a few 120mm tall items with perfect vertical layers.

Yes, direct-drive 1.8-degree stepper motors work great in this application!  We can get away with no reduction when the bed assembly is only ~500g, unlike printers with ~1800g flying gantries.  Direct drive is simpler, more reliable, and lower-cost.

**(2)** We have our first merged Pull Requests!  Props to csch, who contributed 3 different parts in the new Mods folder.

**(3)** We have our first complete release, in Alpha-5!  This includes many new or improved parts:

**New:**
* [ZeroClick](https://github.com/zruncho3d/ZeroClick) is out now, and is the default bed-probing solution for T0.  You don't need to reprint your MiniAB shroud.

  ![Zeroclick](Renders/alpha-5/zeroclick.png)

* [ZeroPanels](https://github.com/zruncho3d/ZeroPanels) are spun out now, and are the default enclosure solution for T0.  Prints in < 2 hrs and pops on and off.
  ![Zeroclick](Renders/alpha-5/zeropanel_clip.png)
* New rear corners are in:

  ![Rear Lower](Renders/alpha-5/rear_lower.png)
  Smaller, stronger (since they mount to the frame crossmember), and now you can reuse your V0.1 inlet.

* [4.3" Waveshare Touchscreen](https://www.amazon.com/dp/B088JTD6JN) mount added: a great way to add [KlipperScreen](https://github.com/jordanruthe/KlipperScreen), which keeps getting better.  Based on Jeoje's great Voron2.4 [Touchscreen mod](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/jeoje/4.3_Inch_Touchscreen_Mount), but adapted to fit securely in a 1515 extrusion.

  ![Rear Lower](Renders/alpha-5/waveshare.png)

* [Mini 12864 Display](https://deepfriedhero.in/products/mini-12864-display) mount added: a super-affordable way to get a display you can easily read from a distance.  Based on Gola's [V0 Trident Skirt Mix](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/golas/v0-trident-skirt-mix), but sized to fit T0.  You don't need the printed corners or guitar feet on your T0 with this one; instead, you can carry over the bumpers from a V0.1.

| ![Front](Images/12864_front.jpeg) | ![Back](Images/12864_back.jpeg) |  ![Part](Images/12864_part.jpeg)
| - | - | - |

**Improved:**
* The Z Nozzle Endstop is now rear-mounted;
![Top Bed](Renders/alpha-5/top_bed_view.png)

  Modified Rear Bed Mount and Front Bed Mounts have been added to match it.  You'll lose a few mm of rear Y travel, but the positioning works much better with [Double Dragon](https://github.com/zruncho3d/double-dragon), where it enables automatic toolhead offset calibration and wider beds.
* The Rear Z Mount is now taller:

  ![Front Lower](Renders/alpha-5/front_lower.png)
  This provides 3 real benefits:
  * Motors (whether NEMA14 or NEMA17) with long shafts no longer conflict with the power supply.
  * Z motors can be removed now, even with the mount in place, as there's more clearance from the power supply for the allen wrench to get in there.
  * Your T0-in-progress can sit flat with only 3 below-deck parts: 2x MotorCorners and one Rear Z Mount.
* Front MotorSkirts now have larger cutouts to fit motors with JST pins... like mine.

What's coming next?  More community contributions, more size options, and more QoL upgrades.  Maybe even a beta release... it's starting to stabilize.  (Famous last words, you say).

As usual, all parts have been pre-oriented for easier printing, and the CAD has been updated.  Enjoy!

#### 2022-02-08 Update
* [ZeroClick](https://github.com/zruncho3d/ZeroClick) is out!  Fast & simple bed probing for tiny printers... like Klicky, but sized right.  The default now for Tri-Zero.  Actually, ZeroClick is a T0 spinoff proect, just like ZeroPanels, but since both have much broader relevance to more V0-ish printers, they live in other GitHub repositories.

#### 2022-01-23 Update
* [ZeroPanels](https://github.com/zruncho3d/ZeroPanels) are out!  These provide an option for easily enclosing your T0, while providing the additional gap needed to enable the carriages to stick out of the frame.  They pop on and off in seconds and reuse your clear panels and front printed parts from a V0.

#### 2022-01-20 Update
* T0-Alpha-4 released, with 11 new parts.
* **Now supports NEMA14 and NEMA17**: use what you've got!
  * The new MotorSkirts push the motors as far out as possible, freeing up enough space to fit larger power supplies  more easily (between motors or against the motor rear plates).  
  * The front skirt can be swapped for a [4" touchscreen mod](https://github.com/Fleafa/VoronUsers/tree/V0.1-Trident-skirt/printer_mods/roboticator24/4inch_touchscreen_mount_for_v2.4) for [KlipperScreen](https://github.com/jordanruthe/KlipperScreen).  
  * Guitar Feet (4x) can be added to give a nice handle with the skirts... or, retain the original V0 bumpers.
* New rear motor mount: now, mounts to the nuts you'd already have on a V0 if doing a conversion.  This is a huge deal!  To convert a V0, you no longer need to dissassemble the rear frame.
* New clip-in 30mm fan mounts on the sides for side-to-side airflow.
* New clip-in front motor pulley covers.  Leave them out if you want to see Z motion or put some spinners on.
* Slightly thinner rear Z idlers: now they fit within the extrusion thickness of 15mm.  Two benefits: more space for a probe back there (hint, hint) and now the center tensioner fits a regular 12mm BHCS, so no cut screw or washers are needed anymore.
* CAD and STLs for alpha-4 are now available.  The original V0.1 bed assembly is gone, for a smaller file size, but Fusion is failing to export, so .step only for this one.
* Want to contribute?  PRs would be welcome for these improvements:
  * Integrated probing solution
  * Rear side skirts with less material.  Duplicating the front skirts adds unnecesary material and gets in the way of a rear outlet.  I got tired and chose to release this instead of modding the skirt.  Other improvements matter more.
  * Integrated bed Wago mount (5x2)

#### 2022-01-16 Update:
Initial BOM posted below.  No large changes are expected, but no promises are made w/an alpha!

#### 2022-01-11 Update:
* T0-Alpha-3 released: **now with less!**
* **Now Direct-Drive** - yes, this is a huge change.  Frees up space, lower costs, and speeds up the conversion time.  And yes, regular NEMA14 motors seem to have just enough unpowered hold and enough resolution to make this work in practice.  Long (V0.1-spec) NEMA14s should be overqualified to hold the bed when the power cuts out.
* **Now using MCMBen Trident-style skirts** - these look great and enable integrated side skirts with motor mounts.  Only needs one part and its mirror to change, the front corners, to add clearance for the front belt pulleys.  See the repo for these.
* Simplified Z attachments: easier and faster to print, increases Z travel (122mm out of the box), and also removes 6 M2 screws.
* New rear motor attachment piece.  It's basically a block.
* Updated front idlers: reduces the material needed and slightly increases clearance for another mm of X travel.
* CAD and STLs for alpha-3 are now available.  GitHub limits files to 100 MB and the Fusion export is just a bit too large.  [Go here for the Fusion export](https://drive.google.com/file/d/1fiEJLRE4qYLFB2CRu8r5_06jv_Fr14W6/view?usp=sharing).
* What's coming next?
   * Redone integrated skirts.  The motors are too far inboard now, which wastes space and loads the motor bearings unnecessarily.  This was intentional, to minimize skirt changes, but if we go full-custom with the skirts, they can be more optimized for Tri-Zero.  For example, by extending beyond the frame boundary - to the enclosure boundary - it should be easier to enable NEMA17 motors.
   * A probing solution is coming, called ZeroClick, but it needs a corresponding dock created before release.
   * A rear Z motor mount that doesn't change the nut locations relative to V0.1 would be nice!
   * Lessons from Double Dragon point the way to probably 130mm Z (!) using the same rails.
   * ZeroPanels are coming soon: screwless, nutless, magnetless, toolless enclosure panels that attach and remove in seconds.
   * Maybe... just maybe... a block-and-tackle Z for 2x resolution and torque.
   * Some built-in solution for mounting Wagos under the bed.

#### 2021-11-15 Update:
* T0-Alpha-2-Green can **reliably** and automatically level itself.  Config coming soon.
* The new flexure joints beat the KGLM03 joints in smoothness, as they converge *very* quicky when doing automatic leveling, plus drop a few bucks from the cost total.
* Z has been increased to right about 120mm, and nearly all main Z motion parts had to change to enable this.
* Front idlers were narrowed a bit to avoid a tiny bit of interference in the very front of the printer.  
* CAD and STLs for alpha-2 are now available.   
* What's coming next?
  * Lessons from alpha-2 will lead to a much simpler alpha-3, likely with even taller Z (beyond 120mm).
  * Different detachable probe options are under testing, including SideSwipe and a stretched Klicky-style probe.

#### 2021-11-07 Update:
* T0-Alpha-1-Green can automatically level itself, as of today!  Images and video proof are availabe on Discord.  Real life nearly matches the CAD.
* CAD and STLs for alpha-1 now available.

## Older updates

* 2021-11-07: Alpha release now up on GitHub.
* 2021-11-06: First successful triple bed leveling, after designing a whole bunch of parts.
* 2021-11-04: After focusing on F-Zero for awhile... we’re back.
* 2021-08-15: Zruncho’s F-Zero-Black torn down to provide parts for Tri-Zero-Proto.
* 2021-08-15: Now using spherical joints.  After some discussion on #tri-zero, going to go with simple spherical joints to start, just like the announced-today Voron-Trident - a triple-Z Voron 1.8 follow-up.  If it’s good enough for that printer, it should be good enough for a much smaller printer.  Kinematic mounts can come later.  
* 2021-08-14: The unofficial DOOM-Stream went well.  Now we have a CAD!  Not complete, but still useful.  Major contributions from `l.e.o.p.a.r.d`, `Ericsson`, `Kayos Maker`, and many others on the call, to figure out how to make this happen, and whether it makes any sense at all.
* 2021-08-14: ``#tri-zero` on DoomCube Discord created - this is where design discussion will live.
