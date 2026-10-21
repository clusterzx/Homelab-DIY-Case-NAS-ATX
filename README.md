# NAS Case V4 — 4 × 3.5" SAS hot-swap, 2 × 2.5" SSD, microATX

3D-printable desktop NAS case in two screwed-together modules: a **JBOD module** at the bottom with four vertical
hot-swap 3.5" bays on a SAS backplane and two 2.5" SSD trays, and a **PC module** on top for a microATX board lying flat.
Every joint uses M3 heat-set inserts. Designed for PETG on a 340 × 320 mm bed (Bambu Lab H2S) without supports.

**Version v1.0** · outside 308 × 290 × 328 mm (W × D × H), 340 mm with feet ·
about 3.1 kg PETG if printed solid (much less with 15 % infill)

![Finished case](docs/images/title.png)

**Status:** a prototype of this case was printed and assembled. v1.0 collects every fix that came out of it (see
[CHANGELOG.md](CHANGELOG.md)). The changes are checked in the model, but v1.0 has not been printed as a complete set yet.

**Assembly guide:** [docs/Assembly_Guide_V4.pdf](docs/Assembly_Guide_V4.pdf) (also as
[Markdown](docs/Assembly_Guide_V4.md)) with exploded views, every heat-set insert per part and every assembly step with
colour-coded screws.

| Lower module (JBOD) | Upper module (PC) |
|---|---|
| ![Exploded view, lower module](docs/images/exploded_lower.png) | ![Exploded view, upper module](docs/images/exploded_upper.png) |

## Features

- **4 × 3.5" SAS/SATA hot-swap** on vertical trays (28 mm pitch) that plug into a 4-bay backplane. Trays slide in
  channels and click into a printed spring latch; pull them out by the finger hole.
- **Self-aligning backplane holder:** it hangs in slots (5 mm down, 3 mm towards the SSD bay,
  1.8 mm towards the left wall). Push one drive fully in, then tighten the four screws. Two braces behind it stop
  it from flexing when drives are inserted.
- **2 × 2.5" SSD trays** next to the drive bays.
- **Drive cooling:** a 120 mm fan under the drive floor blows up through the gaps between the drives; the air leaves
  over the ceiling and through the rear wall.
- **PC module:** microATX up to 244 × 248 mm, standard rear I/O shield, 4 expansion slots (cards go in from the top,
  bracket tabs on a printed shelf under a slot cover), CPU cooler up to 125 mm (8.4 mm left), two 120 mm side
  fans (intake left, exhaust right), 5.79" e-paper display and a 16 mm power button at the front.
- **Standard ATX power supply** (150 × 86 × 140 mm) standing on edge in the lower
  module, fan facing the right wall, full rear cut-out with the 4 standard holes.
- **Separate 12 V JBOD power:** picoPSU-160-XT with a 4-pin DIN jack at the rear. Switch it with the button of an ATX
  breakout board through the finger window (option A) or with a round rocker switch in the printed switch bezel
  (option B).
- **Tool access:** every screw is reachable with a straight hex key in the order of the assembly guide.

## Hardware this was designed around

| Part | Notes |
|---|---|
| microATX board, 244 × 248 mm | Chinese C612 board (Cloudstar). The SFF-8643 ports on this board are SATA only; SAS drives need an HBA in a PCIe slot. |
| CPU cooler | Noctua NH-U9DX i4 (125 mm) |
| ATX PSU | Seasonic Focus GX-550 (150 × 86 × 140 mm, fully modular). Any standard ATX unit 140 mm deep fits; longer units were not checked. |
| 4-bay 3.5" SAS backplane | 124 × 108 mm PCB, 28 mm drive pitch, 2 × Molex power, 4 × SATA/SAS data |
| JBOD power | picoPSU-160-XT + 12 V power brick with 4-pin DIN plug (e.g. Mean Well), ATX 24-pin breakout board **or** 24-pin jumper with latching rocker switch |
| Fans | 3 × 120 × 25 mm |
| Display | Elecrow CrowPanel ESP32 E-Paper 5.79" (DIS08792E), USB-C cable with straight plug |
| Power button | 16 mm momentary push button with LED ring, optional 5 mm LED |

## Before you print

1. **Print the gauges and test pieces first** (`stl/0_test_prints`, about 52 g):
   - `gauge_hdd` / `gauge_ssd`: lay the gauge on the side of your drive, short stop against the front, long stop
     against the PCB side. The threaded holes must show centred in both gauge holes. Only then print the trays.
   - `test_insert_holes`: melt your M3 inserts into the 3.8 / 4.0 / 4.2 / 4.4 mm holes. The model uses
     4 mm.
   - `test_tray_channel` with **one** `hdd_tray`: the tongue slides freely and the latch clicks.
   - `test_io_shield`: your board's I/O shield snaps into the 1.2 mm rim.
