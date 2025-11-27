# SPHINX: A Synthetic Environment for Visual Perception and Reasoning

This repo is for **Sphinx**, a synthetic environment for visual perception and reasoning introduced in:

> [SPHINX: A Synthetic Environment for Visual Perception and Reasoning](https://arxiv.org/abs/2511.20814)

Hugging Face dataset (train + evaluation):  
➡️ https://huggingface.co/datasets/xashru/sphinx

---

## Repository Status
At the moment, this GitHub repo mainly serves as a landing page and pointer to the **paper** and **dataset**.  
Code will be pushed here soon once it is cleaned up.

---

## Overview

Sphinx procedurally generates visual reasoning tasks with verifiable ground-truth answers, enabling:

- Precise, fine-grained evaluation of multimodal models.
- Large-scale dataset construction for supervised training and RL-style post-training.

---

## Hugging Face Dataset

The full Sphinx dataset (training + evaluation) is hosted on Hugging Face:

- **Dataset:** https://huggingface.co/datasets/xashru/sphinx  

You can load it via `datasets`:

```python
from datasets import load_dataset

ds_train = load_dataset("xashru/sphinx", split="train")
ds_eval = load_dataset("xashru/sphinx", split="eval")  # or other splits as defined

print(ds_train[0].keys())
# e.g. image, task_name, question, answer, metadata, ...
