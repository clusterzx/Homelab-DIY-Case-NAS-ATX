# NAS Case V4 – Assembly Guide

**4 × 3.5" SAS hot-swap · 2 × 2.5" SSD · microATX · JBOD with picoPSU** · Version v1.0 · 2026-10-21

![The finished case](images/title.png)

A desktop case made of two screwed-together modules. **Bottom (JBOD):** four 3.5" drives standing on edge in trays that
plug into a SAS backplane, two SSD trays, the 12 V JBOD power (picoPSU) and the ATX power supply of the PC. **Top (PC):**
the microATX board lies flat, the e-paper display and the power button sit at the front. Everything is screwed together
with **M3 heat-set inserts**; nothing is only pushed together.

| | |
|---|---|
| Outside (W × D × H) | 308 × 290 × 328 mm, 340 mm with feet, about 347 mm with thumb screws |
| Drives | 4 × 3.5" SAS/SATA (28 mm pitch), 2 × 2.5" SSD |
| PC | microATX up to 244 × 248 mm, CPU cooler up to 125 mm (8.4 mm left to the top plate), standard ATX PSU 150 × 86 × 140 mm |
| Cooling | 120 mm fan under the drives, 2 × 120 mm side fans in the PC module |
| Fasteners | 61 M3 inserts, 53 M3 screws in the case (plus board, drives and bought parts) |
| Print | PETG, 3126 g if printed solid (less with infill), 13 print beds, no supports |

## 1 How to read the pictures

| Colour | Meaning |
|---|---|
| 🟦 light blue | part added in this step |
| ⬜ light grey | already mounted |
| 🟨 brass | M3 heat-set insert (drawn slightly larger) |
| 🟥 red | M3 × 8 countersunk |
| 🟩 green | M3 × 10 countersunk |
| 🟪 purple | M3 × 20 socket head |
| 🟧 orange | M3 × 12 socket head |
| 🟫 brown | M3 × 6 (board) |
| ⬛ dark grey | all other screws (fan, 6-32, M2.5, 3 mm, thumb screws) |

Screws and inserts are drawn pulled out along their axis; a thin line points into their hole. Arrows show a movement
or the direction of the air flow.

## 2 Exploded views and parts

![Exploded view, lower module (JBOD)](images/exploded_lower.png)

![Exploded view, upper module (PC)](images/exploded_upper.png)

<!-- seitenumbruch -->

**Printed parts** (folder `stl`)

| No. | Part | File | Qty | Size (mm) | PETG each |
|---|---|---|---|---|---|
| 1 | Bottom plate | `bottom_plate_1x.stl` | 1 | 308 × 290 × 33 | 439 g |
| 2 | Foot | `foot_4x.stl` | 4 | 24 × 24 × 12 | 6 g |
| 3 | Drive tub | `drive_tub_1x.stl` | 1 | 168 × 164 × 136 | 504 g |
| 4 | Drive ceiling | `drive_ceiling_1x.stl` | 1 | 125 × 156 × 7 | 87 g |
| 5 | SSD ceiling | `ssd_ceiling_1x.stl` | 1 | 35 × 114 × 5 | 17 g |
| 6 | Backplane holder | `backplane_holder_1x.stl` | 1 | 142 × 158 × 8 | 42 g |
| 7 | Side left lower | `side_left_lower_1x.stl` | 1 | 166 × 286 × 10 | 137 g |
| 8 | Side right lower | `side_right_lower_1x.stl` | 1 | 166 × 286 × 10 | 131 g |
| 9 | Front lower | `front_lower_1x.stl` | 1 | 166 × 300 × 11 | 132 g |
| 10 | Rear lower | `rear_lower_1x.stl` | 1 | 166 × 300 × 11 | 132 g |
| 11 | Mid plate | `mid_plate_1x.stl` | 1 | 308 × 290 × 14 | 341 g |
| 12 | Side left upper | `side_left_upper_1x.stl` | 1 | 152 × 286 × 10 | 108 g |
| 13 | Side right upper | `side_right_upper_1x.stl` | 1 | 152 × 286 × 10 | 118 g |
| 14 | Front upper | `front_upper_1x.stl` | 1 | 152 × 300 × 12 | 135 g |
| 15 | Rear upper | `rear_upper_1x.stl` | 1 | 152 × 300 × 11 | 89 g |
| 16 | Slot shelf | `slot_shelf_1x.stl` | 1 | 104 × 8 × 6 | 5 g |
| 17 | Slot cover | `slot_cover_1x.stl` | 1 | 83 × 31 × 9 | 10 g |
| 18 | Display bracket | `display_bracket_1x.stl` | 1 | 212 × 12 × 4 | 13 g |
| 19 | Top plate | `top_plate_1x.stl` | 1 | 308 × 290 × 4 | 277 g |
| 20 | HDD tray | `hdd_tray_4x.stl` | 4 | 160 × 116 × 28 | 49 g |
| 21 | SSD tray | `ssd_tray_2x.stl` | 2 | 113 × 76 × 15 | 11 g |
| 22 | Accent strip | `accent_strip_4x.stl` | 4 | 2 × 55 × 4 | 1 g |
| 23 | Backplane brace | `backplane_brace_2x.stl` | 2 | 148 × 105 × 12 | 52 g |
| 24 | Clamp washer | `clamp_washer_4x.stl` | 4 | 16 × 16 × 2 | 1 g |
| 25 | Switch bezel | `switch_bezel_1x.stl` | 1 | 32 × 32 × 18 | 4 g |

