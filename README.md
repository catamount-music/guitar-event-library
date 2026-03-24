# Guitar Event Library (GEL)

**A versioned taxonomy and reference dictionary of discrete acoustic and electrical events occurring on the guitar.**

The **Guitar Event Library (GEL)** provides a structured, machine-readable "Source of Truth" for identifying guitar signal signatures ranging from intentional playing techniques to mechanical artifacts for use in machine learning classification (TensorFlow/YAMNet) and content provenance (C2PA).

---

## 🎯 Project Goals
* **Standardization:** Define a common language for guitar signal "events" (e.g., *Wound String Pluck* vs. *Fret Clank*).
* **Machine Learning:** Provide high-quality labels and definitions for training audio classifiers.
* **Provenance:** Establish a reference registry for embedding metadata into audio manifests via C2PA.

---

## 🛠 Project Structure (Beta)
This project is currently in an "Active R&D" phase. The structure will evolve from a flat dictionary into a formal schema.

* `/definitions.md` - The primary encyclopedia of guitar events.
* `/schema` - (Planned) JSON/YAML schema for data validation.
* `/samples` - (Planned) Reference .wav files recorded via BNC-direct output.

---

## 📜 Baseline Definitions (v0.1)
*Currently drafting initial entries for two-string (Low-E / B) reference rigs.*

1. **GEL-001: Wound String Pluck (Low E)** - High-amplitude initial transient with complex harmonic decay.
2. **GEL-002: Plain String Snap (B)** - High-frequency peak with rapid decay; minimal low-mid resonance.
3. **GEL-003: Mechanical Fret-Clank** - Non-musical transient caused by string-to-fret-wire collision.

---

## ⚖️ Licensing & Commercial Use

- **Non-commercial / research use:** Licensed under **CC BY-NC 4.0**.
- **Commercial use:** Not permitted under CC BY-NC 4.0. For commercial licensing, contact Catamount Music.

**Full license terms:** See `LICENSE.md`.

**Contact:** [Catamount Music](https://catamountmusic.com) or [Dave Owczarek](mailto://dave@catamountmusic.com) for commercial inquiries.
---

*Copyright © 2026 Catamount Music. All rights reserved.*