2. **Print settings:** PETG, 0.4 mm nozzle, 0.2 mm layers, 3 walls, 15 % infill, no supports. The files are already
   oriented. 5 mm brim for the drive tub, the mid plate and the top plate. Braces: 4 walls, 40 % infill.

## Parts

### Gauges and test prints (print these first)

| File | Qty | Size (mm) | PETG each | Orientation | Brim | Note |
|---|---|---|---|---|---|---|
| [`gauge_hdd_1x.stl`](stl/0_test_prints/gauge_hdd_1x.stl) | 1 | 16 × 127 × 7 | 7 g | flat, stops up | no | check on your drive before printing the trays |
| [`gauge_ssd_1x.stl`](stl/0_test_prints/gauge_ssd_1x.stl) | 1 | 13 × 94 × 7 | 4 g | flat, stops up | no | check on your SSD |
| [`test_insert_holes_1x.stl`](stl/0_test_prints/test_insert_holes_1x.stl) | 1 | 56 × 16 × 10 | 11 g | as exported, holes up | no | find the hole size for your inserts |
| [`test_tray_channel_1x.stl`](stl/0_test_prints/test_tray_channel_1x.stl) | 1 | 34 × 70 × 8 | 13 g | bottom down, ribs up | no | use with one HDD tray |
| [`test_io_shield_1x.stl`](stl/0_test_prints/test_io_shield_1x.stl) | 1 | 186 × 66 × 3 | 17 g | inner face down | no | does your I/O shield snap in? |

### Lower module (JBOD)

| File | Qty | Size (mm) | PETG each | Orientation | Brim | Note |
|---|---|---|---|---|---|---|
| [`bottom_plate_1x.stl`](stl/1_lower_module/bottom_plate_1x.stl) | 1 | 308 × 290 × 33 | 439 g | underside down | no |  |
| [`foot_4x.stl`](stl/1_lower_module/foot_4x.stl) | 4 | 24 × 24 × 12 | 6 g | pad recess down | no |  |
| [`drive_tub_1x.stl`](stl/1_lower_module/drive_tub_1x.stl) | 1 | 168 × 164 × 136 | 504 g | floor down, cheeks up | 5 mm |  |
| [`drive_ceiling_1x.stl`](stl/1_lower_module/drive_ceiling_1x.stl) | 1 | 125 × 156 × 7 | 87 g | top face down, ribs up | no |  |
| [`ssd_ceiling_1x.stl`](stl/1_lower_module/ssd_ceiling_1x.stl) | 1 | 35 × 114 × 5 | 17 g | top face down, rails up | no |  |
| [`backplane_holder_1x.stl`](stl/1_lower_module/backplane_holder_1x.stl) | 1 | 142 × 158 × 8 | 42 g | front face down, bosses up | no | slotted, aligns to the drives |
| [`backplane_brace_2x.stl`](stl/1_lower_module/backplane_brace_2x.stl) | 2 | 148 × 105 × 12 | 52 g | flat on its side | no | 4 walls, 40 % infill |
| [`clamp_washer_4x.stl`](stl/1_lower_module/clamp_washer_4x.stl) | 4 | 16 × 16 × 2 | 1 g | flat | no |  |
| [`front_lower_1x.stl`](stl/1_lower_module/front_lower_1x.stl) | 1 | 166 × 300 × 11 | 132 g | visible face down | no |  |
| [`rear_lower_1x.stl`](stl/1_lower_module/rear_lower_1x.stl) | 1 | 166 × 300 × 11 | 132 g | outer face down | no |  |
| [`side_left_lower_1x.stl`](stl/1_lower_module/side_left_lower_1x.stl) | 1 | 166 × 286 × 10 | 137 g | outer face down | no |  |
| [`side_right_lower_1x.stl`](stl/1_lower_module/side_right_lower_1x.stl) | 1 | 166 × 286 × 10 | 131 g | outer face down | no |  |

### Upper module (PC)

