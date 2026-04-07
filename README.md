# Guitar Event Library (GEL)

**A versioned taxonomy and reference dictionary of discrete acoustic and electrical events occurring on the guitar.**

The **Guitar Event Library (GEL)** provides a structured, machine-readable "Source of Truth" for identifying guitar signal signatures ranging from intentional playing techniques to mechanical artifacts for use in machine learning classification (TensorFlow/YAMNet) and content provenance (C2PA).

---

## 🎯 Project Goals
* **Standardization:** Define a common language for guitar signal "events" (e.g., *Wound String Pluck* vs. *Fret Clank*).
* **Machine Learning:** Provide high-quality labels and definitions for training audio classifiers.
* **Discovery:** Can we answer the age-old question, "what is noodling?"

---

## 🛠 Project Structure (Beta)
This project is currently in an "Active R&D" phase. The structure will evolve from a flat dictionary into a formal schema.

**Current version:** `0.3.0` — tracked in `VERSION` and via [GitHub Releases](https://github.com/catamount-music/guitar-event-library/releases). This project follows [SemVer](https://semver.org/) with a pre-1.0 interpretation:
- **Patch** (`0.3.x`): new GEL entries added, no schema change.
- **Minor** (`0.x.0`): breaking schema change (fields added, renamed, or removed) — use this freely until 1.0.
- **1.0.0**: schema stabilized and ready for external consumers.

* `/definitions.md` - The primary encyclopedia of guitar events.
* `/schema` - (Planned) JSON/YAML schema for data validation.
* `/samples` - (Planned) Reference .wav files.

---

## 📜 Baseline Definitions
*Currently drafting initial entries for six-string electric guitar, direct-in, with standard tuning.*

1. **GEL-001: Bell Harmonic
2. **GEL-002: Pinch Harmonic

etc.

---

## Signal Processing Roles

GEL entries include both `Coverage` and `Signal Nature`.

- `Coverage = pipeline`: term is actively used by automated ML processing.
- `Coverage = dictionary-only`: term is defined in GEL but not currently part of automated processing.

For pipeline terms, `Signal Nature` separates acoustic detection targets from semantic interpretation and declared context.

- `yamnet-target`: Events intended for frame-level audio detection and timestamped aggregation.
- `semantic`: Higher-level playing modes inferred from longer sequences of events.
- `metadata`: Declared setup, context, or theory terms used for provenance and analysis.

Use this as the default pipeline:

1. Run event detection over short windows for `yamnet-target` events.
2. Post-process detections into timestamped events with confidence and duration.
3. Feed event sequences to semantic modeling for `semantic` labels.
4. Keep `metadata` as declared provenance/session context, not an audio inference target.

### Sample Collection Rule

Build the YAMNet data collection queue by filtering definitions where `Coverage = pipeline` and `Signal Nature = yamnet-target`.

Do not require YAMNet to classify labels marked `semantic` or `metadata`. Keep those as second-stage interpretation outputs or declared recording/session data.

Terms marked `Coverage = dictionary-only` remain in the dictionary but are excluded from automated model processing until promoted.

---

## ⚖️ Licensing & Commercial Use

- **Non-commercial / research use:** Licensed under **CC BY-NC 4.0**.
- **Commercial use:** Not permitted under CC BY-NC 4.0. For commercial licensing, contact Catamount Music.

**Full license terms:** See `LICENSE.md`.**

---
<p align="left">
  <img src="assets/name%2Blogo-black-transparent.png" alt="Catamount Music Logo" width="400">
</p>

**Contact:** [Catamount Music](https://catamountmusic.com) or [Dave Owczarek](mailto://dave@catamountmusic.com) for commercial inquiries.
---
*Copyright © 2026 Catamount Music. All rights reserved.*
