# Event Dictionary

## Proposed fields

**Note:** These don't all exist at the start, but may hopefully be filled in over time.

| Field | Definition | Purpose |
|---|---|---|
| GEL-ID | A unique serial number (e.g., GEL-005). | Permanent reference for code and experiments. |
| Class | The "bucket" (e.g., Physical, Electrical, Artifact, Environmental). | High-level taxonomy for filtering the dataset. |
| Coverage | Whether a term currently participates in automated ML processing. | Separates full dictionary scope from the active pipeline subset. |
| Signal Nature | Detection role in the pipeline: `yamnet-target`, `semantic`, or `metadata`. Applies when `Coverage = pipeline`. | Separates acoustically inferable events from interpretation and declared context. |
| Definition | A 1-2 sentence description of the physical or mechanical cause. | Human-readable dictionary entry. |
| Acoustic Signature | Description of the sound (timbre, duration, pitch). | Useful for manual labeling and ear-testing your rig. |
| Signal Data (BNC) | The "voltage view" (peak mV, waveform shape, noise floor). | Hard data for your oscilloscope and hardware testing. |
| Spectral Profile | Frequency range (e.g., 200 Hz - 5 kHz) and harmonic density. | The electrical characteristics of the signal. |
| Provenance Note | How this event relates to C2PA, authenticity, or consent. | Connects the sound to provenance. |

### Coverage Values

| Value | Meaning | Signal Nature |
|---|---|---|
| `pipeline` | Term is actively used by automated ML processing. | Required (`yamnet-target`, `semantic`, or `metadata`) |
| `dictionary-only` | Term is defined for dictionary completeness but not automated processing. | Leave blank |

### Signal Nature Values

| Value | Meaning | Example |
|---|---|---|
| `yamnet-target` | Directly inferable from audio windows and temporal aggregation. | `pick-slide`, `palm-mute`, `feedback` |
| `semantic` | Intent or behavior inferred from patterns over longer context windows. | `noodling`, `practicing`, `rehearsing` |
| `metadata` | Declared setup/context/theory values not directly recoverable from sound alone. | `pickup-selector`, `standard-tuning`, `DAW`, `CAGED system` |

`Class` and `Coverage` are orthogonal. `Signal Nature` is assigned only when `Coverage = pipeline`.

## Terms

### Bell Harmonic

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-001 | technique | pipeline | yamnet-target | bell-harmonic | Bell Harmonic |  | pinch-harmonic |
A bell harmonic is a bell-like sound made by creating standing waves in the guitar string. This is achieved by placing the tip of a finger, or another object, at an even interval of the string length (half, third, quarter) and then plucking the string.

The finger effectively creates a node where vibration is minimal, which suppresses the primary note vibration and leaves a harmonic series rooted in the bell harmonic.

Bell harmonics are typically played with a left-hand pluck and a right-hand finger over the node combination, but they can be played in a variety of ways, including:

* picking hand only (an index or other finger not used for holding the pick is positioned over the node)
* picking and fretting hand (fretting hand over the node, picking hand strikes string)
* fretting hand only (one finger is held over the node while another plucks the string; yes, this is possible and pretty awesome, but uncommon)

## Pinch Harmonic

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-002 | technique | pipeline | yamnet-target | pinch-harmonic | Pinch Harmonic | pick squeal | bell-harmonic |
Pinch harmonics are typically played with the picking hand only. Usually, the thumb is used to strike the string just after the note is plucked. This creates an extremely short standing wave that has a very high pitch.

While audible at normal volume, pinch harmonics are typically played with compression and distortion, which allows the lower-amplitude standing-wave signal to be heard at loud volume, causing a distinct squeal with a pitch.

## Afterlength

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-003 | physical | pipeline | yamnet-target | afterlength | Afterlength |  | bridge-length |
The `afterlength` is the section of the strings between the bridge and the tailpiece. It makes a plasticky, trebly sound when plucked or picked that has extremely low sustain due to the shortness of the string length. Striking the afterlength can still produce a quiet signal in an electric guitar, but it is often more audible than headstock overhang because it is closer to the bridge/pickup side of the instrument.

## Headstock Overhang

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-004 | physical | pipeline | yamnet-target | bridge-length | Headstock Overhang | headstock length | afterlength |
Headstock overhang (also called headstock length) is the exposed section of string between the nut and the tuning machines. This section can be plucked or struck to create a short, bright, plasticky sound with very low sustain. On most electric guitars, this signal is relatively quiet because the vibrating segment is on the nut/headstock side and not directly over the pickups.

There is no headstock overhang on a headless guitar, obvs, it being a guitar without a headstock.

## Pick Slide

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-005 | technique | pipeline | yamnet-target | pick-slide | Pick Slide | pick scrape |  |
A pick slide occurs when the edge of the pick, or plectrum, is run along the wound strings, creating a loud, harsh, grinding sound.

