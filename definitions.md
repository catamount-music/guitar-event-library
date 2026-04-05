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

## Chicken Picking

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-021 | technique | chicken-picking | Chicken Picking | |

The chicken picking technique is named after the sound of one of its' principal movements. Chicken picking is alternating staccato notes that are picked and plucked with the fingers. The cononical chicken picking sound mimics clucking or the "bawk-bawk" sound of a chicken when the pick strikes a note on a string which is the immediately palm muted, followed by the pick-hand fingers pulling sharply on another string, almost slapping it back onto the neck, to create the second note, which is then also immediately palm muted. While there are many more complicated patterns, this kind of syncopated alternation between a strongly picked note and other notes "plucked" with the fingers creates a distinction sound that is a staple, particularly in country music and bluegrass.

## Palm Mute

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-022 | technical | palm-mute | Palm Mute | |

A palm mute is when you press the palm of your hand over the strings right where they meet the rollers, tailstop, or bridge. Palm muting allows for a rich transient attack with a very short decay to quiet, perfect for creating rhythmic sequences and gallops. The level of muting can be adjusted by how close the palm is to the strings at the bridge. In addtion, the palm mute is typically applied from low to high strings as a generate purpose mute during playing. For example, a passage that starts out with power chords on the first few frets of the neck that eventually turns into a lead line on the higher strings. The palm mute will cover the bottom three strings for that first passage, and then move up, covering more strings as the score move to a higher pitched passage.

## False Start

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-023 | technique | false-start | False Start | | |

A false start happens when beginning a song or starting a passage. Although  making a mistake is not required, it is typically the reason the false start behavior develops. In a false start, the player realizes immediately that they do not wish to continue playing and simply stop playing the passage, resting briefly, then starting again. I suppose it is not tecnically required to play the passage again for it to be a false start. ONe could simply give up after the attempt and it might be called just a failed attempt at a song. But a false start is usually immediately followed by another attempt.

False starts in an ensemble setting are trickier. Often, once does not have the luxury of stopping, and having "broken" from the stream of musical consciousness due to the mistake, you have to slam your way back into the song at the right moment while simlutaneously attempting to regain your composure.

## E Flat Tuning

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-024 | tuning | e-flat-tuning | E Flat Tuning | |

Made popular by Eddie Van Halen (EVH), E flat tuning involves tuning the guitar to E flat versus E, unsurprisingly. The story goes that EVH thought it sounded nastier, more evil, so he always tuned his guitar down a half step. The annoying thing about E flat tuning is that most tuners default to sharps, not flats, so instead of tuning to Eb, Ab, Db, Gb, Bb, and Eb, you are actually tuning to D#, G#, C#, F#, A#, and D#. But you are a pro, so you can handle that.

## String Bend

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-025 | technique | string-bend | String Bend | Boomer bend, fretting out |

As the name suggesting, string bending is when you raise (or lower) the pitch of the string you are playing by bending it away from its' resting place, either up or down the fretboard of the guitar. Typically, you bend up on the high strings and down on the low strings, or put another way, you bend in the direction where there is more fretboard to bend. Bending up versus down sounds different. There are also reverse bends, where you mute the string, bend it, then strike it at the higher pitch and release the bend, causing it to "bend down". 

Modern bends are often acheived by ultra fast fret slides - this is a more contemporary sound. Old school bends are called "boomer bends" and usually involve bending the note at least two semitones and finishing it with a wide vibrator. This is easiest to do on a shorter scale guitar, like a Gibson Les Paul.

## Noodling

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-026 | playing mode | noodling | Noodling | | Improvisation |

Noodling is one of the hardest terms to define because when someone is noodling, it can sound just like improvisation, or workshopping. The general idea is that noodling is undirected, casual playing of the instrument that lacks structure and context, although it may drift in and out of different musical styles. For guitarists, playing meaningless notes in the pentatonic scale is one canonical form of noodling. The guitarist doesn't even have to respect the number of bars in the form - they can just pick away, playing the blues box, stopping and starting, and generally meandering around. This is noodling.

## Scales

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-027 | technique | scales | Scales |  |  |

A scale is a sequence of notes, typically from a root note across one or two octaves following a common patterns. The major scale pattern defines not only the major scale, but all the modes in western music. Each of those modes becomes a scale. Likewise, there are pentatonic scales, diminished scales, and may others. Scales are fundamental to music theory, and for guitarists, tend to be views as the pallete from which one can select notes to play. Playing notes over chords is a fundamental concept in music, and guitar in particular makes this tricky because there are so many ways to play the same note. In order to have all those choices immediately available, we practice scales. There are also non-musical scales that are used as technical exercises to build strength, dexterity, and speed. These are things like "spider drills", inside/outside picking drills, arpeggios, and so forth. Ultimately, these are all different forms of scales.

