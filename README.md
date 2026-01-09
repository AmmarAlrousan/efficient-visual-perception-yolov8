# Efficient Visual Perception with a Lightweight YOLOv8 Architecture

This repository presents an **applied research project** focused on improving
the efficiency of visual perception systems through architectural optimization
of the YOLOv8 model.

The work proposes a **lightweight modification of YOLOv8m using channel pruning**
to reduce computational cost while maintaining competitive detection performance
in **dense visual environments**, with retail shelf detection as a case study.

---

## 🎯 Motivation

Recent advances in visual perception have achieved high accuracy, but deploying
such models in real-world scenarios often faces **computational and resource constraints**.

While prior work by the author focused on **facial emotion recognition at the
classification level**, this project extends the research direction toward
**efficient visual perception at the detection level**, addressing scalability
and deployment challenges.

---

## 🧠 Research Contribution

The main contribution of this work is a **deployment-oriented optimization** of
YOLOv8m through architecture-aware channel pruning:

- A pruned YOLOv8m architecture that significantly reduces model size and GFLOPs.
- Preservation of detection performance with minimal degradation.
- A practical efficiency–accuracy trade-off suitable for dense object detection.

The proposed model serves as an **applied research extension** rather than a
pure engineering or benchmarking project.

---

## 🧩 Method Overview

The optimization pipeline follows these steps:

1. Layer-wise sensitivity analysis to identify low-impact channels.
2. Channel pruning (20–40%) applied to selected C2f blocks in the backbone.
3. Limited pruning in neck layers to preserve feature aggregation.
4. Fine-tuning of the pruned architecture on a dense retail dataset.

The detailed methodology is documented in `docs/methodology.md`.

---

## 📊 Results Summary

A quantitative comparison between the original and pruned YOLOv8m models is
provided in `results/tables/comparison.md`.

Key outcomes include:
- ~31% reduction in parameters
- ~38% reduction in GFLOPs
- ~31% reduction in model size
- Limited performance drop (2–5% across key metrics)

Qualitative detection examples are shown in `results/figures/`.

---

## 📁 Repository Structure


efficient-visual-perception-yolov8/
│

├── configs/ # Proposed pruned YOLOv8m architecture

├── experiments/ # Pruning analysis and training notebooks

├── results/ # Quantitative tables and qualitative figures

├── data/ # Dataset description and access links

├── docs/ # Related work and methodology

├── requirements.txt

└── README.md


---

## 📦 Dataset

Experiments were conducted on a dense retail shelf dataset.

- Dataset: **SKU110K**
- Dataset access information is provided in `data/dataset_link.txt`.

The dataset is not included due to licensing restrictions.

---

## 🔬 Related Work and Attribution

This project is inspired by the pruning strategy proposed in:

Zhang et al., *Optimization of YOLOv8 Model Based on Pruning*, 2024.

The general pruning concept is adapted to dense retail environments and
deployment-oriented constraints. Full attribution is provided in
`docs/related_work.md`.

---

## ⚠️ Scope and Limitations

Due to limited computational resources, this work focuses on a single pruning
configuration that balances efficiency and performance.

Exploration of additional pruning ratios and automated pruning strategies is
left for future work.

---

## 🔮 Future Directions

- Evaluation on additional dense object detection datasets.
- Exploration of structured and automated pruning strategies.
- Integration into broader human-centered visual perception pipelines.
- Extension toward multi-task perception systems.

---

## 📬 Contact

**Ammar Alrousan**  
AI Student | Research-Oriented  
GitHub: https://github.com/AmmarAlrousan  
Email: ammaraimaster@gmail.com