Parts 20–22 are shown in step 22, the braces (23) in step 11, the clamp washers (24) in step 4 and the switch bezel
(25, option B only) in step 10. Gauges and test prints: section 4.

**Bought main parts** (letters in the drawings)

| | Part |
|---|---|
| A | Fan 120 × 25 mm for the drives |
| B | 4-bay 3.5" SAS backplane (124 × 108 mm, 28 mm pitch) |
| C | Option A: ATX 24-pin breakout board with picoPSU-160-XT |
| D | ATX power supply, 150 × 86 × 140 mm (designed with a Seasonic Focus GX-550) |
| E | microATX board with CPU, cooler (Noctua NH-U9DX i4) and expansion cards (HBA) |
| F | 2 × fan 120 × 25 mm for the PC module |
| G | E-paper display Elecrow CrowPanel ESP32 5.79" (DIS08792E) |
| H | 16 mm momentary push button, optional 5 mm LED |
| I | 12 V panel jack (4-pin DIN, Kycon KPJX-PM-4S, comes with the picoPSU) |

<!-- seitenumbruch -->

## 3 Screws, inserts and tools

| Qty | Part | Colour | Used for |
|---|---|---|---|
| 61 | M3 heat-set insert, about 5.7 mm long | 🟨 | all joints of the case |
| 16 | M3 × 8 countersunk (ISO 10642) | 🟥 | lower walls, feet |
| 15 | M3 × 10 countersunk (ISO 10642) | 🟩 | tub, mid plate, slot shelf |
| 12 | M3 × 20 socket head (ISO 4762) | 🟪 | upper walls → lower walls |
| 4 | M3 × 12 socket head (ISO 4762) | 🟧 | backplane holder → tub (with clamp washers) |
| 8 | M3 × 6 (usually comes with the board or case hardware) | 🟫 | board |
| 4 | M3 × 8 knurled thumb screw (DIN 464) | ⬛ | top plate |
| 2 | M3 × 12 self-tapping screw | ⬛ | display bracket |
| 2 | M2.5 × 6 | ⬛ | display to bracket |
| 2 | M2.5 × 6 self-tapping screw | ⬛ | DIN jack |
| 16 | 6-32 flat-head drive screw, short | ⬛ | 3.5" drives |
| 8 | M3 × 4 countersunk | ⬛ | SSDs |
| 4 | 6-32 × 6 (comes with the PSU) | ⬛ | PSU |
| 4 | 6-32 × 8 | ⬛ | card brackets |
| 2 | M3 × 20, any head | ⬛ | brace jack screws |
| 8 | 3 mm self-tapping screw, 8–10 mm | ⬛ | backplane |
| 12 | fan screw | ⬛ | 3 fans |