## String Slap

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-028 | technique | string-slap | String Slap |  |  |

String slap is when the string is released or struck in a way that causes it to hit the fretboard. This can be done by plucking the string, or even grabbing it, pulling it away from the fretboard, and releasing it. Strings can also be slapped with percussive technique, like using the thumb over the pickups to slap the string in such a way as to cause it to slap the fretboard. String slap creates a big transient that it pitched to whatever note or open string was being expressed, making it an amazing technique to bring percussion and melodic lines together.

## Practicing

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-029 | playing mode | practicing | Practicing | rehearsing |

Guitar practice is the act of playing the instrument in ways that build competence. This usually means drills that build speed, dexterity, control, and strings. Practicing builds mental pathways that store musical expressions. These can be recalled later, often without even conscious effort. Practicing can take many forms, from playing through songs, performing scales, and even working on things like looper techniques or physical positioning.

It is important to distinguish between a number of relatyed playing modes: practicing, performing, rehearsing, and workshopping.

Practicing is most directly related to and confusable with rehearsing. The difference is that a rehearsal is the performance of a setlist or set of artistic compositions in the style of the actual performance, whereas practicing does not resemble the performance, even when playing through a song. Practicing invariably includes many non-songplaying elements, like scales and other technical exercises designed to build capability, whearase rehearsing is design to acclimate the performer to a specific artistic expression experience.

## Rehearsing

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-030 | playing mode | rehearsing | Rehearsing |  |  |

When you rehearse a song or a performance, you are not only playing the performance as it would occur on stage, but frequently also practicing the non-musical elements of the performance. From a playing perspective, rehearsing is a form of practice, but practice is typically not rehearsing. A typical practice session includes lots of elements that don't occur during an actual performance, like warm-ups, scales, and noddling, to name a few. By contract, when reheasing one might not only perform the same songs as the upcoming performance, but also in the same order so that transitions and seques can be practiced.

## Workshopping

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-031 | playing mode | workshopping | Workshopping | |  |

When you workshop a song or phrase or passage, you are composing, arranging, and practicing all at the same time. You might have a core musical concepts - an interval, mood, a few chords of a progression, or part of a lead line, and you want to develop it into a meaningful composition. Workshopping is the art of playing through the concepts while changing, adding, removing, and generally experimenting with the concept until a more polished, complete passage has been created.

## Cycle Recording

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-032 | playing mode | cycle-recording | Cycle Recording  | Looping, loop recording |

Cycle, or loop recording, is when you configure your DAW to record in a loop for the purposes of caputuring multiple versions of the same passage as you play it. From the loop recordings, you would typically "comp" or compose a final track that is splied together from the best parts of each individual loop recording. A really short loop recording might be considered an overdub, as you are likely not comping the phrase, but just dropping in a short fix to the prior recording. A longer loop recording, like a verse or a chorus, typically has a bar of padding before and after the passage to give the guitarist a chance to play into and out of the passage in a normal-sounding way.

## DAW

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-033 | technology | DAW | DAW |  | 

DAW is short for `Digital Audio Workstation`. This is the recording and mixing software used to capture performances and edit the resulting music. Popular DAWs include Ableton, LogicPro, FLStudio, Reaper, etc.

## Overdub

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-044 | playing mode | overdub | Overdub |  |  |

An overdub is when you want to fix or change just a small section of playing in a recording. To do that, you arm the DAW to record over a short section and then play the corrected line. This recording then replaces the prior recording in the mix. Overdubs are usually short, attempting to fix a bad note, notes, or chord in an otherwise sufficient recording. Overdubs are kindof notorious for being hard to blend in to sound like the original session. Or perhaps better put, your success at good overdubs is probably limited by your gear. High end studio gear makes this a lot easier. However, anytime you go back to try to mimic an earlier performance, it's probably going to sound different unless it happens right at the same time. 

## Cowboy Chords

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-045 | theory | cowboy-chords | Cowboy Chords |  | 

`Cowboy Chords` are the `open string` or `first position` forms of the chords `A`, `C,`, `D`, `E`, and `G`. These chords also form the basis for the `CAGED` system.
It is believed the term comes from chords that are easy to play around the campfire, as Cowboys apparently do.

## Open Strings

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-046 | theory | open-strings | Open Strings | Muted strings |

An `Open String` is a string that is played without placing a finger on a fret. By open, it means the string is allowed to vibrate at it's fundamental frequency - E A D G B E on a guitar in standard tuning. In other contexts, it refers using at least one open string. For example, there are 'open string' chord formulations, especially for the CAGED chords. You can also opt to play the open strings whenever that note appears in the score (when possible, and it won't sometimes be physically possible). This would be called an `open string` run, even as not all the notes are actually open strings. But the fact that open strings are used consistently makes it an open string run. This is true in other contexts as well (chords, scales, etc.)

