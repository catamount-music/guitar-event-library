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

| GEL-ID | Class | Field | Display Label | Synonyms |
|---|---|---|---|---|
| GEL-001 | technique | bell-harmonic | Bell Harmonic | |

A bell harmonic is a bell-like sound make by creating standing waves in the guitar string. This is achieved by placing the tip of a finger (or other object, but finder is most common) at an even interval of the string length (half, third, quarter) and then plucking the string.
The finger is effectively creating a node where vibration is minimal, which suppresses the primary note vibration, leaving a harmonic series rooted in the bell harmonic.

Bell harmonics are typically played with a left-hand (pluck) / right-hand (finger over node) combination, but they can be played in a variety of ways, including

* picking hand only (index or other finger not used for holding the pick is positioned over the node.
* picking and fretting hand (fretting hand over the node, picking hand strikes string)
* fretting hand only (in the fretting hand, one finger is held over the node while another plucks the string. Yes, this is possible and pretty asesome, but uncommon.

## Pinch Harmonic

| GEL-ID | Class | Field | Display Label | Synonyms |
|---|---|---|---|---|
| GEL-002 | technique | pinch-harmonic | Pinch Harmonic | pick squeal |

Pinch harmonics are typically played with the picking hand only. Usually, the thumb is used to strike the string just after the note is plucked. This creates an extremly short standing wave that has a very high pitch.
While audible at normal volume, pinch harmonics are typically played with compression and distortion, which allows for the lower standing wave signal to be heard at loud volume, causing a distinct squeal kind of noise with a pitch.
