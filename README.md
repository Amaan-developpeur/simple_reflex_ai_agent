# 🧠 Simple Reflex AI Agent for Fundus Disease Screening

This project implements a **Simple Reflex Agent** for automated screening of retinal fundus images to classify them into four categories:  
**Cataract**, **Diabetic Retinopathy**, **Glaucoma**, and **Normal** — and take corresponding actions such as _Refer_, _Monitor_, or _Ignore_.

Inspired by the **agent architectures** from _Artificial Intelligence: A Modern Approach (AIMA)_, this project goes beyond CNN model training and builds a structured **Perceive → Decide → Act** system.

---

## 🧭 Project Goals

- ✅ Wrap a trained CNN model inside an autonomous decision-making loop.
- ✅ Simulate an environment to evaluate agent decisions.
- ✅ Design an educational, modular walkthrough for beginners to understand how to build AI agents (even reflex ones) from scratch.
- ✅ Prepare ground for building more intelligent, utility- or goal-based agents in future phases.

---

## 📂 Folder Structure

```
simple_reflex_ai_agent/
├── agent/                     ← All modular Python code
│   ├── sensor.py             ← CNN model + image perception
│   ├── decision.py           ← Decision logic based on class & confidence
│   ├── agent_loop.py         ← Agent controller (perceive → decide → act)
│   ├── environment.py        ← Simulated feedback environment
│   ├── reward.py             ← Evaluation logic
│   ├── logger.py             ← Log saving/loading
│   └── files.py              ← Image path loader
│
├── notebooks/                ← Exploratory notebooks
│   └── testing_implementation.ipynb
│
├── models/
│   └── full_model.keras      ← Pretrained MobileNetV2-based classifier
│
├── notes/
│   ├── notes.pdf
│   └── notes.docx            ← AIMA-based theory and architecture notes
│___simple_reflex_ai_agent.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```
---

## ⚙️ Tech Stack

- Python 3.8+
- TensorFlow / Keras
- NumPy, pandas, OpenCV
- Matplotlib, seaborn
- Jupyter Notebook

---

## Sample Output

Image: split/val/glaucoma/xyz.jpg
→ Predicted: Glaucoma
→ Confidence: 0.92
→ Action: Refer immediately
→ Reward: 1.0