Instead of a socket head you can use a countersunk screw of the same length with a washer (those holes are not
countersunk).

**Other small parts:** 4 rubber pads Ø 12–13 mm (into the recesses of the feet), cable ties, SFF-8643 → 4 × SATA (HBA →
backplane), power for the backplane (2 × Molex), SATA data and SATA power for the SSDs, USB-C cable with a straight plug
(display), 12 V power brick with 4-pin DIN plug (JBOD).

**Tools**
- Soldering iron, ideally with an M3 insert tip
- Hex keys 2 mm (M3 countersunk) and 2.5 mm (M3 socket head); every screw is reachable with a straight key
- Phillips PH1 and PH2, flush cutters

## 4 Before printing

**Print the gauges and test pieces first** (together about 52 g):

| File | Purpose |
|---|---|
| `gauge_hdd_1x.stl` | Hole gauge 3.5": short stop against the front of the drive, long stop against the PCB side. The threaded holes must show centred in both holes (16.9 / 118.5 mm from the front). Only then print the trays. |
| `gauge_ssd_1x.stl` | The same for the SSD (9.85 / 86.45 mm from the front) |
| `test_insert_holes_1x.stl` | Melt inserts into the 3.8 / 4.0 / 4.2 / 4.4 mm holes. All parts use 4 mm. If your inserts need a clearly different hole, use inserts that fit this size. |
| `test_tray_channel_1x.stl` | With **one** HDD tray: the tongue slides freely, the latch clicks |
| `test_io_shield_1x.stl` | Does your board's I/O shield snap into the window? |

**Print settings** for all parts: PETG, 0.4 mm nozzle, 0.2 mm layers, 3 walls, 15 % infill, **no supports**. The files
are already oriented. 5 mm brim for the drive tub, the mid plate and the top plate. Braces: 4 walls, 40 % infill.

**Print beds (340 × 320 mm):**

1. Bottom plate
2. Mid plate
3. Top plate
4. Front lower + front upper
5. Rear lower + rear upper
6. Side left lower + upper
7. Side right lower + upper
8. Drive tub + drive ceiling
9. Backplane holder + SSD ceiling
10. 4 HDD trays
11. SSD trays, display bracket, slot cover, slot shelf, feet, accent strips
12. Gauges and test prints (print first)
13. 2 braces + 4 clamp washers (+ switch bezel for option B)

<!-- seitenumbruch -->

## 5 Melting in the inserts

All **61 inserts** go into the parts before assembly. Set the soldering iron to about 230–250 °C (try it on
`test_insert_holes`), put the insert on the hole and let it sink in straight without pressure until it is flush. Press
it level with a flat surface and let it cool. An insert that went in crooked can be straightened while it is warm.

| File | Inserts | Where |
|---|---|---|
| `bottom_plate_1x.stl` | 5 | on top of the fan box bosses (for the tub) |
| `foot_4x.stl` | 1 per foot | 1 on top of each foot (4 feet) |
| `drive_tub_1x.stl` | 10 | 6 on top of the cheek pads, 4 in the rear cheek ends |
| `side_left_lower_1x.stl` | 7 | 3 bottom (opening faces down), 4 top |
| `side_right_lower_1x.stl` | 6 | 3 bottom, 3 top |
| `front_lower_1x.stl` | 5 | 2 bottom, 3 top |
| `rear_lower_1x.stl` | 8 | 4 bottom, 4 top |
| `mid_plate_1x.stl` | 8 | on top of the board standoffs |
| `side_left_upper_1x.stl` | 2 | top tabs (for the thumb screws of the top plate) |
| `side_right_upper_1x.stl` | 2 | top tabs (for the thumb screws of the top plate) |
| `rear_upper_1x.stl` | 2 | from outside into the two bosses (for the slot shelf) |
| `backplane_brace_2x.stl` | 2 | 1 at the back of each brace foot (for the jack screw) |
| **total** | **61** | |

No inserts in: ceilings, backplane holder, front upper (self-tapping screws into its bosses), slot shelf, slot cover,
display bracket, top plate and the trays.