## Tap Harmonic

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-006 | technique | pipeline | yamnet-target | tap-harmonic | Tap Harmonic |  |  |
A tap harmonic creates a similar sound to the bell harmonic, but it is created through a different physical process. Instead of having one fingertip suppress string vibration on a node while the string is plucked, a tap harmonic happens as a result of the impact of the finger on the string. A tap harmonic occurs when the player taps the fret that lies at one of the strong harmonic nodes, such as the 12th, 7th, and 5th frets. If the tap is positioned right over the fret and is extremely quick, it activates the string and creates a standing wave with a node at the fret being tapped. The result is a bell harmonic that includes a transient, which is the tap of the finger on the string.

The location of the harmonic nodes can be changed by shortening the string length. If the player, for example, puts a barre on the first fret, all the harmonic-node locations will change. They may or may not line up exactly with frets, depending on the location of the barre.

## Barre

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-008 | technique | pipeline | semantic | barre | Barre |  |  |
A barre occurs when the fretting hand plays a chord shape with no open strings, so all strings vibrate. A simple barre occurs when one picks a fret and places a finger across all the strings on that fret.

The F barre chord is notorious for being the most difficult chord for beginners. String tension is higher near the headstock, and it takes a lot more force to press down cleanly enough to articulate a note on every string in this position.

## Barre Chords

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-009 | technique | pipeline | semantic | barre-chords | Barre Chords |  |  |
A barre chord is a chord that includes a barre, or a finger placed vertically across the guitar neck, articulating a note on every string. The open chord "E" shape is the most commonly used and named barre chord. It is played with just three fingers in the open position, but the addition of the first-finger barre allows the chord to be moved up and down the neck in any position, changing only the root note of the chord.

## Chukka

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-010 | technique | pipeline | yamnet-target | chukka | Chukka | chuc, chuk, chuhk, chuck | chug |
A chukka is played by muting the strings so they do not ring out in any way, then strumming the strings rapidly enough that you do not hear individual string strikes. This creates a "chukk" sound. If the "chukk" is the downstroke, the "a" is the upstroke. When it is played the same way, the down-up pair is called a chukka.

It is related to a chug in that it is a percussive technique. When played in syncopation with extremely staccato pressure on the frets to create a brief chord, complex rhythms can evolve.

## Chug

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-034 | technique | pipeline | yamnet-target | chug | Chug |  | chukka, djent |
A chug occurs when you strike the strings with them simultaneously palm-muted. While in some cases the muting can be done in other ways, such as muting at the headstock or nut for open-string runs, it is most commonly done with palm muting on the bottom three strings: low E, A, and D in standard tuning.

Chugging is a rhythmic expression that uses patterns of the basic chug to create structure. In metal, this is best exemplified by the `djent` style.

## 3NPS ("Three Notes Per String")

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-011 | technique | pipeline | semantic | 3nps | 3NPS |  | scales |
A 3NPS scale is one where there are always three notes on each string. They can be tricky, especially on the lower frets, because they frequently require a 5-fret span, which is a relatively longer distance when located near the headstock.

There are healthy debates about whether 3NPS scales are better than other approaches. Ultimately, the scale patterns are the same; it is just how they are played that varies, and most guitarists would do well to practice all variations because they have different utility in different situations. 3NPS scales are great for legato, hammer-ons, pull-offs, and speed because they have a unifying cadence across all strings. The only thing that really sucks about them is that alternate picking with 3NPS requires you to learn some patterns for moving from string to string.

## Inside Picking

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-012 | technique | pipeline | semantic | inside-picking | Inside Picking |  | outside-picking, economy-picking, alternate-picking |
Inside picking occurs when a series of notes falls on two adjacent strings and the passage is played by attacking each string from inside the gap between them. The pick always starts from "inside" the strings.

## Outside Picking

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-013 | technique | pipeline | semantic | outside-picking | Outside Picking |  | inside-picking, economy-picking, alternate-picking |
Outside picking occurs when a series of notes falls on two adjacent strings and the passage is played by attacking each string from outside the gap between them. The pick always starts from "outside" the strings.

## Economy Picking

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-014 | technique | pipeline | semantic | economy-picking | Economy Picking |  | inside-picking, outside-picking, alternate-picking |
Economy picking is using the most efficient technique to play a phrase of notes. The classic example is alternate picking with an added sweep-pick motion for any string change that occurs in the same direction as the pick motion. The notion of economy comes from minimizing the number of times the guitarist has to perform an awkward note-to-note transition, such as downstrokes on two different strings at high speed.

## Alternate Picking

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-035 | technique | pipeline | semantic | alternate-picking | Alternate Picking |  | inside-picking, outside-picking, economy-picking |
Alternate picking is a technique where the pick always alternates between downstroke and upstroke, no matter where the notes need to be played on the neck. This creates challenging situations, particularly around string switching, where it is sometimes natural and faster to break the alternation. A purist, though, would require strict alternation on every note.

