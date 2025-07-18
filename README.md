# BugFix-AI-Project
A Generative AI project that automatically fixes buggy code using CodeT5 and error-aware decoding

# 🧠 BugFix-AI: Intelligent Bug Repair with CodeT5 and Error-Aware Decoding

Welcome to **BugFix-AI**, a generative AI system designed to automatically detect and fix buggy source code using a fine-tuned CodeT5 model. This project bridges the gap between traditional compiler-based debugging and modern machine learning approaches by leveraging contextual understanding and error message conditioning.

---

## 📌 Project Summary

Software bugs are inevitable—but fixing them shouldn't require hours of manual effort. BugFix-AI is an end-to-end system that takes buggy Java code along with its compiler error message and returns a corrected version of the code, along with a natural language explanation.

This project was developed as part of an academic research initiative focused on **neural program repair**, with emphasis on **sequence-to-sequence learning**, **transfer learning**, and **multi-modal conditioning** (code + error message). The model used is a **fine-tuned CodeT5**, optimized to produce high-quality patches based on syntactic and semantic signals.

---

## 🏗️ Key Features

- ⚙️ **Custom Training Pipeline**  
  Fine-tuned [CodeT5-small](https://huggingface.co/Salesforce/codet5-small) model on a curated Java bug-fix dataset using HuggingFace Transformers and PyTorch.

- 💬 **Error-Aware Decoding**  
  Enhanced inference by conditioning on both the buggy code and its corresponding error message, improving patch precision.

- 🛠️ **Multi-Mode Inference Engine**  
  Choose from basic greedy decoding, beam search, or execution-based filtering modes for diverse use cases.

- 📖 **Explanation Generator**  
  Generates a human-readable explanation describing how and why the fix was applied—a powerful tool for learning and debugging.

- 🧪 **Demo-Ready and Modular**  
  Clean, modular codebase suitable for demonstrations, extensions (e.g., Python/C++), or integration into IDE plugins.

---

## 📂 Project Structure

```plaintext
BugFix-AI/
├── checkpoints/              # Trained CodeT5 model checkpoints (optional or downloadable)
├── dataset/                  # Preprocessed bug-fix dataset (JSONL format)
│   └── final_dataset.json
├── train_codet5.py           # Custom training script
├── run_inference.py          # Run inference on buggy code + error
├── generate_explanation.py   # Generate explanation using fixed and buggy code
├── requirements.txt          # Python dependencies
├── README.md                 # This file
└── utils/
    └── preprocessing.py      # Dataset loading, formatting, tokenizing utils