The bottom tabs of the walls open **downwards**. Turn the wall over for these inserts.

![bottom_plate](images/inserts_bottom_plate.png) ![foot (each)](images/inserts_foot.png)

![drive_tub (from behind)](images/inserts_drive_tub.png) ![mid_plate](images/inserts_mid_plate.png)

![side_left_lower (inside)](images/inserts_side_left_lower.png) ![side_right_lower (inside)](images/inserts_side_right_lower.png)

![front_lower (inside)](images/inserts_front_lower.png) ![rear_lower (inside)](images/inserts_rear_lower.png)

![side_left_upper (inside)](images/inserts_side_left_upper.png) ![side_right_upper (inside)](images/inserts_side_right_upper.png) ![rear_upper (outside)](images/inserts_rear_upper.png)

<!-- seitenumbruch -->

## 6 Lower module (JBOD)

### Step 1 – Feet and drive fan

![Step 1](images/step01_feet_fan.png)

1. Stick the rubber pads into the recesses under the feet.
2. Hold each foot against the underside of the bottom plate, insert facing up. From the inside drive an M3 × 8
   countersunk screw through the bottom plate into the foot. **Feet first:** the fan frame later covers part of the
   screw of the front left foot.
3. Put the fan into the fan box, **air flowing upwards** (the arrow on the fan frame points up). Lead its cable to the
   pass-through at the back of the box.
4. Slide the bottom plate over the edge of the table and fix the fan from below with 4 fan screws.

**Screws:** 🟥 4 × M3 × 8 countersunk · ⬛ 4 × fan screw

### Step 2 – Drive tub

![Step 2](images/step02_drive_tub.png)

1. Put the tub onto the fan box: SSD bay on the right, channels open to the front.
2. Drive 5 × M3 × 10 countersunk from above through the tub floor into the inserts of the bosses.

**Screws:** 🟩 5 × M3 × 10 countersunk

### Step 3 – Backplane onto the holder (on the bench)

![Step 3](images/step03_backplane.png)

1. Lay the holder on the bench with its bosses facing down. The engraving **BOTTOM** on the back marks the
   lower edge.
2. Put the backplane on it, drive connectors facing up (towards the drives).
3. Drive one screw through each of the 8 tab holes into the boss underneath, hand-tight.

> The holder has bosses for both hole rows of the backplane. 8 bosses stay empty; that is intended.

**Screws:** ⬛ 8 × 3 mm self-tapping screw

### Step 4 – Holder onto the tub

![Step 4](images/step04_holder.png)

1. Hold the holder with the backplane from behind against the ends of the left and the middle cheek. It hangs
   8 mm above the bottom plate; the drive fan cable runs underneath.
2. Drive 4 × M3 × 12 socket head, each with a clamp washer, from behind through the slots into the inserts
   of the cheek ends. **Only so tight that the holder can still be moved.** It is aligned after step 5.

> Where the connectors sit on the backplane is not dimensioned in the vendor drawings. That is why the holder is
> adjustable (5 mm down, 0.4 mm up, 3 mm towards the SSD bay, 1.8 mm towards the
> left wall) and aligns itself to a drive.

**Screws:** 🟧 4 × M3 × 12 socket head · 4 clamp washers

### Step 5 – Ceilings, then align the backplane

![Step 5](images/step05_ceilings.png)

1. Slide the drive ceiling, ribs down, from the front into the grooves of the left and the middle cheek until it stops.
2. Slide the SSD ceiling the same way into the grooves above the SSD bay.

The front lower wall holds them at the front later. No screws.

**Align the backplane:** put a drive into a tray and push it slowly all the way in. Its connector pulls the backplane
and the holder into place; if it catches, guide the holder by hand from behind. Leave the drive in and tighten the 4
holder screws. Then check the other bays.

### Step 6 – JBOD electronics and power supply

![Step 6](images/step06_electronics.png)

The drives get their own 12 V supply through a picoPSU. There are two ways to switch it:

