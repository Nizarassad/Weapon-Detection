# Real-Time Gun Detection System

Research software and the supporting MSc Data Science project artifact for comparing four deep-learning approaches to gun detection: YOLOv5s, YOLOv7, YOLOv8s, and VGG16.

> **Research status:** the original project was completed in 2023. This repository is being prepared as a public research artifact in 2026. It has not been peer reviewed and is not a safety-certified detection system.

## Overview

The project investigates whether transfer learning and fine-tuning can support gun detection in CCTV-style imagery. It contains the original training notebooks, the submitted MSc report, links to the external dataset and trained weights, and a small archive used for qualitative unseen-image checks.

The work should be read as an academic experiment, not evidence that the models generalize to every weapon, camera, population, or deployment environment.

### Example test-set visual

<div align="center">
  <img height="350" src="https://drive.google.com/uc?id=1L2AJvTsN4-H7bswK1zGTtNYHExhT4wST" alt="Gun-detection test-set example" width="500" />
</div>

## Historical results

The following values are transcribed from Table 5 of the submitted project report. The reported test set contained 250 images.

| Model | Precision | Recall | F1 | mAP@0.5 | Reported test time |
|---|---:|---:|---:|---:|---:|
| YOLOv5s | 0.89 | 0.77 | 0.83 | 0.84 | 10 s |
| YOLOv7 | 0.81 | 0.73 | 0.80 | 0.80 | 13 s |
| YOLOv8s | 0.91 | 0.75 | 0.83 | 0.83 | 9 s |
| VGG16 | 0.86 | 0.85 | 0.82 | 0.81 | 20 s |

These are historical project results, not a universal benchmark. The report did not preserve enough hardware and timing detail to interpret the final column as hardware-normalized per-image latency. The qualitative evaluation also observed false positives, including detections around empty hands.

## Repository contents

- `Notebooks/` — original training and evaluation notebooks
- `Report/Individual Project Report.pdf` — submitted MSc project report
- `Models/Best Performing models.txt` — link to externally hosted trained weights
- Qualitative unseen-image testing is discussed in the report; the underlying third-party images are intentionally excluded because redistribution rights were not documented.
- `REPRODUCIBILITY.md` — rerun guidance and known reproducibility limits
- `ETHICS.md` — responsible-use and risk statement
- `RIGHTS_AND_LICENSING.md` — current rights position
- `RELEASE_CHECKLIST.md` — GitHub/Zenodo release gates

## Reproducing the experiments

Read [REPRODUCIBILITY.md](REPRODUCIBILITY.md) before running the notebooks. In brief:

1. Create an isolated Python environment.
2. Install only the dependencies required by the notebook you intend to run.
3. Obtain the dataset under its current provider terms.
4. Set `ROBOFLOW_API_KEY` in your environment; never put credentials in a notebook.
5. Record dataset version, dependency versions, hardware, random seeds, and evaluation settings for any new run.

The existing `requirements.txt` is a historical environment export, not a minimal reproducibility lockfile.

## Data and model weights

- Dataset: [Guns Dataset on Roboflow Universe](https://universe.roboflow.com/upc-tf3xi/guns-dataset-j8cz1)
- Historical trained weights: [Google Drive folder](https://drive.google.com/drive/folders/1o37wWBGuH7HGw9sc2HK1VMCc3maSKQuM?usp=sharing)

The external dataset and weights are not relicensed by this repository. Check their source terms before use or redistribution.

## Responsible use

Weapon detection is a high-consequence application. These models must not be used as the sole basis for policing, accusation, access denial, or use-of-force decisions. A real deployment would require representative local validation, human review, calibrated operating thresholds, monitoring for domain shift, documented escalation procedures, security testing, and legal/ethical review. See [ETHICS.md](ETHICS.md).

## Limitations

- The evaluation is limited in scale and domain.
- False positives and false negatives remain consequential.
- The notebooks do not fully pin data versions, dependencies, seeds, or hardware.
- The project does not establish demographic fairness, adversarial robustness, or field reliability.
- No peer-reviewed publication currently validates the claims.

## Author and academic context

**Nizar Assad**  
MSc Data Science, City, University of London  
Project supervisor: **Dr Panos Giannopoulos**

Supervisor attribution records academic supervision and does not imply repository authorship or endorsement of later releases.

## Citation

Until a DOI is issued, cite the repository using [CITATION.cff](CITATION.cff). After the first audited GitHub release is archived by Zenodo, the DOI will be added here and to the citation metadata.

## Rights

No blanket open-source license is asserted for the current mixed-content repository. See [RIGHTS_AND_LICENSING.md](RIGHTS_AND_LICENSING.md) before reuse or redistribution.