## Galloping

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-015 | technique | pipeline | yamnet-target | gallop | Galloping |  |  |
Credit Ben Eller on this one; I did not realize it was a named thing. Galloping is a rhythmic technique that combines playing chugs in doublets, triplets, or other arrangements to create a rhythmic sound that mimics galloping.

## Dive Bomb

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-016 | technique | pipeline | yamnet-target | dive-bomb | Dive Bomb |  | tremolo-bar |
A dive bomb is when you play a string, often an open middle string like the G, and then press the tremolo bar sharply toward the guitar, causing the strings to loosen and the pitch of that played string to drop into the bass range. With a locking tremolo, the strings can be made so loose that they do not vibrate and sometimes get stuck to the pickups due to magnetic attraction. The sound mimics the tropey old-school falling-bomb sound: trebly at first, then dropping in pitch as it descends. The loosening strings hitting the pickups can sound like the explosion as well.

## Bigsby Tremolo

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-017 | physical | pipeline | metadata | bigsby-tremolo | Bigsby Tremolo |  | tremolo-bar |
A Bigsby tremolo is a bar that uses a moving roller to raise and lower string tension, creating the tremolo effect. A Bigsby tremolo bar has a much narrower range than a spring-loaded tremolo and is used for shallower tremolo effects. Like most tremolo systems, a Bigsby tremolo affects tuning stability and can create pings and knocks from the strings moving around on the tremolo bar. A Bigsby tremolo bar cannot be used in a highly aggressive manner and is not appropriate for most hard rock and metal, where a much greater tremolo range is needed.

## Legato

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-018 | technique | pipeline | yamnet-target | legato | Legato |  |  |
Legato has a specific meaning as a guitar technique. While it canonically means playing smoothly articulated lead lines that are connected and fluid, in the guitar world it also means doing that with only the fretting hand. Legato is a left-hand technique for right-handed players, or a right-hand technique for left-handed players. With legato, you use hammer-ons and pull-offs to create all the notes, and the pull-offs are done from one finger to the next on the fretting hand. Legato requires building hand-muscle strength, especially for first-finger hammer-ons and pinky pull-offs.

## Hammer On

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-019 | technique | pipeline | yamnet-target | hammer-on | Hammer On |  | legato |
A hammer-on is when you play the note by striking and holding the string against the fretboard without using a pick, using only the fingertip. It can be played with either hand. To make hammer-ons effective, they must be played close to the fret with a sharp striking motion. Compression is often used in the signal chain to help smooth out the sound and raise the levels of the quieter notes.

## Pull Off

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-020 | technique | pipeline | yamnet-target | pull-off | Pull Off |  | legato |
A pull-off is when a note is played by pulling up or down on the string with a finger, usually on the fretting hand, and then releasing it. The note is thus played without a pick. Pull-offs can also be done with the picking hand. In that case, a finger on the picking hand will usually hammer on the note and then pull off to the next note.

## Chicken Picking

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-021 | technique | pipeline | semantic | chicken-picking | Chicken Picking |  |  |
The chicken-picking technique is named after the sound of one of its principal movements. Chicken picking alternates staccato notes that are picked and plucked with the fingers. The canonical chicken-picking sound mimics clucking, or the "bawk-bawk" sound of a chicken, when the pick strikes a note on a string that is immediately palm-muted, followed by the picking-hand fingers pulling sharply on another string, almost slapping it back onto the neck, to create the second note, which is then also immediately palm-muted. While there are many more complicated patterns, this kind of syncopated alternation between a strongly picked note and notes plucked with the fingers creates a distinct sound that is a staple, particularly in country music and bluegrass.

## Palm Mute

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-022 | technique | pipeline | yamnet-target | palm-mute | Palm Mute |  |  |
A palm mute is when you press the palm of your hand over the strings right where they meet the rollers, tailstop, or bridge. Palm muting allows for a rich transient attack with a very short decay to quiet, which is perfect for creating rhythmic sequences and gallops. The level of muting can be adjusted by how close the palm is to the strings at the bridge. In addition, the palm mute is typically applied from low to high strings as a general-purpose mute during playing. For example, a passage that starts with power chords on the first few frets of the neck and eventually turns into a lead line on the higher strings might begin with the palm muting the bottom three strings and then move up, covering more strings as the score moves to a higher-pitched passage.

## False Start

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-023 | technique | pipeline | semantic | false-start | False Start |  |  |
A false start happens when beginning a song or starting a passage. Although making a mistake is not required, it is typically the reason the false-start behavior develops. In a false start, the player realizes immediately that they do not wish to continue playing and simply stops the passage, rests briefly, then starts again. I suppose it is not technically required to play the passage again for it to be a false start. One could simply give up after the attempt and it might be called just a failed attempt at a song. But a false start is usually immediately followed by another attempt.