## First Position

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-047 | theory | first-position | First Position |  | 

The `First Position` in guitar typically refers to one of two things. 

1. Your hand position relative to the nut. I don't think it's supposed to be synonymous with fret number, but it could be construed that way.
2. Your hand position relative to the scale. When you map a scale out on the guitar neck, you find that it repeats, as a 24 fret guitar is basically two 12 fret segments side-by-sie. 12 frets is convenient becuase all the finger patterns repeat every 12 frets for all scales. In normal scales, there are 7 tones. This leads to 7 positions as the scale is viewed relative to the tones. In a pentatnoic scale there are five patterns that repeat. They are called positions, so there is a first through fifth position in pentatonic scales. Each position plays a pentatonic scale, but they all start on a different, successive note of the scale.

## CAGED System

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-048 | theory | caged-system | CAGED System | |  |

The `CAGED` system using the open string form of the chords C, A, G, E, and D to map the first 12 frets of the guitar into the major scale. The chord forms connect, providing access to many of the notes of the major scale linked across the 12 frets. CAGED is used to teach major scale soloing and provides easy reference points to many of the notes in the major scale through those chord shapes. CAGED is a conceptual tool rather than a precise one, and there are complaints that some of thd chord shapes are really extensions, and there should only be three chords in the form.

## Standard Tuning

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-049 | tuning | standard-tuning | Standard Tuning |    |

Standard tuning for a guitar is, from low string to high string, E, A, D, G, B, E. It's always been that way as far as I know. And yeah, the B string is a real fucking beeyotch to deal with. Standard tuning is also based on a 440 Hz A. Note that bands like Van Halen are technically not using standard tuning. In their case, it's called "E flat" tuning, and it means standard tuning pitched down by one semitone.

## Feedback

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-050 |  | feedback | Feedback | |  |

Feedback occurs when the amplified signal of the guitar is picked up by the guitar pickup, causing a positive feedback loop. This an engineering term of art. A positive feedback loop means that the signal feeding back causes constructive interference, increasing the amplitude of the signal as it is being amplified. This is categorized by squeals and howling sounds. In high gain / high distortion situations, feedback can begin to develop as notes and chords decay. It is used as a performative technique as well, by letting the feedback cycle establish into a stable tone, and then moving the strings, pickup selector, or making some other change that alters the feedback sound.

## String Slip

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-051 | noise | string slip | String Slip | tuning nut ping |

String slip occurs when the string becomes mechanically locked to either the nut or the bridge or the rollers on the bridge, and some kind of movement breaks the static friction. It typically sounds like a snap or ping sound, as the string suddently snaps into a new resting place. The grooves of the nut or the rollers of the bridge can be lubricated to reduce the incidence of string slip.

## Noise Floor

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-052 | noise | noise floor | Noise Floor |  |  |

The noise floor is a measurement made with no actual signal present to determine the ambient sound conditions for the recording. So, for example, plugging in a guitar but muting the strings with one hand. The sound coming out is only some low noise or buzzing, but no guitar signal. That is one measurement of the noise floor. If you disconnect the guitar and leave the input to the interface floating, you will get another noise floor - that of the recording device. The noise floor is what they are referring to when they say "signal to noise" ration, a term of art, meaning the average or maximum signal amplitude divided by the average or maximum noise amplitude.

The noise floor is also how a noise gate works. It simply suppressed the sound whenever the amplitude drops below the noise floor, as set by the noise gate's threshold.

## Capo

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-053 | technique | capo | Capo |  |  | |  |  |

A capo is a mechanical device that creates a barre across the fretboard, essentially changing the location of the nut an shortening the stings. A capo can be used to transpose a song to a different key by simply moving the capo to a new root note. While most capos bar the entire neck, there are capos that only barre part of the neck, and some that even allow for indiidual frets to be selected or not. A capo can also be used to change the shape of chords. For example, if a song is in A, but you put a capo on the fifth fret, you can now play it with the open E chord shape instead of the traditional open A chord shape.

## Nashville tuning

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-053 | tuning | nashville-tuning | Nashville Tuning |  | |  |  |

In Nashville tuning, the strings guages are changed to be the second, or alternate string in a 12 string guitar set. In such a set, there is a normal set of strings. But a 12 string has two strings per note. On the lower strings (E A D) the second string is an octive higher. For the other strings, it is in unison. THus, a Nashville guitar has an octive E, ocirve A, octive D, G, B, E. It sounds pretty strange when yo uhearr it. However, if you double track guitar, you can track the Nashville guitar and it will make the whole mix richer. If you mix it too aggressively, it might sounds like a 12 string, so it's best to choose a different way of playing that piece, and then it will really fucking POP.

## Intonation

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-054 | Physical | intonation | Intonation | |  |  |