- **Option A – ATX breakout board:** plug the picoPSU onto the 24-pin socket of the breakout board and lay the board
  into the frame at the front right: **power button at the front** (behind the finger window), **voltage display on the
  right** (behind the slots in the right wall).
- **Option B – rocker switch:** leave the breakout board out. Plug the picoPSU onto the 24-pin plug of an ATX jumper
  cable with a latching rocker switch; the switch goes into the switch bezel in the finger window (step 10). Power the
  backplane from the picoPSU's own leads.

Then put the **ATX power supply** on its edge into the cradle at the rear right: fan towards the right wall, mains
inlet at the bottom, modular sockets facing forward. Plug in the modular cables now (24-pin, 8-pin EPS, SATA for the
SSDs); there are 30 mm free in front of the sockets.

No screws yet. The PSU is screwed on from behind in step 9.

### Step 7 – DIN jack into the rear lower wall

![Step 7](images/step07_din_jack.png)

1. Put the 12 V panel jack of the picoPSU from the inside into the pocket of the rear lower wall; the flange sits in the
   recess.
2. From outside drive 2 self-tapping screws M2.5 × 6 through the wall into the flange.

**Screws:** ⬛ 2 × M2.5 × 6 self-tapping

### Step 8 – Lower walls

![Step 8](images/step08_lower_walls.png)

1. Stand the four lower walls into the rim of the bottom plate, tabs inside: side left (louvres), side right
   (honeycomb grille in front of the PSU fan), rear lower (with the jack) and front lower.
2. Slide the case over the edge of the table until the countersinks at the edge of the bottom plate are free. From
   below drive 12 × M3 × 8 countersunk into the bottom tabs: left 3, right 3, front 2, rear 4.
3. Start all screws first, then tighten them.

**Screws:** 🟥 12 × M3 × 8 countersunk

### Step 9 – Screw the power supply on from behind

![Step 9](images/step09_psu.png)

1. Push the PSU fully against the rear wall. Its whole back is open through the large cut-out.
2. Drive 4 screws 6-32 × 6 from outside through the rear wall into the PSU.

**Screws:** ⬛ 4 × 6-32 × 6

### Step 10 – Option B: rocker switch in the switch bezel

![Step 10 (front lower wall, detail)](images/step10_switch_bezel.png)

Only for option B. The bezel fits a round rocker switch with a Ø 20 mm body and a Ø 25 mm
ring (seat Ø 20.4 mm, 1.5 mm thick, clips left and right).

1. Push the switch with its cable from the inside through the finger window to the front (the ring fits through the
   26 mm window).
2. Slide the bezel sideways over the wires behind the switch through its 6 mm cable slot, frame to the front.
3. Press the switch into the bezel from the front until its clips snap in. Turn the rocker the way you want it.
4. Pull the cable back inside and press the bezel with the switch into the window until both snap arms click.

To remove it, press both arms (top and bottom) towards the centre from inside and push the bezel out to the front.

### Step 11 – Braces for the backplane holder

![Step 11 (rear wall and left wall hidden)](images/step11_braces.png)

The holder is screwed only to the ends of the cheeks. Without braces its strips flex backwards when drives are pushed
in. The two triangular braces carry the load into the rear lower wall.

1. Melt the insert into the back of each brace foot. Screw an M3 × 20 in from the front until its tip is flush with
   the back.
2. Pull the drives out so the holder is relaxed.
3. Lower each brace from above to the right of the holder (behind the SSD bay), about 7 mm behind the holder. Slide it
   to the left behind the holder until it is behind its boss: the 3rd and the 6th boss, counted from the left case
   wall. If a backplane connector is in the way there, any other boss works too.
4. Push it forwards until the pockets at the top and bottom sit over the bosses and the pads rest against the holder.
5. Turn the jack screw hand-tight until it touches the rear wall. No glue needed.

![Step 11, side view](images/step11_braces_side.png)

**Inserts:** 🟨 1 per brace foot · **Screws:** ⬛ 2 × M3 × 20 (jack screw)

### Step 12 – Cables in the lower module

![Step 12](images/step12_cables_lower.png)

