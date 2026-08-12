# Reproducibility guide

## Scope

This repository preserves the original 2023 MSc experiments. It supports inspection and partial reruns, but it is not yet a bit-for-bit reproducibility package. The dataset, framework code, and some weights are externally hosted, and the historical runs did not preserve every seed, package version, split identifier, or hardware detail.

## Notebook inventory

- `Notebooks/YOLOv5s_Training.ipynb`
- `Notebooks/YOLOv7_Training.ipynb`
- `Notebooks/YOLOv8_Training.ipynb`
- `Notebooks/VGG16_Training.ipynb`

Treat notebook outputs as records of historical runs, not as independently verified results.

## Suggested rerun environment

Use Python 3.10 in a fresh virtual environment or container. Install dependencies separately for each architecture from the corresponding upstream version used by the notebook. The root `requirements.txt` is a broad historical environment export and contains platform-specific packages; it is not a minimal lockfile.

Credentials must be supplied through environment variables:

```bash
export ROBOFLOW_API_KEY="your-own-key"
```

Do not commit keys, tokens, service-account files, or local configuration.

## Data

The training data is linked from the README and remains governed by its provider's current terms. Record all of the following for a new experiment:

- dataset project and immutable version identifier;
- download date and license/terms;
- train/validation/test split membership;
- preprocessing and augmentation;
- class definitions and annotation changes.

Do not assume the provider's current dataset is identical to the historical 2023 snapshot.

## Minimum rerun protocol

1. Choose one notebook and a clean environment.
2. Record the Git commit, Python version, exact package versions, CUDA/cuDNN versions, GPU model, and operating system.
3. Set explicit random seeds where supported.
4. Acquire a permitted dataset version and preserve its identifier.
5. Run training without relying on saved notebook state.
6. Evaluate once on a held-out test set whose membership is recorded.
7. Save raw predictions and calculate precision, recall, F1, and mAP@0.5 using documented confidence and IoU thresholds.
8. Report total and per-image inference timing after warm-up, including batch size and hardware.
9. Compare new measurements with the historical table without replacing historical facts.

## Provenance of reported values

The README table is transcribed from Table 5 of `Report/Individual Project Report.pdf`. The report states that the test set contained 250 images. The timing methodology and hardware context are insufficient for hardware-normalized latency claims.

## Known gaps

- No immutable copy or checksum of the historical dataset snapshot.
- Incomplete environment and random-seed capture.
- Externally hosted weights.
- Small qualitative unseen-data evaluation.
- No independent replication.
- No documented demographic-fairness or adversarial-robustness evaluation.

A future reproducibility release should add data/weight checksums where redistribution is permitted, minimal per-model lockfiles or containers, split manifests, an evaluation-only script, and machine-readable result files.
