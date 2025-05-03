# ai_demo_presentation

Please note that this is meant for a demo of how AI can easily be led to believe false information. The results of each query or the leading questions in `generated_questions.txt` do not represent my beliefs.

## Overview

This is a classroom demo designed to show how artificial intelligence models can be shaped by biased or ideologically skewed training data. In just a few seconds, a simple AI system can be “taught” to echo the values of whatever documents it's fed—regardless of whether the information is accurate, fair, or ethical.

This demo is not about building a smart assistant. It's about exposing how easy it is for machine learning models to sound confident while reproducing harmful logic.

## Purpose

The goal of this project is to explore the question:  
**Can AI be re-coded to serve justice, or does it always reproduce old logics of power?**

The assignment for my class was to present a public-facing, interactive awareness campaign about my final paper topic—AI bias and algorithmic injustice. This project aims to make visible the mechanics of "machine bias" through a live demonstration.

## How It Works

1. A set of controversial, ideologically biased PDF articles is loaded into a simple AI system (using [llama-index](https://github.com/jerryjliu/llama_index)).
2. The model is then asked a series of leading or ethically loaded questions, stored in `generated_questions.txt`.
3. Responses from the model are displayed, showing how the AI internalizes and reflects the perspectives in the source texts.

Later in the demo, the same questions can be posed to a model trained on a different set of sources—such as academic or investigative journalism (e.g. Meredith Broussard or Josh Dzieza)—to compare how framing, tone, and assumptions shift.

## Key Concepts

- **Machine learning is pattern-matching, not reasoning.**
- **AI doesn’t invent values—it scales the values in its training data.**
- **Fairness in AI depends on whose definitions we embed in the system.**

This project draws on ideas from:
- *Artificial Unintelligence* by Meredith Broussard
- “AI is a Lot of Work” by Josh Dzieza
- Course materials on bias, racialized data, and sociotechnical systems

## How to Run

1. Clone or download this repository.
2. Open `AI_Presentation.ipynb` in Jupyter Notebook.
3. Install dependencies (see below).
4. Run the notebook to load PDFs and feed questions to the model.
5. Observe responses and discuss them critically.

```bash
pip install -r requirements.txt