| File | Qty | Size (mm) | PETG each | Orientation | Brim | Note |
|---|---|---|---|---|---|---|
| [`mid_plate_1x.stl`](stl/2_upper_module/mid_plate_1x.stl) | 1 | 308 × 290 × 14 | 341 g | underside down, standoffs up | 5 mm |  |
| [`front_upper_1x.stl`](stl/2_upper_module/front_upper_1x.stl) | 1 | 152 × 300 × 12 | 135 g | visible face down | no |  |
| [`rear_upper_1x.stl`](stl/2_upper_module/rear_upper_1x.stl) | 1 | 152 × 300 × 11 | 89 g | outer face down | no |  |
| [`slot_shelf_1x.stl`](stl/2_upper_module/slot_shelf_1x.stl) | 1 | 104 × 8 × 6 | 5 g | wall side down | no |  |
| [`slot_cover_1x.stl`](stl/2_upper_module/slot_cover_1x.stl) | 1 | 83 × 31 × 9 | 10 g | inner face down | no |  |
| [`side_left_upper_1x.stl`](stl/2_upper_module/side_left_upper_1x.stl) | 1 | 152 × 286 × 10 | 108 g | outer face down | no |  |
| [`side_right_upper_1x.stl`](stl/2_upper_module/side_right_upper_1x.stl) | 1 | 152 × 286 × 10 | 118 g | outer face down | no |  |
| [`display_bracket_1x.stl`](stl/2_upper_module/display_bracket_1x.stl) | 1 | 212 × 12 × 4 | 13 g | flat | no |  |
| [`top_plate_1x.stl`](stl/2_upper_module/top_plate_1x.stl) | 1 | 308 × 290 × 4 | 277 g | top face down | 5 mm |  |

### Drive trays

| File | Qty | Size (mm) | PETG each | Orientation | Brim | Note |
|---|---|---|---|---|---|---|
| [`hdd_tray_4x.stl`](stl/3_drive_trays/hdd_tray_4x.stl) | 4 | 160 × 116 × 28 | 49 g | on its side | no | print one first with the channel test |
| [`ssd_tray_2x.stl`](stl/3_drive_trays/ssd_tray_2x.stl) | 2 | 113 × 76 × 15 | 11 g | on its side | no |  |
| [`accent_strip_4x.stl`](stl/3_drive_trays/accent_strip_4x.stl) | 4 | 2 × 55 × 4 | 1 g | flat, orange | no | optional, glue in |

### Options

| File | Qty | Size (mm) | PETG each | Orientation | Brim | Note |
|---|---|---|---|---|---|---|
| [`switch_bezel_1x.stl`](stl/4_options/switch_bezel_1x.stl) | 1 | 32 × 32 × 18 | 4 g | front face up | no | option B: round rocker switch instead of the breakout board button |

## Heat-set inserts and screws

All inserts: **M3 heat-set insert, about 5.7 mm long**, hole 4 mm, **61 in total**.
Each screw is listed at the part where its head sits.

| Part | Inserts | Where | Screws you drive at this part |
|---|---|---|---|
| `bottom_plate` | 5 | 5 in the fan box bosses (for the tub) | 12 × M3×8 countersunk from below → lower wall tabs; 4 × M3×8 countersunk from inside → feet; 4 × fan screw from below → drive fan |
| `foot` | 4 | 1 per foot, from the top | – |
| `drive_tub` | 10 | 6 on top of the cheek pads, 4 in the rear cheek ends | 5 × M3×10 countersunk through the floor → bottom plate bosses |
| `backplane_holder` | 0 | – | 4 × M3×12 socket head with clamp washer through the slots → tub; 8 × 3 mm self-tapping screw: backplane → holder bosses |
| `backplane_brace` | 2 | 1 at the back of each brace foot | 1 × M3×20 (any head) per brace as jack screw |
| `side_left_lower` | 7 | 3 in the lower tabs, 4 in the upper tabs | – |
| `side_right_lower` | 6 | 3 in the lower tabs, 3 in the upper tabs | – |
| `front_lower` | 5 | 2 in the lower tabs, 3 in the upper tabs | – |
| `rear_lower` | 8 | 4 in the lower tabs, 4 in the upper tabs | 4 × 6-32×6 from outside → PSU; 2 × M2.5×6 self-tapping from outside → DIN jack flange |
| `mid_plate` | 8 | 8 in the board standoffs | 6 × M3×10 countersunk → tub cheeks; 2 × M3×10 countersunk → rear lower wall; 8 × M3×6 → board |
| `side_left_upper` | 2 | 2 in the top tabs (thumb screws) | 4 × M3×20 socket head from above through the tabs and the mid plate → lower wall; 4 × fan screw from outside → case fan |
| `side_right_upper` | 2 | 2 in the top tabs (thumb screws) | 3 × M3×20 socket head from above through the tabs and the mid plate → lower wall; 4 × fan screw from outside → case fan |
| `front_upper` | 0 | – | 3 × M3×20 socket head from above through the tabs and the mid plate → lower wall |
| `rear_upper` | 2 | 2 pressed in from outside (slot shelf) | 2 × M3×20 socket head from above through the tabs and the mid plate → lower wall |
| `slot_shelf` | 0 | – | 2 × M3×10 countersunk from outside → rear upper wall |
| `slot_cover` | 0 | – | 4 × 6-32×8 through cover and bracket tab → slot shelf |
| `display_bracket` | 0 | – | 2 × M2.5×6 → display standoffs; 2 × M3×12 self-tapping → front upper bosses |
| `top_plate` | 0 | – | 4 × M3×8 thumb screw (DIN 464) → upper side walls |
| `hdd_tray` | 0 | – | 4 × 6-32 flat-head drive screw per tray |
| `ssd_tray` | 0 | – | 4 × M3×4 countersunk per tray |

