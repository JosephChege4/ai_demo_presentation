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

1. A group of ideologically loaded PDFs (Group A or Group B) is fed into a basic AI model.
2. The system is prompted with ethically or politically charged questions from `generated_questions.txt`.
3. The model responds—often confidently—even when trained on skewed data.
4. By switching source sets, users can compare how drastically tone, values, and assumptions shift depending on the training material.

## Source Groups

- **Group A** (AI_Presentation_GroupA.ipynb): PDFs from far-right, inflammatory media outlets.
- **Group B** (AI_Presentation_GroupB.ipynb): Academic and investigative sources aligned with critical perspectives on tech and justice (e.g. Broussard, Dzieza).

Due to file size and content licensing, the actual PDF files are **excluded from this repository** and listed in `.gitignore`. You must add your own PDF sources to run the notebook.

## Why This Approach?

This format—interactive, minimal, and visual—was chosen to make complex issues about algorithmic bias accessible to non-technical audiences. It shows in real-time that:

- **Machine learning is not neutral.**
- **AI systems are only as fair as the data we give them.**
- **Even basic models can reinforce dangerous ideologies.**

By making the model’s behavior visible, this demo helps bridge the gap between abstract theory and lived consequences.

## Key Concepts

- **AI doesn’t invent logic—it amplifies existing ones.**
- **Training data is political.**
- **“Objectivity” in AI is often just well-disguised bias.**
- **Bias isn’t always about intent—it’s often structural.**

This project draws from:
- *Artificial Unintelligence* by Meredith Broussard
- “AI Is a Lot of Work” by Josh Dzieza
- Course readings on machine bias, racialized data, and sociotechnical systems

## How to Run the Demo

### Requirements

- Python 3.9+
- Jupyter Notebook
- Dependencies in `requirements.txt`

### Setup

```bash
git clone https://github.com/JosephChege4/ai_demo_presentation.git
cd ai_demo_presentation
pip install -r requirements.txt
````

Then launch the Jupyter interface:

```bash
jupyter notebook
```

### Running Either Model

You have two demo notebooks:

* `AI_Presentation_GroupA.ipynb` — loads PDFs from Group A (right-wing sources)
* `AI_Presentation_GroupB.ipynb` — loads PDFs from Group B (critical/academic sources)

Each file performs the following steps:

1. Loads the source PDFs from a directory like `./SourceGroupA/` or `./SourceGroupB/`.
2. Merges all documents into one training corpus.
3. Builds a queryable AI index using LlamaIndex.
4. Asks each question from `generated_questions.txt` and displays the responses.

## 🛠️ How to Add Your Own Sources

1. Create a folder inside the project directory called `SourceGroupC/` (or reuse A or B).
2. Add your PDF files there.
3. Open either notebook and edit this code cell:

```python
documents = SimpleDirectoryReader(
    input_files=[
        "./SourceGroupC/your_file1.pdf",
        "./SourceGroupC/your_file2.pdf"
    ]
).load_data()
```

4. Also update the `save_dir` argument here:

```python
index = build_automerging_index(
    [document],
    llm=OpenAI(model="gpt-3.5-turbo", temperature=0.5),
    save_dir="./merging_index_GroupC",
)
```

5. Rerun the notebook from the top.

That’s it! Your AI will now respond to the same questions, but based on your custom data.

## Example Questions

These are stored in `generated_questions.txt` and include prompts like:

* “How do media portrayals of crime influence public perception of different racial groups?”
* “Is there evidence to support claims of systemic racism within law enforcement agencies?”
* “How do law enforcement agencies address allegations of racial bias in their practices?”

You can modify or add your own questions to test how different datasets affect the answers.

## Limitations

This is a prototype designed for a five-minute educational demo. The model uses relatively simple tools and does not represent a production system. Its value is in revealing how AI outputs are shaped—not in optimizing or correcting them.

## Acknowledgments

Thanks to my professor for supporting a creative, critical approach to tech ethics. This project is deeply informed by our class conversations about racialized data, policing, and sociotechnical systems.