False starts in an ensemble setting are trickier. Often, one does not have the luxury of stopping, and having broken from the stream of musical consciousness due to the mistake, you have to slam your way back into the song at the right moment while simultaneously attempting to regain your composure.

## E Flat Tuning

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-024 | tuning | pipeline | metadata | e-flat-tuning | E Flat Tuning |  |  |
Made popular by Eddie Van Halen (EVH), E-flat tuning involves tuning the guitar to E flat instead of E. The story goes that EVH thought it sounded nastier and more evil, so he tuned his guitar down a half step. The annoying thing about E-flat tuning is that most tuners default to sharps, not flats, so instead of tuning to Eb, Ab, Db, Gb, Bb, and Eb, you are actually tuning to D#, G#, C#, F#, A#, and D#. But you are a pro, so you can handle that.

## String Bend

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-025 | technique | pipeline | yamnet-target | string-bend | String Bend | boomer bend, fretting out |  |
As the name suggests, string bending is when you raise or lower the pitch of the string you are playing by bending it away from its resting place, either up or down across the fretboard of the guitar. Typically, you bend up on the high strings and down on the low strings, or, put another way, you bend in the direction where there is more fretboard to bend into. Bending up versus down sounds different. There are also reverse bends, where you mute the string, bend it, then strike it at the higher pitch and release the bend, causing it to bend down.

Modern bends are often achieved by ultrafast fret slides, which is a more contemporary sound. Old-school bends are called "boomer bends" and usually involve bending the note at least two semitones and finishing it with a wide vibrato. This is easiest to do on a shorter-scale guitar, like a Gibson Les Paul.

## Noodling

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-026 | playing mode | pipeline | semantic | noodling | Noodling |  | improvisation |
Noodling is one of the hardest terms to define because when someone is noodling, it can sound just like improvisation or workshopping. The general idea is that noodling is undirected, casual playing of the instrument that lacks structure and context, although it may drift in and out of different musical styles. For guitarists, playing meaningless notes in the pentatonic scale is one canonical form of noodling. The guitarist does not even have to respect the number of bars in the form; they can just pick away, play the blues box, stop and start, and generally meander around. This is noodling.

## Scales

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-027 | technique | pipeline | semantic | scales | Scales |  |  |
A scale is a sequence of notes, typically from a root note across one or two octaves, following a common pattern. The major scale pattern defines not only the major scale, but all the modes in Western music. Each of those modes becomes a scale. Likewise, there are pentatonic scales, diminished scales, and many others. Scales are fundamental to music theory, and for guitarists they tend to be viewed as the palette from which one can select notes to play. Playing notes over chords is a fundamental concept in music, and guitar in particular makes this tricky because there are so many ways to play the same note. In order to have all those choices immediately available, we practice scales. There are also non-musical scales that are used as technical exercises to build strength, dexterity, and speed. These are things like spider drills, inside and outside picking drills, arpeggios, and so forth. Ultimately, these are all different forms of scales.

## String Slap

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-028 | technique | pipeline | yamnet-target | string-slap | String Slap |  |  |
String slap is when the string is released or struck in a way that causes it to hit the fretboard. This can be done by plucking the string, or even grabbing it, pulling it away from the fretboard, and releasing it. Strings can also be slapped with a percussive technique, such as using the thumb over the pickups to slap the string in such a way that it hits the fretboard. String slap creates a big transient that is pitched to whatever note or open string was being expressed, making it an amazing technique for bringing percussion and melodic lines together.

## Practicing

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-029 | playing mode | pipeline | semantic | practicing | Practicing | rehearsing |  |
Guitar practice is the act of playing the instrument in ways that build competence. This usually means drills that build speed, dexterity, control, and strength. Practicing builds mental pathways that store musical expressions. These can be recalled later, often without even conscious effort. Practicing can take many forms, from playing through songs to performing scales to working on things like looper techniques or physical positioning.

It is important to distinguish between a number of related playing modes: practicing, performing, rehearsing, and workshopping.

Practicing is most directly related to, and often confused with, rehearsing. The difference is that a rehearsal is the performance of a setlist or set of artistic compositions in the style of the actual performance, whereas practicing does not resemble the performance, even when playing through a song. Practicing invariably includes many non-song-playing elements, like scales and other technical exercises designed to build capability, whereas rehearsing is designed to acclimate the performer to a specific artistic-expression experience.

## Rehearsing

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-030 | playing mode | pipeline | semantic | rehearsing | Rehearsing |  |  |
When you rehearse a song or a performance, you are not only playing the performance as it would occur on stage, but frequently also practicing the non-musical elements of the performance. From a playing perspective, rehearsing is a form of practice, but practice is typically not rehearsing. A typical practice session includes lots of elements that do not occur during an actual performance, like warm-ups, scales, and noodling, to name a few. By contrast, when rehearsing one might not only perform the same songs as the upcoming performance, but also perform them in the same order so that transitions and segues can be practiced.