### Shopping list

| Qty | Part |
|---|---|
| 61 | M3 heat-set insert, approx. 5.7 mm long |
| 16 | M3×8 countersunk (ISO 10642 / DIN 7991) |
| 15 | M3×10 countersunk (ISO 10642 / DIN 7991) |
| 12 | M3×20 socket head (ISO 4762 / DIN 912) |
| 4 | M3×12 socket head (backplane holder) |
| 2 | M3×20, any head (brace jack screws) |
| 8 | M3×6 (board) |
| 4 | M3×8 knurled thumb screw (DIN 464) |
| 2 | M3×12 self-tapping screw (display bracket) |
| 2 | M2.5×6 (display) |
| 2 | M2.5×6 self-tapping screw (DIN jack) |
| 16 | 6-32 flat-head drive screw (3.5" drives) |
| 8 | M3×4 countersunk (SSDs) |
| 4 | 6-32×6 (PSU, usually included with the PSU) |
| 4 | 6-32×8 (expansion card brackets) |
| 8 | 3 mm self-tapping screw, 8–10 mm (backplane) |
| 12 | fan screw (1 drive fan + 2 case fans) |

Tools: soldering iron with an M3 insert tip, hex keys 2 and 2.5 mm, Phillips PH1/PH2, flush cutters.

## Assembly in short

The [assembly guide](docs/Assembly_Guide_V4.pdf) shows every step. In short:

1. Melt in all 61 inserts.
2. **Lower module:** feet and drive fan onto the bottom plate, drive tub onto the fan box, backplane onto its holder,
   holder loosely onto the tub, slide in the ceilings, align the backplane with one drive and tighten the holder. JBOD
   electronics and PSU, DIN jack, the four lower walls from below, PSU from the rear, braces behind the holder, cables.
3. **Upper module:** mid plate, slot shelf, the four upper walls with 12 × M3×20 from above into the lower walls,
   then display, button and case fans, board, cards and slot cover, top plate with thumb screws.
4. Drives into the trays, slide them in until they click.

## What was checked and what was not

Checked in the parametric model (Blender/Python): no collisions between any printed parts, bought parts, screws and
plug envelopes (pairwise checks between all of them), every screw ends in an insert with material around it, every
long screw is reachable with a straight key, the backplane holder is free over its whole adjustment range, the drive fan cable
passes under the holder, PSU modular plugs (30 mm zone), mains plug and the cable path up to the board are free, trays
and drives pull out without hitting anything, every part is one solid body without unsupported flat overhangs.

Not verified on real hardware for v1.0:
- **Backplane connector position:** not dimensioned in the vendor drawings. The holder is adjustable for this reason.
  If a drive latches but does not seat fully, the drive-to-backplane depth is off (not adjustable).
- **Board standoffs** follow the microATX standard, except hole **S** (the board this was built for has a coil there)
  and an extra plain support (no insert) under a non-standard hole near the front corner on the slot side, measured
  from a photo (±1.5 mm). If your board has hole S, glue in a 10 mm M3 standoff; if the support hits a part on your
  board, cut it off.
- **ATX PSU:** outline and holes from the Intel ATX design guide; inlet and switch are inside the large rear cut-out.
- **Switch bezel (option B):** sized from measured estimates of the switch (body Ø 20 mm, ring
  Ø 25 mm, clips behind a 1.5 mm panel). It is a 4 g print, so print it and try.
- **Insert hole size** 4 mm: use the test print.

## Version history

See [CHANGELOG.md](CHANGELOG.md).
