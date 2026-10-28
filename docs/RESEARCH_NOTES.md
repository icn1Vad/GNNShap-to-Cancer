# Adaptation and reproduction notes

## Available artifacts

| Artifact | Role |
| --- | --- |
| `data_preprocess_cv.py` | Project-specific preprocessing and graph-data preparation context. |
| `config_load.py` | Configuration loading used by the data pipeline. |
| `MCF7_CPDB_dataset.pkl`, `MCF7_CPDB_dataset_final.pkl` | Saved dataset artifacts; inspect provenance and expected schema before use. |
| `dataset/configs.py`, `dataset/utils.py` | Dataset/model settings and data-loading paths. |
| `run_gnnshap.py` | Explanation entry point inherited and adapted from the upstream workflow. |
| `执行过程.txt` | Historical execution record, including failures and solver fallback. |

## Historical command

The saved log records this command:

```sh
python run_gnnshap.py --dataset CGMega --num_samples 25000   --sampler GNNShapSampler --batch_size 1024 --repeat 1
```

This is provenance, not a freshly verified quick start. The environment, matching dataset configuration, model checkpoint, and input schema must be checked first.

## What needs to be verified

1. Confirm the dataset version, labels, train/validation masks, and model input dimensions.
2. Record the PyTorch / PyG / CUDA versions and GPU-memory budget.
3. Distinguish successful explanations from node failures and solver fallback.
4. Preserve per-run settings and results before comparing sampling configurations.

The log contains “Number of players should be greater than 1” failures and switches to `WLRSolver` for large player sets. A reproduction report should count failures and explain their handling, rather than reporting the loop completion as universal success.

## Attribution

The original method, general benchmark code, and upstream pretrained models belong to the cited GNNShap work. The thesis adaptation should be assessed through its data-alignment steps, project-specific experiments, and limitations. See [the original README](UPSTREAM_GNNSHAP.md) for the upstream description.