## Workshopping

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-031 | playing mode | pipeline | semantic | workshopping | Workshopping |  |  |
When you workshop a song, phrase, or passage, you are composing, arranging, and practicing all at the same time. You might have a core musical concept, such as an interval, a mood, a few chords of a progression, or part of a lead line, and you want to develop it into a meaningful composition. Workshopping is the art of playing through the concepts while changing, adding, removing, and generally experimenting with them until a more polished, complete passage has been created.

## Cycle Recording

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-032 | playing mode | pipeline | semantic | cycle-recording | Cycle Recording | looping, loop recording |  |
Cycle, or loop, recording is when you configure your DAW to record in a loop for the purpose of capturing multiple versions of the same passage as you play it. From the loop recordings, you would typically comp a final track that is spliced together from the best parts of each individual take. A really short loop recording might be considered an overdub, because you are likely not comping the phrase but just dropping in a short fix to the prior recording. A longer loop recording, like a verse or chorus, typically has a bar of padding before and after the passage to give the guitarist a chance to play into and out of the passage in a natural-sounding way.

## DAW

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-033 | technology | pipeline | metadata | DAW | DAW |  |  |
DAW is short for `Digital Audio Workstation`. This is the recording and mixing software used to capture performances and edit the resulting music. Popular DAWs include Ableton, Logic Pro, FL Studio, Reaper, and others.

## Overdub

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-044 | playing mode | pipeline | semantic | overdub | Overdub |  |  |
An overdub is when you want to fix or change just a small section of playing in a recording. To do that, you arm the DAW to record over a short section and then play the corrected line. This recording then replaces the prior recording in the mix. Overdubs are usually short, attempting to fix a bad note, notes, or chord in an otherwise sufficient recording. Overdubs are kind of notorious for being hard to blend in so they sound like the original session. Or perhaps better put, your success at making good overdubs is probably limited by your gear. High-end studio gear makes this a lot easier. However, any time you go back to try to mimic an earlier performance, it is probably going to sound different unless it happens right away.

## Cowboy Chords

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-045 | theory | pipeline | metadata | cowboy-chords | Cowboy Chords |  |  |
`Cowboy chords` are the `open-string` or `first-position` forms of the chords `A`, `C`, `D`, `E`, and `G`. These chords also form the basis for the `CAGED` system.

It is believed that the term comes from chords that are easy to play around the campfire, as cowboys apparently do.

## Open Strings

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-046 | theory | pipeline | yamnet-target | open-strings | Open Strings |  | muted strings |
An `open string` is a string that is played without placing a finger on a fret. By open, it means the string is allowed to vibrate at its fundamental frequency: E A D G B E on a guitar in standard tuning. In other contexts, it refers to using at least one open string. For example, there are open-string chord formulations, especially for the CAGED chords. You can also opt to play the open strings whenever that note appears in the score, when possible, though it will not always be physically possible. This would be called an `open-string` run, even though not all the notes are actually open strings. The fact that open strings are used consistently makes it an open-string run. This is true in other contexts as well, including chords and scales.

## First Position

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-047 | theory | pipeline | metadata | first-position | First Position |  |  |
The `first position` in guitar typically refers to one of two things.

1. Your hand position relative to the nut. I do not think it is supposed to be synonymous with fret number, but it could be construed that way.
2. Your hand position relative to the scale. When you map a scale out on the guitar neck, you find that it repeats, because a 24-fret guitar is basically two 12-fret segments side by side. Twelve frets is convenient because all the finger patterns repeat every 12 frets for all scales. In normal scales, there are 7 tones. This leads to 7 positions as the scale is viewed relative to those tones. In a pentatonic scale there are five patterns that repeat. They are called positions, so there is a first through fifth position in pentatonic scales. Each position plays a pentatonic scale, but each starts on a different successive note of the scale.

## CAGED System

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-048 | theory | pipeline | metadata | caged-system | CAGED System |  |  |
The `CAGED` system uses the open-string forms of the chords C, A, G, E, and D to map the first 12 frets of the guitar into the major scale. The chord forms connect, providing access to many of the notes of the major scale across the 12 frets. CAGED is used to teach major-scale soloing and provides easy reference points to many of the notes in the major scale through those chord shapes. CAGED is a conceptual tool rather than a precise one, and there are complaints that some of the chord shapes are really extensions and that there should only be three chords in the form.

## Standard Tuning

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-049 | tuning | pipeline | metadata | standard-tuning | Standard Tuning |  |  |
Standard tuning for a guitar is, from low string to high string, E, A, D, G, B, E. It has always been that way as far as I know. And yes, the B string is a real fucking beeyotch to deal with. Standard tuning is also based on a 440 Hz A. Note that bands like Van Halen are technically not using standard tuning. In their case, it is called E-flat tuning, and it means standard tuning pitched down by one semitone.

