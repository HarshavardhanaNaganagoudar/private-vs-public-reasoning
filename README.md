# Private vs Public Reasoning

A small Ollama experiment exploring how a language model allocates information when it can choose between a **private** and **public** scratchpad.

## Question

> When a model can decide what to keep private and what to expose, does it systematically place different kinds of reasoning in the two channels?

## Experiment

The model is given a scenario containing information with different levels of relevance and sensitivity.

It can independently choose what to write to:

* **Private Scratchpad** — not intended for the user.
* **Public Scratchpad** — visible to the user.
* **Final Action** — the resulting decision.

The experiment also captures Ollama's exposed `thinking` output so the allocation can be examined alongside the model's final response.

## Setup

* Python
* Ollama
* Gemma 4 12B

```bash
pip install ollama
```

Make sure Ollama is running and the model is available:

```bash
ollama run gemma4:12b
```

## Run

Set the number of runs in `experiment.py`:

```python
NUM_RUNS = 10
```

Then:

```bash
python experiment.py
```

## Output

Each run is stored separately:

```text
outputs/
├── run_01/
│   ├── scenario.txt
│   ├── thinking.txt
│   └── response.txt
├── run_02/
│   ├── scenario.txt
│   ├── thinking.txt
│   └── response.txt
└── ...
```

`thinking.txt` contains the model's exposed reasoning trace.

`response.txt` contains the model's private/public allocation and final action.

## Goal

Look for **information asymmetry** between the private and public channels and examine what reasoning precedes those allocation decisions.
