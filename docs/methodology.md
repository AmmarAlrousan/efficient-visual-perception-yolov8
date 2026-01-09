## Methodology Overview

The proposed approach focuses on reducing the computational cost of YOLOv8m
through architecture-aware channel pruning.

### Key Steps
- Conducted layer-wise sensitivity analysis to identify low-impact channels.
- Applied 20–40% channel pruning on selected C2f blocks in the backbone.
- Applied limited pruning on neck layers to preserve feature aggregation.
- Fine-tuned the pruned architecture on a dense retail dataset.

### Scope
Due to limited computational resources, a single pruning configuration was
evaluated in detail. Further exploration of pruning ratios is left for future work.
