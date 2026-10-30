# Lazy Dashboard

[Connect IQ Store](https://apps.garmin.com/apps/6b6fd786-e6ac-4419-9f56-75a55b97b7a3) · [한국어 설명서](README.ko.md) · [日本語マニュアル](README.ja.md)

![Lazy Dashboard on an Edge 1040](docs/edge1040-ride.png)

This repository holds the user manual only. Questions and bug reports: e-mail the developer at [lazyfrmr@gmail.com](mailto:lazyfrmr@gmail.com), or comment on the [introduction post](https://corearoadbike.com/board/board.php?t_id=Menu03Top1&no=2628419) (Korean cycling forum).

A Connect IQ data field for Garmin Edge. One screen shows cadence, speed, power and heart rate, your drivetrain (gears
and cross-chain guidance), wind, grade and altitude, and component batteries. Verified with SRAM AXS; Shimano Di2 gears
are supported (Di2 batteries can't be shown: Garmin doesn't give their values to apps).

> Menu names follow Garmin's English Edge owner's manuals. They may differ slightly by device and firmware.

---

## 1. Supported devices

| Device | Layout | Lazy Digits (big digit font) |
|---|---|---|
| Edge 1040 / 1050 | full | yes |
| Edge 550 / 850 | full | yes |
| Edge 1030 / 1030 Plus / 1030 Bontrager | full | no (system digits) |
| Edge 540 / 840 | compact (numbers) | yes |
| Edge 530 / 830 | compact (numbers) | no (system digits) |
| Edge 520 Plus | compact (numbers) | no (system digits) |

- **Lazy Digits** is a digit font built into the app. Set to an Asian language (Korean, Japanese, Chinese, Thai), the
  540/840, 550/850, 1040 and 1050 give Connect IQ apps small fixed-size digit fonts; with Lazy Digits the numbers stay
  big in any language. The other devices keep the same digits in every language and use the system font. The font is
  open (OFL): https://github.com/bwchae/lazy-digits
- The Edge 520 Plus doesn't give apps shifting data, so shifter batteries can't be shown (gears are). The original
  Edge 520 and the Edge 1000 aren't supported.
- Required software: Edge 1040 **31.35 or later**, 1050 / 850 / 550 **32.20 or later**. If the install asks for a
  software update, update with Garmin Express or the Edge's settings, then install again.

## 2. Install and update

1. Install Garmin's **Connect IQ** app on your phone and connect it to the Edge.
2. Search for **Lazy Dashboard** in the Connect IQ app and install it.
   Store: https://apps.garmin.com/apps/6b6fd786-e6ac-4419-9f56-75a55b97b7a3
3. The app reaches the Edge at its next phone sync. Add it to a data screen as in section 3.

Updates arrive when the Edge syncs with the phone (if automatic updates are off in the Connect IQ app, update from
there). Your settings are kept.

## 3. Add it to a data screen

**Edge 530 / 830**
1. Select **Menu > Settings > Activity Profiles** and pick a profile (e.g. Road).
2. Select **Data Screens > Add New > Data Screen**.
3. Use the arrows to choose the **one-field layout**.
4. In the data field categories select **Connect IQ > Lazy Dashboard**, then **Done**.

**Edge 1040 (and other touch units)**
1. Select the menu icon > **Activity Profiles** and pick a profile.
2. Select **Data Screens > Add New > Data Screen**.
3. Use the arrows to choose the **one-field layout** and set the field to **Connect IQ > Lazy Dashboard**.

> Use a **one-field** screen. On a screen with several fields you get the small, simple layout.

> **Keep one of your usual data screens.** If a Connect IQ field ever fails, the Edge keeps recording but the field
> stays off until the ride ends. With a regular screen next to it you just swipe and ride on.

## 4. One-time setup

- **Pair your sensors** — shifting (AXS/Di2), power meter and heart-rate strap must be in the Edge's **Sensors** list.
  Edge 1040: menu > **Sensors > Add Sensor**.
- **Enter your teeth** — in the Edge's shifting sensor settings (gear info), enter chainring and cassette teeth.
  Without them the Edge sends its defaults, so `46/15` and the gear ratio are wrong (gear numbers and cross-chain
  detection are still right). SRAM D1 has no field for this in the AXS app, so enter it on the Edge. Di2 can use the
  teeth set in E-Tube.
- **First ride** — use every gear once; the teeth are learned (per bike) and the chart and hints become exact.
- **Phone** — wind uses the weather Garmin Connect on your phone keeps on the Edge. Without a phone the wind area
  shows **No phone**. If the phone that was connected during the ride drops out, it turns into a red **No phone!** box,
  and riding off after a stop of more than 5 minutes with the phone gone for 20 s brings a **full-screen alert with a
  tone**, once (left at the café?). Tap the screen or press Back to close it; left alone, the Edge closes it after a
  while. The red **No phone!** stays until the phone connects again. Start a ride without a phone and there is no alert
  or tone, just the grey **No phone**.

## 5. Settings

**Activity Profiles > Data Screens > (the screen with Lazy Dashboard) > Connect IQ Data Fields > Lazy Dashboard**.
Selecting an item opens its list of values; picking one saves it.

| Setting | Default | What it does |
|---|---|---|
| Language | Auto | Auto (device language) / English / Korean |
| Power cell / Balance cell / Heart rate cell | Auto | What those cells show; Auto picks by sensors (below). Options include **NP** (normalized power, from 30 s into the ride; it starts over if the field is restarted mid-ride) |
| Distance cell | Auto | The distance cell at the lower left. Without a course: the ridden distance. Following a course, **Auto** shows the next course point (name and distance; the destination when the course has none) while you ride, and the distance to the destination when you stop (lights, rests). It can be fixed to **Ridden distance / To destination / Next course point**. Off the course (more than 30 m for 5 s) it shows the distance back to it in orange, unless fixed to ridden distance. A bar along the bottom shows the ridden share in green, the next course point as a black post with white edges and a chequered finish. Within 1 km the next course point is shown in metres, with a small "m" after the number ("350m"; the off-course distance and a next-course-point cell above too). The three cells above also offer ridden distance and next course point, to mix and match |
| FTP | 200 W | **Set your own FTP.** Power zone colours and the threshold tick. Phone: any value 50-600 W; Edge menu: the current value +-75 W in 5 W steps (reopen at the end of the list to go further) |
| Cadence red below | 65 rpm | Red below this; also the easier-gear hint threshold |
| Cadence green from / to | 70 / 95 rpm | Target cadence band |
| Speed dial max | 60 km/h | End of the speed scale |
| Cross-chain warning / cogs | On / 2 | Big ring on the 2 largest cogs, small ring on the 2 smallest = cross-chained |
| Shift hint after | 3 s | Green hint once cross-chained this long |
| Cross-chain pop-up | after 10 s | Pop-up if it lasts; 0 = off |
| Easier-gear hint | On | Cadence coaching (below) |
| BLE battery scan | On | Reads AXS battery %; off saves battery |
| Record to FIT | On | Component batteries and cross-chain time in the activity's FIT file. Garmin limits the developer fields of one activity, shared by every Connect IQ data field on it, so with several recording data fields Lazy Dashboard can stop right at the start. Turn this off then (applies the next time the field starts) |
| Battery row | All sensors | "Drivetrain + power meter only" shows shifters, derailleurs and the power meter and hides radar / speed / cadence sensors (bigger icons). FIT recording unchanged |

**Auto cells**
The performance zone on top (rows 1-2) arranges itself by the sensors connected (when the power and heart rate cells
are both Auto):
- Left (arc): cadence, else 3s power, else heart rate, else just speed, bigger.
- Centre: whichever of power / heart rate isn't on the left; a single one gets total ascent below it; with neither,
  avg speed (plus avg cadence with a cadence sensor) and ascent.
- For the first 90 s of a ride the last ride's sensors are assumed, so the screen doesn't jump while sensors connect.
- Power and cadence, once seen, keep their place until the ride ends (even at 0 W downhill). Heart rate gives way
  after 1 minute without a value (strap off, watch broadcast switched off) and comes back when the Edge reconnects it.
- Balance cell: altitude. (Grade is always in the attitude indicator below, on every device.)

## 6. Reading the screen

### Full layout (1040, 1030, 1050, 550, 850)
```
 cadence arc  | 3s power W  ###o  | speed arc
    88 rpm    | heart rate bpm #o#|  32.5 km/h
 ---------------------------------------------
 46/15  2/2   sprocket chart + arrows
 3.07   7/12
 ---------------------------------------------
 distance+track | attitude (grade) + wind | altitude+profile
 time of day    |                         | timer
 ---------------------------------------------
 L R FD RD PM batteries     (bottom bar: Edge battery %)
```
- **Cadence and speed arcs** fill from the outside in. Cadence colours: red (low) / orange / green (target).
  Magenta wedge inside the arc = ride average, also as a small magenta number above the unit ("AVG 29.9").
  **Stopped** (lights, a break, paused timer), the big cadence, speed and power numbers show the ride averages, the
  unit tagged "AVG"; the power caption adds the ride's NP so far ("AVG W | NP 163"). Heart rate stays live, so you
  can watch it recover.
  An average speed cell (e.g. without power and heart rate sensors) would repeat the speed dial, so while stopped it
  shows how long you have been **STOPPED** - handy for keeping breaks short.
- **3s power and heart rate** — the bar colour under the big number is the current zone (blue, green, orange, red,
  purple); the tick is FTP (HR: threshold); the magenta wedge above the bar is the average.
- **Attitude indicator** — the ground rises to the right on climbs (3x exaggerated); the number below is grade %,
  shifted towards the deeper ground. The yellow level ticks at the edges show only where they aren't buried in the
  ground (both when nearly level).
- **Temperature and wind** — "TEMP" on the left of the sky is the Edge's thermometer (the same sensor as its own
  Temperature field; the phone's weather if there is none), "WIND" on the right the arrow relative to your travel.
  Standing in the sun, the thermometer can read higher than the air.
- **Rider (orange)** — the legs swap every second while you pedal. Stopped, the rider puts the left foot down;
  after 5 minutes stopped (longer than a red light), the rider gets off and sits on a chair, legs crossed.
- **Wind** — up = your direction of travel. The arrow in the sky above the rider points the way the wind blows; the
  stronger the wind, the thicker the arrow. Red headwind / orange crosswind / green tailwind. No speed number: Garmin's
  weather is one nearby station's mean wind, updated about hourly and without gusts, so it reads well below what you feel. Below 1.5 m/s (light air) a small **arrowhead inside a ring** is shown, in teal.
  Wind comes from the weather your phone keeps on the Edge, so it changes every few tens of minutes to an hour - it
  is not a measurement of the gusts you ride through.

### Compact layout (530, 830, 540, 840)
Numbers on top (cadence | speed, power | heart rate, drivetrain), and the same environment panel as the full layout
below (distance / time | attitude + wind | altitude / timer; the clock is on the left so the Edge's radar bar on the
right edge can't hide its minutes). The attitude indicator is monochrome (grey ground only) so
the numbers stand out; only the wind arrow is coloured. The cadence number is coloured by its band.

### Drivetrain (all devices)
- **46/15** — current chainring/cog teeth. **3.07** — gear ratio (one crank turn ≈ three wheel turns).
- **2/2, 7/12** — front gear / rear gear (rear: the largest cog is 1).
- **Green arrow + `Shift to Green`** — cross-chained; shift to the gear drawn in green.
- **Orange arrow + `Shift easier`** — cadence has been below the red line for 8 s on a climb (2 % or more) or into a
  strong headwind. Shift one gear easier; the 8 s restart after any shift. With a power meter only while you push
  (60 % of FTP or more); headwind only after 2 min without stopping. Not shown on flat city riding or at the lights.

### Mechanical groupsets
Without electronic shifting (AXS / Di2) data the drivetrain row changes:
- With cadence (a cadence sensor or a power meter): on the left the **estimated gear ratio** (from speed and cadence,
  approximate, 700c wheel) and the **distance per crank turn**; on the right the target cadence band, or the
  **orange arrow + Shift easier** after 8 s of low cadence.
- Without cadence: max speed | calories.

### Batteries
- Components: **L, R** shifters, **FD, RD** derailleurs, **PM** power meter, **RDR** radar (radar tail lights too),
  **SPD** speed and **CAD** cadence sensors.
- Nothing to set up: a cell appears only for sensors paired with the Edge **and connected now**.
- When cells run short, the healthy ones fold into one **`OK 6`** chip on the right (inverted box, number = count);
  only the ones worth a look keep their own cell.
- Grey **`?`**: a sensor that was connected this ride (or in a ride that ended under 10 min ago) is gone now —
  switched off or its battery ran out.
- Colours: green good / orange OK / red replace. Icons while riding, voltage / % when stopped.
- Not readable: heart-rate straps, Bluetooth-only sensors, Di2 — check those on the Edge's sensor page.
- Bottom bar: the **Edge's own battery** %. Green from 30 %, orange from 15 %, red below.
- Di2: shows `Di2 batt: Edge sensor page` — check Di2 batteries on Garmin's own sensor page.

## 7. Troubleshooting

| Problem | Check |
|---|---|
| Won't install / asks for a software update | The Edge's software version (section 1); update, then install again |
| Not in the Connect IQ list | Has the Edge synced with the phone (not still pending in the Connect IQ app)? |
| Next course point shows a street name | With turn guidance on, the Edge's turns become the "next point". Turn it off to see only course points |
| Course point names cut short | Garmin Connect stores 16 bytes of a name (about 5 Korean characters); keep names short |
| Small layout shows | It must be on a one-field layout |
| No gears | Electronic: pair the shifting sensor. Mechanical: see "Mechanical groupsets" |
| Wrong teeth / ratio | Enter teeth in the Edge's sensor settings, then use each gear once |
| Wind shows `--` | Phone connected; riding faster than 5 km/h (needs a heading) |
| Sweat or rain swapped the field for another one | The touchscreen took it for a long press. On sweaty or rainy days **lock the screen** (touch units: press the power key during an activity to lock / unlock). Put Lazy Dashboard back in the data screen editor |
| Only an IQ logo right from the start (other Connect IQ data fields in use) | The data fields together ran out of the activity's FIT developer fields. Turn **Record to FIT** off in the settings, or use fewer Connect IQ data fields in that activity profile |
| Only an IQ logo mid-ride | The field stopped on an error. Your ride is still recorded: swipe to a regular screen and ride on. See "Restarting it mid-ride" below to bring it back without ending the ride. Please send the developer the `CIQ_LOG` file (`.YML` or `.BAK`) from `Garmin\Apps\LOGS\` |
| Blank or blue field | Tell the developer (photo of the device and screen) |

### Restarting it mid-ride
If the field stopped and only an IQ logo is left, you can bring Lazy Dashboard back without stopping the recording:
open the data screen editor and back out **without changing anything**. Menu names follow Garmin's English owner's
manuals ("Editing a Data Screen").

| Device | Path |
|---|---|
| Edge 1040, 840, 540, 550, 850 | menu icon > **Activity Profiles** > (current profile) > **Data Screens** > (the Lazy Dashboard screen) > **Layout and Data Fields** |
| Edge 530, 830 | **Menu > Settings > Activity Profiles** > (current profile) > **Data Screens** > (the Lazy Dashboard screen) > **Layout and Data Fields** |

- Touch units: tap the screen to open the menu, and press **Back** a few times from the layout screen to return to the ride.
- Button units (530, 540 and others): open the menu with the buttons, go the same way and leave with the back button.
  On the layout screen the up / down buttons change the layout, so press only back there.
- Verified on the Edge 1040; other units should behave the same (the data screen is loaded again).
- After the restart, values the Edge computes (distance, averages, ascent) carry on; what the dashboard collects
  itself (the track sketch, sensor history) starts afresh from that point.
