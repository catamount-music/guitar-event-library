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

## Chukka

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-010 | technique | chukka | Chukka | chuc, chuk, chuhk, chuck | chug |

A chukka is played by muting the strings so they don't ring out in any way, then strumming the strings rapidly enough so you don't hear individual string strikes. This creates a "chukk" sound. If the chukk is the downstroke, the "a" is the upstroke. When it is played the same way, the down up pair is called a chukka. 

It is related to a chug in that it is a percussive technique. When played in syncopation with extremely staccato pressure on the frets to create a brief chord, complex rhythms can evolve.

## Chug

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-010 | technique | chug | Chug |   | Chukka, djent |

A chug occurs when you strike the strings with them simultaneously palm-muted. While in some cases the muting can be done in other ways (like muting at the headstock/nut for open string runs) it is most commonly palm muting on the bottom three strings (low E, A, and D in standard tuning)

Chugging is a rhythmic expression that uses patterns of the basic chug to create structure. In metal, this is best exemplified by the `djent` style.

## 3NPS ("Three Notes Per String")

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-011 | technique | 3nps | 3NPS |    | scales |

A 3NPS scale is one where there are always three notes on each string. They can be tricky, especially on the lower frets, because they frequntly require a 5 fret span, which is a relatively longer distance when located on the lower frets near the headstock. 

There are healthy debates about whether 3NPS scales are better and others. Ultimately, the scale patterns are the same, it just how they are played that varies, and most guitarists would do well to try and practice all variations because the have different utility in different situations. 3NPS scales are great for legato, hammer-on, pullof, and speed, because they ahve a unifying cadence across all strings. The only thing that sucks about it is that alternate picking with 3NPS requires you to learn some patterns for moving from string to string.

## Inside Picking

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-012 | technique | inside-picking | Inside Picking | | outside-picking, economy picking, alternate-picking |

Inside picking occurs when a series of notes falls on two adjecent strings and the passage is played by attacking each string from inside the gap between them. The pick always starts from "inside" the strings.

## Outside Picking

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-013 | technique | outside-picking | Outside Picking |  | inside-picking, economy-picking, alternate-picking |

Outside picking occurs when a series of notes falls on two adjacent strings and the passage is played by attacking each string from ouside the gap between them. The pick always starts from "outside" the strings.

## Economy Picking

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-014 | technique | economy-picking | Economy Picking | | inside-picking, outside-picking, alternate-picking |  

Economy picking is using the most efficient technique to play a phrase of notes. The classic example of this is using alternate picking but adding a sweep pick motion for any string change that occurs in the same direction as the pick motion. The notion of economy comes from minimizing the number of times the guitarist has to perform an awkward note to note transition, such as downstrokes on two different strings at high speed.


## Alternate Picking

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-014 | technique | alternate-picking | Alternate Picking | | inside-picking, outside-picking, economy-picking |  

Alternate picking is a technique where the pick is always alternating between downstroke and upstroke, no matter where the notes need to be played on the neck. This creates challenging situations, particularly around string switching, where it is sometime natural and faster to break the alternation. But a purist would require strict alternation on every note.

## Galloping

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-015 | technique | gallop | Galloping  |  | | 

Description
Credit Ben Eller on this one, I didn't realize it was a thing. Galloping is a rhythmic technique that combines playing chugs in doublets, triplets, or other arrangements to create a rhythmic sound that mimics galloping.

## Dive bomb

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-016 | tecnnique | dive-bomb | Dive Bomb | | Tremolo bar |

A dive bomb is when you play a string, often an open, middle string like the G, and then press the tremolo bar down sharply towards the guitar, causing the strings to loosen and the pitch of that played string to drop down into the bass range. With a locking tremolo, the strings can be made so loose they don't vibrate and sometimes get stuck to the pickups due to magnetic attraction. The sound mimics the tropey version of an old-school falling bomb, that makes a trebly sound that drops in pitch as it descends towards the earth. And the loosening strings hitting the pickups can sound like the explosion as well.

## Bigsby Tremolo

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-017 | technique | bigsby-tremolo | Bigsby Tremolo | | tremolo-bar |

A Bigsby Tremolo is a bar that uses a moving roller to raise and lower the string tension creating the tremolo effect. A Bigsby Tremolo bar has a much narrower range than a spring-loaded tremolo, and is used for shallower tremolo effects. Like most tremolo systems, a Bigsby Tremolo affects tuning stability and can create pings and knocks from the strings moving around on the tremolo bar. A Bigsby tremolo bar cannot be used in a highly aggressivce manor and is not appropriate for most hard rock and metal and a much greater range of tremolo is needed.

Description

## Legato

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-018 | technique | legato | Legato | | |

Legato has a specific meaning as a guitar technique. While it canonically means playing smoothly articulated lead lines that are connected and fluid, in the guitar world, it also means doing that with only the fret-hand. Legato is a left-hand technique (for right-handed players) or a right-handed technique for left-handed players. With legato, you use the hammer-on, pull-off technique to create all the notes, but the pull-offs are done from one finger to the next on the fretting hand. Legato requires building hand muscle strength, especially for first-finger hammer-ons and pinky pull-offs.

## Hammer On

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-019 | technique | hammer-on | Hammer On | | legato |


A hammer-on is when you play the note by striking and holding the string against the fretboard without using a pick - using only the finger tip. It can be played with either hand. To make hammer-ons effective, they must be played close to the fret with a sharp, striking motion. Compression is often used in the signal chain to help smooth out the sound and raise the levels of the quieter notes.

## Pull Off

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-020 | technique | pull-off | Pull Off | | legato  |

A pull-off is when a note is played by pulling up or down on the string with a finger, usually on the fretting hand, and then releasing it. The note is thus played without a pick. Pull-offs can be done with the picking hand. In that case, a finger on the picking hand will usually hammer-on the note and then pull-off to the next note.

## 

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL- |  |  |  | |  |  |

Description

## 

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL- |  |  |  | |  |  |

Description

Description

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
