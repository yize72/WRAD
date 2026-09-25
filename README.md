# WRAD

WRAD is an image dataset organized for research, education, and reproducible experiments. The repository currently provides predefined training and validation subsets. Please read the citation, usage, and disclaimer sections before using or redistributing the data.

## Dataset overview

- Total images: **1,002 JPEG files**
- Training set: **794 images**
- Validation set: **208 images**
- Approximate repository data size: **2.3 GB**
- Main filename groups: `LI`, `MJ`, `RJ`, `MIX`, and `T-*`

The filename codes are retained from the source dataset. They should not be interpreted as formal class definitions unless a separate annotation or data description explicitly defines them.

## Directory structure

```text
WRAD/
├── README.md
├── train/
│   └── images/
│       └── *.jpg
└── val/
    └── images/
        └── *.jpg
```

## Download

Clone the complete repository with Git:

```bash
git clone https://github.com/yize72/WRAD.git
cd WRAD
```

Because the dataset is large, downloading may take some time and requires sufficient disk space and a stable network connection.

## Basic use

The repository supplies image files and a predefined train/validation split. Users should independently verify file integrity, image properties, class definitions, and suitability for their intended analysis before training or evaluation.

Example file discovery in Python:

```python
from pathlib import Path

root = Path("WRAD")
train_images = sorted((root / "train" / "images").glob("*.jpg"))
val_images = sorted((root / "val" / "images").glob("*.jpg"))

print(f"Training images: {len(train_images)}")
print(f"Validation images: {len(val_images)}")
```

## Citation

If WRAD contributes to a publication, report, dataset, software project, presentation, or other public result, please cite this repository and include the repository URL. Until a formal paper or DOI is released, the following citation may be used:

```bibtex
@misc{wrad2026,
  author       = {{WRAD Contributors}},
  title        = {WRAD: Image Dataset},
  year         = {2026},
  howpublished = {GitHub repository},
  url          = {https://github.com/yize72/WRAD},
  note         = {Accessed: YYYY-MM-DD}
}
```

Please replace `YYYY-MM-DD` with the date on which you accessed the dataset. If a formal publication or DOI becomes available, cite that record in addition to this repository.

## Usage requirements

By using this repository, users are requested to:

1. Cite WRAD in public outputs derived from the dataset.
2. Clearly describe any filtering, relabeling, preprocessing, augmentation, or train/validation changes.
3. Avoid presenting modified data as an unchanged official WRAD release.
4. Preserve attribution and a link to the original repository when sharing derived materials.
5. Use the data lawfully and ethically, and comply with applicable institutional, contractual, privacy, and intellectual-property requirements.
6. Contact the maintainer before commercial use, substantial redistribution, or inclusion in another public dataset.

No standalone license file is currently provided. Availability on GitHub does not by itself grant unrestricted permission to copy, redistribute, sublicense, or use the dataset commercially. Contact the maintainer if your intended use requires explicit permission.

## Disclaimer

WRAD is provided **as is**, without warranties or guarantees of accuracy, completeness, fitness for a particular purpose, or uninterrupted availability. The dataset may contain labeling errors, duplicates, artifacts, sampling bias, or other limitations. Users are responsible for validating the data and evaluating the reliability, fairness, and safety of any model or conclusion derived from it.

The dataset should not be used as the sole basis for safety-critical, medical, legal, regulatory, financial, or other high-impact decisions. The maintainers are not responsible for losses, claims, or damages arising from use, misuse, interpretation, redistribution, or inability to use the dataset.

If you identify questionable content, incorrect attribution, duplicate material, privacy concerns, or other issues, please contact the maintainer so the repository can be reviewed.

## Contact

- GitHub: [yize72](https://github.com/yize72)
- Repository issues: [WRAD Issues](https://github.com/yize72/WRAD/issues)
- Email: [3265529455@qq.com](mailto:3265529455@qq.com)

For questions about access, citation, collaboration, corrections, or reuse permission, open a GitHub issue or contact the maintainer by email. Please include `WRAD` in the subject line.

## Versioning

The Git commit history records dataset updates. For reproducible work, record the commit hash used in your experiment or publication:

```bash
git rev-parse HEAD
```
