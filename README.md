# ai_demo_presentation

> **Note**: This project is a critical demo. The results of each query and the questions in `generated_questions.txt` do **not** reflect my personal views. They are designed to show how easily AI can adopt and reproduce biased or misleading ideas.

## Overview

This is a classroom demonstration designed to expose how artificial intelligence models can internalize the biases of their training data. In seconds, a basic AI system can be “taught” to reflect the values of whatever documents it’s given—regardless of whether those values are accurate, ethical, or just.

This project is not about building a helpful chatbot. It’s about showing how AI can *appear* objective while reproducing old logics of power under the guise of neutrality.

## Purpose

The driving question behind this project is:

**Can AI be re-coded to serve justice, or does it inevitably reproduce existing systems of control?**

This demo was created for an “Un-Conference” class project where students were asked to design a public-facing awareness campaign related to their research. My research focuses on AI bias and algorithmic injustice. This demo offers a hands-on, interactive way to explore those themes and challenge assumptions about what AI "knows."

## What the Demo Shows

1. A group of controversial, ideologically biased PDFs (e.g. far-right media articles) are loaded into a local AI system using [llama-index](https://github.com/jerryjliu/llama_index).
2. The system is prompted with ethically or politically charged questions, stored in `generated_questions.txt`.
3. The model responds—often confidently—despite its responses being shaped entirely by biased or misleading data.
4. Later, the same questions can be asked again using an alternative source set (e.g. academic writing or investigative journalism) to highlight how drastically the framing and tone change.

## Why This Approach?

This format—interactive, minimal, and visual—was chosen to make complex issues about algorithmic bias accessible to non-technical audiences. It shows in real-time that:

- **Machine learning is not neutral.**
- **AI systems are only as fair as the data we give them.**
- **Even basic models can reinforce dangerous ideologies.**

By making the model's behavior visible, this demo helps bridge the gap between abstract theory and practical understanding.

## Key Concepts

- **AI doesn’t invent logic—it amplifies existing ones.**
- **Training data is political.**
- **“Objectivity” in AI is often just well-disguised bias.**
- **Bias isn’t always about intent—it’s often structural.**

This project draws from the work of scholars and journalists including:
- *Artificial Unintelligence* by Meredith Broussard
- “AI Is a Lot of Work” by Josh Dzieza
- Class readings on machine bias, racialized data, and sociotechnical systems

## How to Run the Demo

### Requirements

- Python 3.9+
- Jupyter Notebook
- Dependencies in `requirements.txt`

### Instructions

```bash
git clone https://github.com/JosephChege4/ai_demo_presentation.git
cd ai_demo_presentation
pip install -r requirements.txt