| From | To | Route |
|---|---|---|
| DIN jack (rear wall) | picoPSU input | right of the tub to the front |
| picoPSU / breakout board, 2 × Molex | backplane power | right of the tub to the back, behind the holder to the left |
| drive fan | fan header (breakout board, or a Molex fan adapter) | from the pass-through at the back of the fan box flat under the holder, then right |
| PSU, SATA power | SSDs | behind the SSD bay, with some slack (the trays are pulled out to plug in) |
| PSU, 24-pin + 8-pin EPS | board | up through the mid plate in step 13 |

Keep the cables flat with cable ties so they do not touch the fan or cover the vents.

<!-- seitenumbruch -->

## 7 Upper module (PC)

### Step 13 – Mid plate

![Step 13](images/step13_mid_plate.png)

1. Hold the 24-pin and 8-pin cables of the PSU up, lay the mid plate on and lead the cables through the slots on the
   right.
2. Drive 6 × M3 × 10 countersunk from above into the cheeks of the tub and 2 × M3 × 10 countersunk at the back
   into the rear lower wall.

The 8 board standoffs already carry their inserts (hole S has no standoff; there is a plain support without insert near the front corner on the slot side).

**Screws:** 🟩 8 × M3 × 10 countersunk

### Step 14 – Prepare the rear upper wall (on the bench)

![Step 14](images/step14_slot_shelf.png)

1. Hold the slot shelf against the outside of the rear upper wall, pilot holes facing up. Drive 2 × M3 × 10
   countersunk from outside into the inserts of the bosses.
2. Press the board's I/O shield into the window from the inside until it snaps in all round.

**Screws:** 🟩 2 × M3 × 10 countersunk

### Step 15 – Upper walls

![Step 15](images/step15_upper_walls.png)

1. Stand the rear upper, the front upper (still **without** display and button) and the two upper side walls (still
   **without** fans) into the rim of the mid plate, tabs inside.
2. Drive 12 × M3 × 20 from above through the bottom tabs of the upper walls and the mid plate into the inserts of
   the lower walls: left 4, right 3, front 3, rear 2. This joins the two modules.

> All 12 screws are reachable with a straight key. Mount the display and the case fans only afterwards: they sit
> above some of these screws.

**Screws:** 🟪 12 × M3 × 20 socket head

### Step 16 – Display and power button

![Step 16 (front upper only, from inside)](images/step16_display.png)

1. Push the button from the front through the round hole on the left and tighten its nut inside. Optionally a 5 mm
   LED with holder into the small hole below.
2. Lay the display into the window from the inside: USB-C socket at the bottom, the knob in the recess on the right.
   It rests against the stop rails at the top and on the left.
3. Put the display bracket behind it: 2 × M2.5 × 6 through the bracket into the middle standoffs of the display, then
   2 self-tapping screws M3 × 12 through the bracket into the bosses of the front.

**Screws:** ⬛ 2 × M2.5 × 6 · ⬛ 2 × M3 × 12 self-tapping

### Step 17 – Case fans

![Step 17 (front hidden)](images/step17_case_fans.png)

1. Hold each fan against the inside of the side wall and screw it on from outside with 4 fan screws.
2. **The left one blows in** (the arrow on the frame points into the case), **the right one blows out** (the arrow
   points to the wall).
3. Lead the cables to the fan headers of the board.

**Screws:** ⬛ 8 × fan screw

### Step 18 – Board

![Step 18](images/step18_board.png)

1. Mount CPU and cooler on the board first.
2. Put the board in at an angle: rear edge first with the connectors into the I/O shield, then lower the front.
3. Drive 8 × M3 × 6 into the inserts of the standoffs.

**Screws:** 🟫 8 × M3 × 6

### Step 19 – Expansion cards and slot cover

![Step 19 (upper left side hidden)](images/step19_cards.png)

1. Plug the cards (HBA) into the slots from above; the bracket tabs rest on the slot shelf at the back.
2. Put the slot cover from above into the gap in the rear wall. Its clamping strip lies on the tabs.
3. Drive 4 screws 6-32 × 8 through the cover and the tabs into the pilot holes of the slot shelf.