## Feedback

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-050 | noise | pipeline | yamnet-target | feedback | Feedback |  |  |
Feedback occurs when the amplified signal of the guitar is picked up again by the guitar pickup, causing a positive feedback loop. This is an engineering term of art. A positive feedback loop means that the signal feeding back causes constructive interference, increasing the amplitude of the signal as it is being amplified. This is characterized by squeals and howling sounds. In high-gain or high-distortion situations, feedback can begin to develop as notes and chords decay. It is also used as a performative technique by letting the feedback cycle settle into a stable tone and then moving the strings, changing the pickup selector, or making some other change that alters the feedback sound.

## String Slip

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-051 | noise | pipeline | yamnet-target | string-slip | String Slip | tuning nut ping |  |
String slip occurs when the string becomes mechanically locked to either the nut, the bridge, or the rollers on the bridge, and some kind of movement breaks the static friction. It typically sounds like a snap or ping, as the string suddenly snaps into a new resting place. The grooves of the nut or the rollers of the bridge can be lubricated to reduce the incidence of string slip.

## Noise Floor

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-052 | noise | pipeline | yamnet-target | noise-floor | Noise Floor |  |  |
The noise floor is a measurement made with no actual signal present in order to determine the ambient sound conditions for the recording. So, for example, if you plug in a guitar but mute the strings with one hand, the sound coming out is only low noise or buzzing with no guitar signal. That is one measurement of the noise floor. If you disconnect the guitar and leave the input to the interface floating, you will get another noise floor: that of the recording device. The noise floor is what people are referring to when they say signal-to-noise ratio, a term of art meaning the average or maximum signal amplitude divided by the average or maximum noise amplitude.

The noise floor is also how a noise gate works. It simply suppresses the sound whenever the amplitude drops below the noise floor, as set by the noise gate's threshold.

## Capo

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-053 | physical | pipeline | metadata | capo | Capo |  |  |
A capo is a mechanical device that creates a barre across the fretboard, essentially changing the location of the nut and shortening the strings. A capo can be used to transpose a song to a different key by simply moving the capo to a new root note. While most capos barre the entire neck, there are capos that only barre part of the neck, and some even allow individual frets to be selected or skipped. A capo can also be used to change the shape of chords. For example, if a song is in A, but you put a capo on the fifth fret, you can now play it with the open E chord shape instead of the traditional open A chord shape.

## Nashville Tuning

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-036 | tuning | pipeline | metadata | nashville-tuning | Nashville Tuning |  |  |
In Nashville tuning, the string gauges are changed to match the second, or alternate, string in a 12-string guitar set. In such a set, there is a normal set of strings, but a 12-string has two strings per note. On the lower strings, E, A, and D, the second string is an octave higher. For the other strings, it is in unison. Thus, a Nashville-tuned guitar has octave E, octave A, octave D, G, B, and E. It sounds pretty strange when you hear it by itself. However, if you double-track guitar, you can track the Nashville guitar too, and it will make the whole mix richer. If you mix it too aggressively, it might sound like a 12-string, so it is best to choose a different way of playing that part, and then it will really fucking pop.

## Intonation

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-054 | physical | pipeline | metadata | intonation | Intonation |  |  |
The intonation of a guitar indicates how well it stays in tune when you play up the neck. The best test of intonation is to compare the pitch of the note on the 12th fret of the string with the 12th-fret harmonic. If they are different, it means that the string length is not exactly halved over the 12th fret. It is normal for a guitar to go a little out of tune as you play up the neck, but if the intonation is off, it will sound worse and worse as you play farther up the neck. To fix it, you typically adjust the bridge saddles so that the halfway point of the string is exactly over the 12th fret. You can do this by using a tuner to compare the pitch while you adjust the string length.

## Tone Swell

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-055 | technique | pipeline | yamnet-target | tone-swell | Tone Swell |  |  |
Tone swell is a sound that emulates a wah-wah pedal. You do it by rolling the tone knob to the bass setting. Then you strike a note or chord, then roll the tone knob to treble and back. This creates that "wah" sound. On some guitars, like the Telecaster, you can roll the knob with your pinky while you are playing, and some players develop very advanced techniques using this method.

## Diming

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-056 | technique | dictionary-only |  | diming | Diming |  |  |
Diming is an amplifier term. The knobs typically run from 1 to 10, insert Spinal Tap joke here. When you "dime" an amp, you roll all the knobs to 10 and run it flat out in every way.

## Rolling Off

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-057 | technique | pipeline | yamnet-target | rolling-off | Rolling Off |  |  |
Rolling off typically refers to turning down the volume with the volume knob. It is called rolling off because of the technique. To roll off the volume, you typically use a finger or the side of the hand, contacting the volume knob tangentially and then using friction to spin the knob as your finger or hand moves downward. From a different perspective, it looks like the knob is rolling off your hand. When you are playing electric guitar in a band or around other people and you have to switch from talking to playing, and the playing is loud enough that you cannot talk while playing, this motion of running your hand down the volume knob to quickly drop the volume to zero becomes fluid and instinctive.

