# Voices Under Fire

**Live site:** [https://kazuyanagisawa.me/burma-archive](https://kazuyanagisawa.me/burma-archive)

## Overview
**Voices Under Fire** is a digital humanities archive documenting lived experiences from Myanmar’s ongoing conflict through letters, interviews, photographs, video, and testimony.  
The project combines curation with AI-assisted analysis to examine what computational tools can recover, distort, or miss when working with fragile humanitarian records.  
Its core aim is to preserve voice while making limits of machine interpretation visible.

## Problem / Motivation
Conflict documentation is often fragmented across organizations, platforms, and formats, while the people most affected are frequently reduced to abstract categories.  
This project addresses a representation gap: how to preserve testimony as lived narrative, not just data, and how to evaluate AI tools without letting automation replace human meaning-making.

## What This Project Does
- Curates primary artifacts (audio, images, handwritten letters, testimony) into a structured public archive.
- Applies AI methods across modalities: OCR, transcription, translation, sentiment analysis, and image classification/tagging.
- Compares AI outputs against human-grounded references (ground truth where available, model-agreement checks where not).
- Connects technical results to a humanities argument about memory, resilience, and ethical interpretation.

## Key Insights
- AI tools are useful for access and triage, but unreliable as final interpreters in humanitarian contexts.
- OCR quality varies dramatically by model; weak outputs can erase emotional and narrative structure.
- Translation pipelines can preserve broad meaning while still drifting on tone, nuance, and cultural context.
- Speech transcription support claims do not guarantee usable results for Burmese field audio.
- Archives matter not only for storing evidence, but for preserving voice, context, and ethical framing.

## Methodology
The project combines qualitative close reading with quantitative evaluation.  
Multiple models and workflows were tested per modality, then compared using metrics (for example WER/CER, similarity scores, agreement rates) and interpretive review.  
Where reference transcriptions existed, outputs were scored directly; where they did not, confidence was inferred through cross-model convergence and disagreement analysis.

## Tech Stack
- **HTML/CSS** — Static site structure, navigation, and presentation.
- **Python (Google Colab)** — Analysis workflows, preprocessing, and metric calculations.
- **Gemini models** — OCR, translation, and image-description/tagging tasks.
- **OpenAI Whisper** — Speech transcription testing for Burmese audio.
- **VADER** — Sentence-level sentiment scoring and emotional arc analysis.
- **Sentence Transformers (SBERT)** — Semantic similarity for translation distortion analysis.
- **ElevenLabs Speech-to-Text** — Comparative transcription attempts in browser workflow.

## Project Structure
- **Archive** — Curated primary artifacts with metadata and interpretation.
- **AI Analysis** — Full-method pages for OCR, sentiment, transcription, translation, and classification.
- **Argument** — Long-form humanities argument integrating artifacts and scholarship.
- **Sources** — Primary, secondary, tools, and notebook references.
- **Supplementary documents**
  - `/assets/text/argument.md`
  - `/assets/text/concatenated_analyses.md`
  - `/assets/text/concatenated_artifact_descriptions.md`

## AI Usage
AI was used extensively for coding support, workflow development, and analytical assistance.  
All outputs were reviewed and edited, and final interpretive choices, narrative framing, and argumentation were human-authored.

## What I Learned
- How to work with imperfect, multilingual, and emotionally sensitive data without over-claiming certainty.
- How to evaluate AI outputs critically by separating convenience from reliability.
- How to design an end-to-end project that integrates technical analysis with historical and ethical interpretation.
- How quickly model performance can diverge across modality, language, and context.
- How to build a public-facing research artifact that serves both technical and non-technical audiences.

## Credits
- **Primary documentation networks:** Free Burma Rangers and associated field testimony contributors.
- **Academic context:** DH 150, *Artificial Intelligence and Automation in Humanities* (UCLA), taught by Dr. Nicholas Sabo.