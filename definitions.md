# Event Dictionary

## Proposed fields

**Note:** These don't all exist at the start, but may hopefully be filled in over time.

| Field | Definition | Purpose |
|---|---|---|
| GEL-ID	| A unique serial number (e.g., GEL-005).	| Permanent reference for code and experiments |
| Class	| The "Bucket" (e.g., Physical, Electrical, Artifact, Environmental).	| High-level taxonomy for filtering the dataset. |
| Definition	| A 1-2 sentence description of the physical/mechanical cause.	| Human-readable "Dictionary" entry. |
| Acoustic Signature	| Description of the sound (timbre, duration, pitch).	| Useful for manual labeling and "ear-testing" your rig. |
| Signal Data (BNC)	| The "Voltage View" (Peak mV, waveform shape, noise floor).	| Hard data for your Oscilloscope and hardware testing. |
| Spectral Profile	| Frequency range (e.g., 200Hz - 5kHz) and harmonic density.	| The electrical characteristics of the signal |
| Provenance Note	| How this event relates to C2PA, authenticity, or consent.	| Connects the sound to provenance |

## Terms

### Bell Harmonic

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-001 | technique | bell-harmonic | Bell Harmonic | | pinch-harmonic |

A bell harmonic is a bell-like sound make by creating standing waves in the guitar string. This is achieved by placing the tip of a finger (or other object, but finder is most common) at an even interval of the string length (half, third, quarter) and then plucking the string.
The finger is effectively creating a node where vibration is minimal, which suppresses the primary note vibration, leaving a harmonic series rooted in the bell harmonic.

Bell harmonics are typically played with a left-hand (pluck) / right-hand (finger over node) combination, but they can be played in a variety of ways, including

* picking hand only (index or other finger not used for holding the pick is positioned over the node.
* picking and fretting hand (fretting hand over the node, picking hand strikes string)
* fretting hand only (in the fretting hand, one finger is held over the node while another plucks the string. Yes, this is possible and pretty asesome, but uncommon.

## Pinch Harmonic

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-002 | technique | pinch-harmonic | Pinch Harmonic | pick squeal | bell-harmonic |

Pinch harmonics are typically played with the picking hand only. Usually, the thumb is used to strike the string just after the note is plucked. This creates an extremly short standing wave that has a very high pitch.
While audible at normal volume, pinch harmonics are typically played with compression and distortion, which allows for the lower standing wave signal to be heard at loud volume, causing a distinct squeal kind of noise with a pitch.

## Afterlength

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-003 | physical | afterlength | Afterlength |  | bridge-length |

The `afterlength` is the section of the strings between the nut and tuning machines. It makes a plasticy, trebly sound when plucked or picked that has extremely low sustain due to the shortness of the length of strings. Striking the afterlength also tends to produce and extremely quiet signal in an electric guitar, because the part of the strings that is vibrating does not occur over a pickup. 

There is no afterlength on a headless guitar (a guitar without a headstock).

## Bridge Length

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-004 | physical | bridge-length | Bridge Length |  | after-length |

Bridge length is similar to after length. It is any section of exposed string that runs between the bridge and tailstop. Bridge length does not occur on all guitars - it depends on the bridge design. Bridge length strikes tend to be more audible than afterlength, because they are closer to the pickups and electronics, and because the bridge is mechanically cricital to the transfer of vibration to the instrument (and likely also grounded).

## Pick Slide

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-005 | technique | pick-slide | Pick Slide | Pick Scrape |  |

A pick slide occurs when the edge of the pick (plectrum) is run along the wound strings, creating a loud, harsh, grinding sound.

## Tap Harmonic

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-006 | technique | tap-harmonic | Tap Harmonic |  |  |

A tap harmonic creates a similar sound to the bell harmonic, but is created through a different physical process. Instead of having one fingertip suppress string vibration on a node while the string is plucked, a tap harmonic happens as a result of the impact of the finger on the string. A tap harmonic occurs when the player taps the fret that occurs at one of the strong harmonic nodes. (12th, 7th, and 5th frets). If the tap is possitioned right over the fret and is extremely quick, it activates the string and creates a standing wave with a node at the fret being tapped. The result is a bell harmonic that includes a transient (the tap of the finger on the string). 

The location of the harmonic nodes can be changed by shortening the string length. If the player, for example, puts a barre on the first fret, all the harmonic node locations will change. They may or may not line up exactly with frets, depending on the location of the barre.

## Barre

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-008 | technique | barre | Barre |  |  |

A barre occurs when the fetting hand plays a chord shape with no open strings - all strings vibrate. A simple bar occurs when one picks a free and places a finger over all the strings on that fret.

The F barre chord is notorious for being the most difficult chord to play for beginners. String tension is higher near the headstock, and it takes a lot more force to press down to cleanly articulate a note on every string in this position.

## Barre Chords

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-009 | technique | barre-chords | Barre Chords |  |  |

A barre chord is a chord that includes a barre, or a finger that is placed vertically across the guitar neck, articulating a note on every string. The open chord "e" shape is the most commonly used and named barre chord. It is played with just three fingers in the open position, but the addition of the first finger barre allows the chord to be moved up and down the next in any position changing just the root note of the chord.

---
## Additional Sources

Other references, aside from [Wikipedia](https://wikipedia.com).

* [Guitar Scholar](https://www.guitarscholar.co.uk/dictionary/)
* [Guitar Gear Finder](https://guitargearfinder.com/guides/guitar-glossary-of-terms/)
* [Mel Bay Glossary of Guitar Terms](https://www.melbay.com/pages/about/glossary_of_guitar_terms/)

---
<p align="left">
  <img src="assets/name%2Blogo-black-transparent.png" alt="Catamount Music Logo" width="400">
</p>    

*Copyright © 2026 Catamount Music. All rights reserved.*