## Cutaway

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-058 | physical | pipeline | metadata | cutaway | Cutaway |  | upper bout |
The cutaway is a rounded section of the guitar body that is removed to make space for the player's fretting hand. The cutaway is taken out of the lower bout and allows access to frets higher than 12 or 14, depending on the guitar's geometry. With no cutaway, it is extremely difficult to access these frets, and you typically cannot use your thumb or palm on the back of the neck to anchor hand position.

## 60Hz Hum

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-059 | noise | pipeline | yamnet-target | 60hz-hum | 60Hz Hum | 50 Hz hum, ground loop |  |
60 Hz hum is a buzzing noise, low in frequency, obviously, that usually occurs when there are ground loops present in the guitar signal path. Sixty hertz is the frequency of alternating current in North America. This noise is at 50 Hz in Europe, Asia, and other parts of the world. There can also be other low-frequency noises picked up besides the line noise.

## Ground Loop

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-060 | noise | pipeline | yamnet-target | ground-loop | Ground Loop |  |  |
A ground loop usually occurs when the guitar signal path includes daisy-chained pedals that have different grounding paths. One common source is using power cords that run back to different source outlets. Take the example of a pedal chain with two pedals: distortion and reverb. If you plug both of those pedals into different power supplies, then you allow a current path that goes from one pedal back through the power supply to the other pedal. This loop acts as an antenna, picking up noise along the loop and then injecting that into the guitar signal. For simple rigs, ground loops can be pretty easy to eliminate. For complex rigs, having a good power supply is essential. There are devices called galvanic isolators that can filter out ground loops, but these should be used as a last resort and are not generally necessary for guitar rigs.

## Electromagnetic (EM) Interference

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-061 | noise | pipeline | yamnet-target | electromagnetic-interference | Electromagnetic Interference |  |  |
Electromagnetic interference is when any kind of signal is injected into the guitar signal through some kind of coupling mechanism. It could be capacitive coupling in a power supply, phone broadcasts being picked up through a poorly insulated pedal case, line noise coming in through a ground loop, or a million other causes. Because generating electricity creates a magnetic field, and a magnetic field causes current to flow in metal, we are surrounded by EM noise.

## Shielded Cable

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-062 | noise | pipeline | metadata | shielded-cable | Shielded Cable |  |  |
A shielded cable comprises one or more conductors carrying signals inside a woven metal sheath. This sheath is called the shielding, and it creates a Faraday cage around the conductors. When the shield itself is grounded, it shunts all the intercepted EM energy to ground, leaving a very clean signal. Shielded cables are not perfect, though. Even small distortions in the shielding can impair the shielding effect. There is also typically a minimum turning radius on the cable, so you cannot coil it tightly and expect the same EM rejection.

Coaxial cable is a special form of shielded cable. Coaxial cable's geometry itself aids in EM rejection, as the magnetic fields from the conductors and the shield cancel each other out elegantly. Seriously, it is one of the most rewarding proofs to learn in physics, when you get to the end of the formula and all the terms start canceling out. Math can be beautiful sometimes.

## Fingerstyle

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-063 | technique | pipeline | semantic | fingerstyle | Fingerstyle |  |  |
Fingerstyle is a technique used to play guitar which, unsurprisingly, features the fingers and not a pick. Fingerstyle guitarists replace the pick with one of three things:

- a fingertip
- finger picks that slide onto each fingertip
- a fingernail

Similar to classical guitarists, serious fingerstyle guitarists grow and treat their nails, or have artificial nails applied, in order to get a clean picked sound and precision that a finger pad cannot match.

There are different kinds of fingerstyle guitar playing. Travis picking is probably one of the most famous and is a staple in country, bluegrass, and Western music.

## Travis Picking

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-064 | technique | pipeline | semantic | travis-picking | Travis Picking |  |  |
Named after Travis, which I need to research more fully, Travis picking is a specific alternation played either fingerstyle or with a pick hitting the bass note while the fingers hit the other notes in a chicken-picking style.

Travis picking uses the thumb to create a bass line that alternates on the lower strings in between arpeggios or chords.

We should probably show some music or tablature to explain this better.

## Plectrum

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-065 | physical | pipeline | metadata | plectrum | Plectrum |  | pick |
A `plectrum` is simply the official term-of-art name for the thing that almost everyone else in the world calls a `pick`.

## Flatpicking

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-066 | technique | pipeline | semantic | flatpicking | Flatpicking |  |  |
Flatpicking is when you play the guitar using a pick only, with no fingers. Common in country and bluegrass, flatpicking usually involves precise alternate picking and is best exemplified by runs on the acoustic guitar. The best-known example is probably the famous G run, which I should include.

