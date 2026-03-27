# A Bolu: A Dataset of Sardinian Extemporaneous Poetry 📜

A comprehensive digital collection of **Sardinian Extemporaneous Poetry Challenges** (*gara poètica*).
This dataset provides high-fidelity transcriptions of historical poetic duels in **JSON format**, designed for linguistic research, Natural Language Processing (NLP), and cultural preservation.

---

## 📋 Project Overview

This repository hosts a curated collection of improvised Sardinian poetry, primarily focused on the **Logudorese** tradition.

The dataset captures dialectical poetic exchanges (*temas*) between some of the most prominent cantadores of the 20th century. Each entry includes not only the transcribed verses but also rich metadata describing:

* the thematic context of the performance
* the poets involved
* the metrical structure
* the stanza execution time

---

## 🌍 Why this matters

Sardinian is a **low-resource language** with limited digital representation.

This dataset contributes to:

* Preservation of oral cultural heritage
* Inclusion of minority languages in NLP research
* Study of real-time constrained creativity
* Computational analysis of oral-formulaic traditions

---

## 📊 Dataset Statistics

* 📄 Total poems: **55**
* 🧩 Total stanzas: **2,835**
* 🔤 Total tokens: **141,321**
* 🧠 Unique poets: **8**

The dataset preserves incomplete and missing stanzas using explicit annotation, ensuring the structural integrity of poetic debates.

---

## 📂 Dataset Structure

Each poem is encoded in a structured hierarchical JSON format:

```json
{
  "metadata": {
    "titolo": "Title of the contest or theme",
    "fonte": "Original transcription URL",
    "intro_tema": "Historical context and poet biographies",
    "tema_centrale": "Summary of the dialectical dispute"
  },
  "trascrizione": [
    {
      "id": 1,
      "poeta": "Name of the poet (e.g., Sozu, Piras, Masala)",
      "metrica": "Poetic meter (e.g., Otada)",
      "tempo": "Stanza execution time",
      "versi": [
        "Line 1",
        "Line 2",
        "..."
      ]
    }
  ]
}
```

This structure enables:

* fine-grained linguistic analysis
* temporal modeling of performances
* stylometric and comparative studies

---

## 🚀 Usage

The dataset can be loaded in any JSON-compatible environment.

### Python example

```python
import json

with open("dataset/example.json", "r", encoding="utf-8") as f:
    data = json.load(f)

print(data["metadata"]["titolo"])
```

---

## 🧠 Research Applications

This dataset enables:

* Computational stylistics
* Stylometry and author attribution
* Study of oral-formulaic patterns
* Low-resource language modeling
* Temporal dynamics of improvised speech

It is particularly suited for investigating **formulaicity in oral traditions**, in line with the Parry–Lord theory.

---

## 🏗️ Methodology

The dataset was constructed through a multi-stage pipeline:

* Automated scraping from the Làcanas archive
* Manual philological verification
* Deduplication of performances
* Normalization of poet identities
* Structural validation of stanzas
* Temporal standardization (timestamps converted to seconds)

### Missing Data Annotation

Incomplete stanzas are explicitly marked:

* `otada` → complete stanza
* `otada*` → partially missing
* `otada**` → fully missing

This preserves the sequential structure of poetic exchanges while ensuring analytical transparency.

---

## 📁 Repository Structure

```
dataset/
  ├── poem1.json
  ├── poem2.json
  ├── ...
README.md
```

---

## ⚠️ Limitations

* Some performances are incomplete due to source constraints
* Not all sessions include opening (*esordiu*) or closing (*dispèdida*) phases
* Timing data may be missing or approximate
* The dataset is restricted to the Logudorese variety

These limitations reflect the inherent challenges of digitizing oral traditions.

---

## 🙏 Acknowledgments

We sincerely thank the Làcanas editorial team for providing access to the poetic transcriptions that constitute the core of this dataset.

Their work represents a fundamental contribution to the preservation and dissemination of Sardinian oral traditions. This dataset builds directly upon their archival efforts.

All rights to the original texts belong to their respective authors and the source platform.
This dataset is intended for research and educational purposes only.

---

## 📖 Citation

If you use this dataset, please cite:

```bibtex
@article{abolu2025,
  title={A Bolu: A Structured Dataset for the Computational Analysis of Sardinian Improvisational Poetry},
  author={Silvio Calderaro, Johanna Monti},
  year={2026}
}
```

---

## 📜 License

This dataset is released for academic and research purposes under the Creative Commons Attribution-NonCommercial-NoDerivs 4.0 International (CC BY-NC-ND 4.0) license. As the first structured digital corpus of its kind for the cantada logudorese, it is essential to maintain the philological integrity of the 2,835 stanzas and their associated metadata, including poet identifiers, metrical labels, and execution timestamps. By using A Bolu, you agree to provide appropriate credit to the authors, Silvio Calderaro and Johanna Monti, and to refrain from using this material for commercial purposes or distributing modified versions of the data. For the full legal code, please visit the https://creativecommons.org/licenses/by-nc-nd/4.0/

---