The intonation of a guitar indicates how well it stays in tune when you play up the neck. The best test of intonation is to compare the pitch of the note on the 12th fret of the string with the 12th fret harmonic. If they are different, it means that the string length is not exactly half over the 12th fret. It is normal for a guitar to go a little out of tune as you play up the neck, but if the intonation is off, it will sound worse and worse as you play up the next. To fix it, you typically adjust the bridge saddles so that the 1/2 mark of the string is exactly over the 12th fret. You can do this by using a tuner to compare the pitch while ou adjust the sring lenth.

## Tone swell

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-055 | tecnique | tone-swell | Tone Swell |  |  |

Tone swell is a sound that emulates a wah-wah peddle. You do it by rolling the tone knob to the bass setting. Then you strike a note or chord, then roll the tone knob to treble and back. This creates that "wah" sounds. One some guitars, like the Telecaster, you can roll the knob with your pinky while you are playing, and some players develop very advanced techniques using this method.

## Diming

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-056 | technique | dimming | Diming |   |  |

Diming is an amplifier term. The knobs typically run from 1 to 10 (insert Spinal Tap joke here). When you "dime" am amp, you roll all the knobs to 10 and run it full out in all the ways.

## Rolling-off

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-057 | technique | rolling-off | Rolling Off |   |  |

Rolling-off typically refers to turning down the volume using the volume knob. It's called rolling off because of the technique. To "roll off" the volume, you typically use a finger or the side of the hand contacting the volume knob at a tangent and then using the friction to spin the knob as your finger or hand moves downwards. From a different perspective, it looks like the knob is rolling off your hand. When you are playing electric guitar in a band or around other people and you have to switch from talking to playing, and the plyaing is loud enough that you can't talk while playing, this motion of running your hand down the volume knob to quickly drop the volume to zero becomes fluid and instinctive.

## Cutaway

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-058 | physical | cutaway | Cutaway | | upper bout  |

The cutaway is a rounded section of the guitar body that is removed to make space for the players fretting hand. The cutaway is taken out of the lower bout, and allows access to frets higher than 12 or 14 (this varies depending on the guitar's geometry). With no cutaway, it is extremely difficult to access these frets and you typically cannot use your thumb or palm on the back of the neck to anchor the hand position.

## 60Hz hum

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-059 | noise | 60hz-hum | 60Hz Hum | 50 Hz hum, ground loop  |

60 Hz hum is a buzzing noise, low in frequency, obvs, that usually occurs when there are ground loops present in the guitar signal path. 60Hz is the frequency of the alternating current in North America. This noise is at 50 Hz in Europe, Asia, and other parts of the world. There can also be other low frequency noises that are picked up than just the line noise.

## Ground loop

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-060 | noise | ground-loop | Ground Loop |  |  |

A ground loop usually occurs when the guitar signal path includes daisy-chained pedals that have different grounding paths. One common source is using power cords that all run back to different source outlets. Take the example of a pedal chain with two pedals: distortion and reverb. If you plug both of those pedals into different power supplies, then you allow a current path that goes from one pedal, back through the power supply, to the other pedal. This loop acts an antenna, pickup up noise along the loop and then injecting that into the guitar signal. For simple rigs, ground loops can be pretty easy to eliminate. For complex rigs, having a good power supply is essential. There are devices called "galvanic isolators" that can filter out ground loops, but these should be used as a last resort and aren't generally necessary for guitar rigs.

## Electromagnetic (EM) interference

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-061 | noise | electromagnetic-interference | Electromagnetic Interference | |  |  | |  |  |

Electromagnetic inteference is when any kind of signal is injected into the guitar signal through some kind of coupling mechanism. It could be capacitive coupling in a power supply, phone broadcasts being picked up through poorly insulated pedal case, line noise coming in through a ground loop, or a million other causes. Because generating electricity created a magnetic field, and a magnetic field causes current to flow in metal, we are surrounded by EM noise.

## Shielded cable

| GEL-ID | Class | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|
| GEL-062 | noise | shielded-cable | Shielded Cable | |   |  |

A sheilded cable comprises one or more conductors carrying signals inside of a woven metal sheath. This sheath is called the shielding and it creates a faraday cage around the conductors. When the sheild itself is grounded, it shunts all the intercepted EM energy to ground, leaving a very clean signal. Sheilded cables are not perfect, though. Even small distortions in the sheilding can impair the sheilding effect. There is also typically a mimumum turning radius ont he cable, so you can't coil it tightly and expect the same EM rejection.

Coaxial cable is a special form of sheilded cable. Coaxial cable's gemoetry itself aids in EM rejection, as the magnetic fields from the conductors and the sheid cancel each other out elegantly. Seriously, it's one of the most rewarding proofs to learn in physics, when you get to the end of the formula and all the terms start cancleling out. Maths can be beautiful, sometimes.

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