The challenge with flatpicking is that strict alternate picking creates difficult string-switching choices, and these are complicated further by the more challenging aspects of playing an acoustic guitar cleanly at speed. When executed crisply, though, it sounds amazeballs.

## Vibrato

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-037 | technique | pipeline | yamnet-target | vibrato | Vibrato |  |  |
Adding vibrato to a note is one of the most essential forms of expression, and one that is typically unique to the player. Vibrato is when you alter the pitch of the note that is ringing out by either bending the string up and down, moving it from side to side quickly, or using the tremolo bar to raise and lower the string tension. Vibrato mimics the sound a human voice makes when pitch variation is added to the end of a sung, sustained note.

The wild thing about vibrato is that it tends to sound better when you bend up into it. The reason is that the pitch variations should happen from a baseline of the primary frequency of the note. But when you finger a note on guitar, you cannot lower the pitch, only raise it through bending. Thus, the vibrato created centers around a note that is actually sharper than the one played so that the vibrato can be above and below it. When you bend up to a note and then add vibrato, you can center the vibrato pitch on the note you want to play. Since you are bending up into it, as you vary the bend to create vibrato, you are able to lower the pitch below the note you are trying to sustain.

I think I need some 8x10 photos with circles and arrows on the back to explain this fully.

## Body Percussion

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-067 | technique | pipeline | yamnet-target | body-percussion | Body Percussion |  |  |
Body percussion is self-explanatory as long as you realize we are talking about the guitar body. When you tap the body of the guitar, you are able to make sounds that are picked up by the pickup even though you are not engaging in the typical direct excitation of metal strings in a magnetic field kind of playing. There are a few reasons why hitting the guitar makes noise. We are talking about electric guitar at the moment. The biggest reason is because it causes the body of the guitar to vibrate, which does cause the strings to move and create noise. It can also cause the pickups to move, knobs and strings to reposition, and other artifacts that are in fact transmitted through the pickups.

On an acoustic guitar you get the added benefit of the reverb and sound transmitted through the body of the guitar, and the bracing, and this can be used as percussion during the performance.

Some guitar pickups also have microphonic properties and may pick up some of the impact noise created during a body strike.

## Rake

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-068 | technique | pipeline | yamnet-target | rake | Rake |  |  |
Raking the strings means strumming them slowly enough to hear every string articulated, but not so slowly that they sound individually played. Basically, on the spectrum of strumming, full strums are fast enough that you cannot hear the individual strings being played and they all ring out close enough together to be one sound. If you slow that down, you get to the point where you can hear the individual strings. That is a rake. A rake is similar to a sweep, although a sweep generally means playing up or down the strings in consecutive or reverse-consecutive order. A rake usually means playing all the strings of a chord rather than a lead line or arpeggio.

## Pickup Selector

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-069 | physical | pipeline | metadata | pickup-selector | Pickup Selector |  |  |
The pickup selector is a switch located typically on the front face of the guitar, either below the strings on or near the pickguard, or above the strings, usually on the upper bout.

The pickup selector switches between the active pickups, assuming there is more than one. Often, a pickup selector also includes pickup blending. That is, there might be five positions: 1, 3, and 5 correspond to pickups physically in the guitar, whereas 2 is a mix of 1 and 3, and 4 is a mix of 3 and 5. Sometimes there are other tricks built into the pickup selector, like splitting a humbucker into a single coil, or blending together two pickups in a different variation than the one described above. They vary wildly by guitar style.

## String Stretching

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL-070 | technique | pipeline | yamnet-target | string-stretching | String Stretching |  |  |
You typically stretch the strings after changing them, or if you have a string go out of tune and it is challenging to keep in tune. String stretching helps settle the windings on the peg, assuming you do not have a locking tremolo. Locking tremolo systems and locking tuners generally obviate the need to stretch strings. The worst string stretcher is a Fender Strat with a spring-loaded tremolo system. Good luck keeping that sucker in tune.

After you change the strings, they will loosen and tighten until the windings on the tuning peg are regular and there are no loose or extra-tight windings. Usually, after changing strings, the strings are stretched either by attempting a large bend on the 12th fret, causing the most deflection and stretching the string around the tuning pegs, or by pulling them away from the body of the guitar as if to snap them.

This is typically done multiple times because the guitar is a tempered instrument, so every time you mess with one string, the others react. By repeating the string stretching, those reactions get smaller and smaller until they fall within the normal deviations of tuning tolerance.

String stretching helps avoid the situation where you change the strings, start to play, and they immediately go out of tune and sound horrible.

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

Description

## 

| GEL-ID | Class | Coverage | Signal Nature | Field | Display Label | Synonyms | Related Terms |
|---|---|---|---|---|---|---|---|
| GEL- |  |  |  |  |  |  |  |

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