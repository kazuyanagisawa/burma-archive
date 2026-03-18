# AI Analysis

## OCR Analysis
This OCR analysis examines three handwritten artifacts in the archive. They include a handwritten letter by Karen medic Naw Gay and two handwritten children’s letters in Burmese. Together, these artifacts test whether AI can reliably recover fragile testimony from conflict when handwriting is uneven, language resources are limited, and human ground truth is not always available.

### Artifact Used
The primary artifact is a handwritten letter addressed to the “FBR family.” Written while the author was physically unable to speak, the letter expresses gratitude toward caregivers, reflects on recovery, and mourns the loss of a friend.  
Two additional handwritten children’s letters in Burmese were also analyzed. These letters were much shorter and visually more difficult. They provided an important second test of OCR performance when no authoritative transcription exists and confidence must be inferred through model agreement rather than direct comparison to a known text.

### Why OCR Was Used
OCR was used to test whether machine reading could help recover handwritten testimony for digital archiving. In theory, OCR can accelerate transcription and make fragile texts searchable. In practice, handwritten documents from conflict settings often resist clean extraction because of uneven handwriting, non-standard grammar, image quality issues, multilingual content, and the emotional urgency of the writing situation.

### Ground Truth Transcription
For the Naw Gay letter, a corrected manual transcription was established as the reference text.  
For the two children’s letters, no authoritative transcription was available, so performance was evaluated indirectly through model agreement.

### Reference-Based OCR Results
The English letter provided the strongest OCR test case because a manual reference text could be established. Tesseract produced near-total failure, while Gemini recovered most of the letter’s structure and emotional content. Gemini 3.1 Pro Preview performed best overall.

### OCR Outputs (Naw Gay Letter)

| Model | WER | CER | Output Excerpt |
|------|-----|-----|----------------|
| Tesseract | 93.28% | 93.28% | dio my deo.a B® peinlly |
| Gemini 2.5 Flash | 32.02% | 12.69% | Hello. My dear FBR family |
| Gemini 3.1 Pro Preview | 30.43% | 10.40% | Hello. My dear FBR family |

### Children’s Letter Analysis
Letter 1 showed extreme disagreement across models, indicating low reliability.  
Letter 2 showed strong convergence, suggesting higher confidence.

### Interpretation
OCR can assist in recovering handwritten testimony but is not reliable without human oversight. Agreement across models can serve as a proxy for confidence when no ground truth exists.

### Conclusion
OCR is useful as a support tool, not a replacement for transcription. Human verification remains essential.

---

## Classification and Tagging Analysis

### Overview
This analysis evaluates whether computer vision systems can generate useful archival tags for visual artifacts.

### Method
Tags were compared using Jaccard similarity (0 to 1 scale). Scores ranged from 0.14 to 0.50, indicating weak agreement.

### Observations
AI recognized visible objects but struggled with historical meaning. For example, landmines were misidentified as grenades.

### Interpretation
Automated tagging is useful for preliminary metadata but cannot replace human interpretation.

### Conclusion
Improved datasets, especially for underrepresented objects like landmines, could enhance performance. Future applications may include drone-based detection systems to reduce human risk.

---

## Sentiment Analysis

This section examines emotional patterns using VADER and Gemini classification.

### Key Results

| Artifact | Sentences | Avg Sentiment | Agreement |
|----------|----------|--------------|----------|
| Interview | 70 | -0.0223 | 0.7143 |
| Prayer Testimony | 124 | 0.0608 | 0.7419 |
| Letter | 17 | 0.4628 | 0.8235 |
| Protest Song | 37 | 0.0923 | 0.5946 |

### Observations
- Personal writing (letter) showed strongest agreement  
- Symbolic language (song) produced disagreement  
- Interview reflected mixed emotional patterns  

### Interpretation
Sentiment analysis highlights patterns but does not replace close reading.

### Conclusion
The tool is useful for visualization, but meaning remains rooted in human interpretation.

---

## Transcription Analysis

This analysis evaluates whether AI can transcribe Burmese audio into English.

### Results
Most models (Whisper, Gemini) failed to produce usable output.  
Only ElevenLabs produced partial results.

### Interpretation
Language support claims do not guarantee real-world performance. Burmese transcription remains unreliable.

### Conclusion
Human transcription is still required for archival accuracy.

---

## Translation Analysis

This analysis evaluates how translation affects meaning and emotional tone.

### Method
Texts were translated Burmese → English → Burmese → English.

Metrics:
- Semantic similarity (SBERT)
- Sentiment shift (VADER)

### Results

| Artifact | Similarity | Sentiment Shift |
|----------|-----------|----------------|
| Protest Song | 0.92 | 0.0735 |
| Child Letter 2 | 0.87 | — |
| Child Letter 1 | 0.78 | 0.1099 |

### Observations
- Structured language translated more consistently  
- Personal writing showed more distortion  

### Interpretation
AI preserves general meaning but loses nuance.

### Conclusion
Translation improves access but cannot replace human interpretation of meaning and tone.