**Screws:** ⬛ 4 × 6-32 × 8

### Step 20 – Cables in the upper module

![Step 20: cable routes through the mid plate](images/step20_cable_routes.png)

| Cable | Route |
|---|---|
| HBA → backplane (SFF-8643 → 4 × SATA) | slot at the rear left, down behind the backplane holder |
| PSU → board (24-pin, 8-pin EPS) | slots on the right (already in step 13) |
| Board → SSDs (SATA data) | front slot on the left, behind the SSD bay, with slack |
| Display (USB-C) | plug straight down, in a bend through the front slot on the right; to the breakout board (option A) or a USB header of the board |
| Button, LED → front panel header | the front panel header is at the front left of the board, close to the button |
| Case fans → board | fan headers |

### Step 21 – Top plate

![Step 21](images/step21_top_plate.png)

1. Put the top plate on.
2. Turn 4 thumb screws M3 × 8 hand-tight into the top tabs of the side walls.

**Screws:** ⬛ 4 × M3 × 8 thumb screw

## 8 Drives

### Step 22 – Drives into the trays

![Step 22](images/step22_trays.png)

1. **3.5":** lay the drive between the two webs of the tray, PCB side on the left (seen from the front), connector at
   the back. Drive 2 drive screws 6-32 through the lower and 2 through the upper web; the countersunk heads sit flush.
2. **2.5":** the SSD the same way into the SSD tray, 2 × M3 × 4 countersunk at the bottom and 2 at the top.
3. Optionally glue the orange accent strips into the slot of the tray front.

**Screws:** ⬛ 16 × drive screw 6-32 · ⬛ 8 × M3 × 4 countersunk

### Step 23 – Inserting the drives

![Step 23](images/step23_insert_drives.png)

1. Push the tray into the bay until the latch clicks and the connector sits in the backplane.
2. To remove it, put a finger into the finger hole at the bottom and pull.
3. **SSDs:** push the tray in halfway, plug in data and power at the back, then push it fully in.

## 9 Operation and connections

![Front](images/controls.png)

- **Switch on the JBOD:** option A with a finger through the window at the front right onto the button of the breakout
  board, option B with the rocker switch. **Drives first, then the PC.**
- **Switch on the PC:** button at the top left of the front.
- **JBOD voltage display (option A):** through the slots at the bottom of the right wall.
- **Swap a drive:** unmount it in the system, pull it out by the finger hole, push the new one in. The case stays closed.

![Rear](images/connections.png)

- **Mains:** into the ATX power supply.
- **12 V JBOD:** power brick into the DIN jack at the rear.
- Board I/O and expansion cards as in any PC.

## 10 Maintenance

- **Board, cards:** loosen the 4 thumb screws and lift off the top plate.
- **Remove the upper module:** top plate off, remove the display with its bracket and the case fans (they sit above
  screws), unplug the cables to the lower module, then unscrew the 12 M3 × 20 and lift the upper module off.
- **Drive fan:** vacuum the dust from below through the grille. To replace it: upper module and mid plate off, front
  lower off, ceilings out, backplane cables off, unscrew the tub and lift it together with the holder.

## 11 Not verified (please check on your hardware)

1. **Insert hole** 4 mm: `test_insert_holes`.
2. **Tray channel and latch:** `test_tray_channel` with one tray.
3. **I/O shield:** `test_io_shield`.
4. **Backplane:** the connector position is not dimensioned by the vendor, so the holder is adjustable. The distance
   from the drive to the backplane (depth) is an assumption: if a drive latches but does not seat fully, please open
   an issue.
5. **Board standoffs:** microATX standard, but hole S has no standoff. The plain support near the front corner on the
   slot side was measured from a photo of one specific board (±1.5 mm).
6. **ATX power supply:** outline and holes from the Intel ATX design guide; units deeper than 140 mm were not
   checked.
7. **Switch bezel (option B):** switch dimensions are measured estimates; the bezel is a 4 g print, try it first.
8. **CPU cooler:** height and position checked against the case; clearance to RAM and VRM heatsinks on the board itself
   was not checked.
