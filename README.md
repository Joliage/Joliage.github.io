# Naomie Bambara — Portfolio (GitHub Pages)

Personal portfolio site showcasing academic research and applied projects in Machine Learning, Natural Language Processing, and Speech Processing.

---

## 👤 About Me

Hi — I’m **Naomie Bambara**, an MSc Computer Science candidate at St. Cloud State University (expected May 2026).  
I build reproducible ML systems and applied research prototypes that bridge linguistics and engineering — for example, a syllable-based Text-to-Speech prototype for the Mooré language.

---

## 📂 What You’ll Find Here

- 🔊 **Text-to-Speech (TTS)** — A tonal, syllable-concatenation TTS system for the Mooré language (hand-segmented syllable database, ARPABET-style lexicon, Python synthesizer, MFCC-based evaluation).  
- 🤖 **Machine learning & data science** — End-to-end projects: predictive modeling, hyperparameter tuning, model evaluation (Scikit-Learn / TensorFlow / Keras).  
- 💻 **Software & tooling** — Scripts and utilities for audio preprocessing, lexicon generation, Praat TextGrid export, and evaluation (pydub, librosa, parselmouth).  
- 📂 **Artifacts** — Code, sample audio, evaluation CSVs, and a design document to reproduce experiments.

---

## 🛠️ Tech Stack

- **Languages:** Python, C/C++, Java, SQL, R  
- **ML / DL:** Scikit-Learn, TensorFlow, Keras, NumPy, Pandas  
- **Audio / NLP tools:** Praat / Parselmouth, librosa, pydub, MFCC, DTW  
- **Tools:** Git, GitHub, Jupyter, Google Colab, Docker (dev)  
- **Databases / infra:** PostgreSQL, MySQL (basic), GitHub Pages for hosting

---

## 🔬 Featured Project — Mooré Text-to-Speech (TTS) Prototype

**Problem:** Mooré is a low-resource tonal language with little existing TTS support. Tonal cues change meaning, so standard TTS approaches require adaptation for accurate tone rendering.

**Approach:**
- Collected and hand-segmented a corpus of recorded Mooré sentences using Praat (syllable-level TextGrids).
- Named syllable audio files with tone annotations (1 = low, 2 = mid, 3 = high) and ARPABET-style tokens.
- Built a concatenative synthesizer in Python that maps orthography → syllable tokens (via a lexicon JSON), selects audio units, applies gentle crossfade and optional formant-preserving pitch adjustments, and outputs synthesized sentences.
- Implemented MFCC + DTW evaluation and a small MOS-style human evaluation protocol.

**Artifacts & outputs:**
- `lexicon_*.json` — orthography → token mappings (including diphthong/triphthong alternates).  
- `syllables/` — hand-cut syllable WAV tokens with tone encoding.  
- `tonal_tts_full.py` — synthesizer & demo (CLI + optional GUI).  
- `mfcc_distances.csv` — objective comparisons (combined tokens vs stitched parts).  
- `design_document.md` & `full_report.md` — implementation notes and defense material.

**Outcome:**
- Working syllable concatenation pipeline suitable for low-resource tonal languages and a reproducible evaluation workflow. Project demonstrates how linguistically informed preprocessing + data-driven evaluation produce usable speech prototypes for under-represented languages.

---
