# Downbeat — Quick Reference

Load a backing track, set its tempo, lock the beat grid, then play guitar along. The app listens through the microphone and tells you whether each strum landed early, late, or on the beat.

**Basic workflow:** load a track → set tempo → press Play → tap "Set beat 1 now" on a downbeat → enable the mic → play.

---

## 1 · Track

| Control | What it does |
|---|---|
| **Choose File** | Loads your backing track (mp3, wav, m4a, etc.). Beat 1 is automatically set to the first sound in the file. |
| **Tempo (number box)** | Shows the current BPM. Tap it and type a value directly (30–300). The label above it shows what one "beat" means for the selected time signature (see below). |
| **− / +** | Nudges the tempo down or up by 1 BPM. |
| **Time signature** | 2/4, 3/4, 4/4, 5/4, 6/8, 7/8, 9/8, 12/8. Sets the beats per measure, which click is accented, and what a "beat" is: a **quarter note** in 2/4, 3/4, 4/4 and 5/4; a **dotted quarter** in 6/8, 9/8 and 12/8 (so 6/8 has 2 beats per measure); an **eighth note** in 7/8. The tempo, click and flashing light all follow this beat. |
| **Auto-detect tempo** | Analyzes the audio and fills in a best-guess BPM. Check it against the music and adjust if needed. In 6/8, 9/8 or 12/8, if the number is about 3x what you count as a beat, divide it by 3. |
| **Tap tempo** | Tap repeatedly along with the music to set the BPM by hand. Resets after 2 seconds of no taps. |

## 2 · Play

| Control | What it does |
|---|---|
| **Play / Pause** | Starts or pauses the track. |
| **Beat light** | Flashes on every beat (brighter on beat 1). You can also **tap it** to re-lock beat 1 (same as "Set beat 1 now"). |
| **Measure : beat counter** | Shows where you are in the song, e.g. `12 : 3` = measure 12, beat 3. |
| **Set beat 1 now** | Tap right as a downbeat hits to anchor the timing grid to the real music. You can re-tap any time to correct it. |
| **Metronome click** (checkbox) | Turns the audible click on or off. Beat 1 gets a higher, louder click. |
| **Click volume** | Volume of the metronome click (default: half). |
| **Track volume** | Volume of the backing track (default: half). |
| **⏮ (restart)** | Jumps to the start, re-anchors beat 1 to the first sound, and plays. |
| **Scrub bar** | Shows playback position; drag to jump to another spot. |

## 3 · Play along

| Control | What it does |
|---|---|
| **Enable / Disable microphone** | Turns mic listening on or off. Your browser will ask for permission the first time. |
| **Reset stats** | Clears the notes-heard count, averages, and history dots. |
| **Microphone input** (dropdown) | Appears only when more than one input is available (for example the iPad's built-in mic plus a headset). Pick which one to use. It refreshes automatically when you plug or unplug a device. |
| **Mic boost** | Amplifies the raw mic signal before anything else processes it, from 1.0x (off) up to 10x. Use this when a mic is just quiet overall — a wired headset's inline mic, for instance, is built for voice close to your mouth and often picks up a guitar held at a normal playing distance far too faintly. Raise it while watching the input level bar until strums register clearly. Leave it at 1.0x for a mic that's already reading at a normal level, like the iPad's own mic. |
| **Cancel track echo** (checkbox) | Reduces the backing track leaking into the mic when you use the speaker. On iPad this can lower the track volume while you play, since iOS treats it like a voice call. Leave it off if you use headphones — if a headset mic seems too quiet, try Mic boost instead of this. |
| **Timing tolerance** | How close counts as "on the beat": **Tight** ±40ms, **Normal** ±70ms, **Loose** ±100ms. |
| **Note grid** | Which timing targets your notes are measured against, in terms of the beat. The choices change with the time signature. **Simple time** (2/4, 3/4, 4/4, 5/4): Quarter notes, Eighth notes, Eighth-note triplets, Sixteenth notes. **Compound time** (6/8, 9/8, 12/8): Dotted-quarter beats, Eighth notes (3 per beat), Sixteenth notes (6 per beat). **7/8**: Eighth notes, Sixteenth notes. Affects scoring only; the click and light stay on the beat. If the targets end up closer together than twice your tolerance, a warning appears, since everything would read "On beat." |
| **Sensitivity** | How big a rise in volume, relative to background noise, counts as a note: **Low** (loud or close mic), **Medium**, **High** (quiet or distant mic). This works on the signal *after* Mic boost — if a mic is so quiet that even High sensitivity isn't catching anything, raise Mic boost first, then adjust sensitivity. |

**What you see while playing**

- **Input level bar** — live mic volume. If it never moves, the app isn't hearing anything.
- **Gauge and verdict text** — inside your tolerance window the needle stays centered and it says **On beat**. Outside, it shows how many ms past the tolerance edge you were, and whether early or late.
- **Avg offset** — your average timing drift (negative = early, positive = late).
- **On-beat rate** — percentage of notes within tolerance.
- **Notes heard** — total strums detected this session.
- **Dots** — recent notes: teal = on beat, red = off.

## 4 · Settings

| Control | What it does |
|---|---|
| **Test speaker (beep)** | Plays a short tone so you can confirm audio output works. Also shows the audio engine's state. |
| **Calibrate latency** | Plays a few clicks through the speaker, listens for them with the mic, and measures your device's round-trip audio delay. Run with the mic on, using the speaker (not headphones), and stay quiet. |
| **Manual offset (ms)** | The delay correction subtracted from every reading (default 78). Type your own value, or let Calibrate fill it in. Use it when readings are consistently early or late by about the same amount. |
| **Show debug info** (checkbox) | Reveals a live readout (input level, detection values) and a log of every detected note with its raw timing. Useful for screen-recording a problem. |

---

## Tips

- **Headphones or wired earbuds** work best for the track: no echo, and no bleed into the mic. Wireless earbuds route the mic over Bluetooth, which adds lag and lowers quality.
- **Mic stops responding?** Reload the page. iOS audio sessions can get stuck after switching devices or toggling settings.
- **Timing consistently off by the same amount?** That's latency. Use Calibrate latency or the manual offset.
- **Timing swinging around?** Check that beat 1 is set accurately, that the BPM is right, and that the note grid matches how you're playing.
