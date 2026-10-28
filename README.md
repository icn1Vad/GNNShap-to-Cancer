# GNNShap-to-Cancer

Undergraduate thesis experiments adapting **GNNShap-based graph explanations** to cancer-related gene data. The repository contains upstream GNNShap components alongside dataset-adaptation files and historical run records.

**PyTorch · PyTorch Geometric · Graph explanations · MCF7 / CGMega data**

[Project case study](https://icn1vad.github.io/projects/gnnshap/) · [Adaptation and reproduction notes](docs/RESEARCH_NOTES.md) · [Original upstream README](docs/UPSTREAM_GNNSHAP.md)

## What is upstream

GNNShap is the work of **Selahattin Akkas and Ariful Azad**, published at The Web Conference 2024. This repository does not claim authorship of the GNNShap method, its general benchmark implementation, or the upstream pretrained artifacts. The original setup instructions and citation are retained separately.

## Thesis focus

My work concerns dataset and model-input alignment, label and mask handling, and sampling / weighted-least-squares explanation experiments for cancer-related graph data. The repository includes `data_preprocess_cv.py`, MCF7 dataset artifacts, configuration files, and an execution log.

The historical log also records solver fallback and failures for some nodes. Finishing an iteration loop is not evidence that every explanation succeeded. No new accuracy gain, publication, or medical usefulness is claimed here.

## Start with the records

Read [the research notes](docs/RESEARCH_NOTES.md) before attempting a run. The upstream CUDA / PyG environment and project-specific dataset configuration require a separate reproduction check. The portfolio documentation change does not rerun the GPU experiments.

## Citation

Selahattin Akkas and Ariful Azad. 2024. *GNNShap: Scalable and Accurate GNN Explanation using Shapley Values*. Proceedings of the ACM Web Conference 2024.

The original repository license is preserved in [LICENSE](LICENSE).
