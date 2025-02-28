# dataset-safari
Exploring some cool datasets from AI conferences in 2024

# Dataset Safari 🦁

Exploring interesting datasets from AI conferences in 2024. This repository contains analysis and insights from various machine learning datasets presented at major AI conferences.

## Overview

This repository serves as a collection of exploratory data analysis (EDA) and insights from notable datasets introduced in AI conferences during 2024. Each dataset exploration includes basic statistics, visualizations, and key findings.

# Datasets Explored

## BIOSCAN-30k
<img src="assets/bioscan-explore.gif">

- **Name**: BIOSCAN-30k (subset of BIOSCAN-5M)

- **Conference**: NeurIPS 2024

- **Description**: A multimodal dataset of arthropod specimens (98% insects) featuring high-resolution images, DNA barcode sequences, and detailed taxonomic information. This is a 30k sample subset of the larger BIOSCAN-5M dataset.

- **Key Features**: 
  - High-resolution microscope images (1024×768px)
  - DNA barcode sequences (COI gene) and BIN clusters
  - 7 taxonomic ranks (phylum to species)
  - Geographical metadata (country, province/state, coordinates)
  - Specimen size metadata

- **My Additional Analysis**:
  - BioCLIP for visual embeddings
  - BarcodeBERT for DNA sequence analysis
  - UMAP visualization
  - Uniqueness and representativeness metrics


## ImageNet-D

<img src="assets/imagenet-d.gif">

- **Name**: ImageNet-D

- **Conference**: CVPR 2024

- **Description**: A challenging benchmark dataset of synthetically generated images (via Stable Diffusion) designed to test the robustness of image classification models. Contains 4,835 "hard images" that were specifically selected for being difficult for current vision models to classify correctly.

- **Key Features**: 
  - 4,835 synthetic images across 113 categories
  - Overlapping categories with ImageNet and ObjectNet
  - 547 nuisance variations including:
    - 3,764 background variations
    - 498 texture variations
    - 573 material variations

- **My Additional Analysis**:
  - CLIP for zero-shot classification
  - AIMv2 for visual understanding
  - UMAP visualization
  - Model performance comparison
  - Hardness analysis

## Illusion Animals
<img src="assets/illusion_animals_initial_explore.gif">

- **Name**: Illusion Animals

- **Conference**: COLM 2024 

- **Description**: A dataset of animal images with intentionally created visual illusions, designed to test how well AI models can perceive both real and illusory elements in images. Part of the larger Illusory VQA benchmark collection.

- **Key Features**: 
  - 4,400 total images (3,300 training, 1,100 test samples)
  - Generated using SDXL-Lightning and ControlNet
  - Multiple image versions:
    - Raw images (original animals)
    - Illusory images (with visual illusions)
    - Filtered images (Gaussian blur + grayscale)
    - "No illusion" class included
  - Human-validated illusions

- **My Additional Analysis**:
  - CLIP for zero-shot classification
  - SigLIP 2 for visual understanding
  - AIMv2 for multimodal analysis
  - Visual Question Answering with Janus-Pro and Moondream2
  - UMAP visualization for embedding analysis

### SkyScenes

- **Name**: SkyScenes

- **Conference**: ECCV 2024 

- **Description**: A comprehensive synthetic dataset for aerial scene understanding containing 33,600 aerial images captured from UAV perspectives using the CARLA simulator. Designed to enable research in aerial imagery analysis and model robustness across different conditions.

- **Key Features**: 
  - 33.6K synthetic aerial images across:
    - 8 town layouts (7 urban + 1 rural)
    - 5 weather/time conditions
    - 12 viewpoint combinations
  - Dense annotations including:
    - Semantic segmentation (28 classes)
    - Instance segmentation
    - Depth information
  - Systematic variations:
    - Heights: 15m, 35m, 60m
    - Pitch angles: 0°, 45°, 60°, 90°
    - Weather conditions: ClearNoon, ClearSunset, ClearNight, CloudyNoon, MidRainyNoon

- **My Additional Analysis**:



## Citations

```bibtex
@misc{gharaee2024bioscan5m,
    title={{BIOSCAN-5M}: A Multimodal Dataset for Insect Biodiversity},
    author={Zahra Gharaee and Scott C. Lowe and ZeMing Gong and Pablo Millan Arias
        and Nicholas Pellegrino and Austin T. Wang and Joakim Bruslund Haurum
        and Iuliia Zarubiieva and Lila Kari and Dirk Steinke and Graham W. Taylor
        and Paul Fieguth and Angel X. Chang
    },
    year={2024},
    journal={NeurIPS},
}
```

```bibtex

@article{zhang2024imagenet_d,
  author    = {Zhang, Chenshuang and Pan, Fei and Kim, Junmo and Kweon, In So and Mao, Chengzhi},
  title     = {ImageNet-D: Benchmarking Neural Network Robustness on Diffusion Synthetic Object},
  journal   = {CVPR},
  year      = {2024},
}
```

```bibtex
@article{zhang2024webuot,
  title={WebUOT-1M: Advancing Deep Underwater Object Tracking with A Million-Scale Benchmark},
  author={Zhang, Chunhui and Liu, Li and Huang, Guanjie and Wen, Hao and Zhou, Xi and Wang, Yanfeng},
  journal={NeurIPS},
  year={2024}
}
```

```bibtex
@misc{rostamkhani2024illusoryvqabenchmarkingenhancing,
      title={Illusory VQA: Benchmarking and Enhancing Multimodal Models on Visual Illusions}, 
      author={Mohammadmostafa Rostamkhani and Baktash Ansari and Hoorieh Sabzevari and Farzan Rahmani and Sauleh Eetemadi},
      year={2024},
      eprint={2412.08169},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2412.08169}, 
}
```

```bibtex
@misc{khose2023skyscenes,
      title={SkyScenes: A Synthetic Dataset for Aerial Scene Understanding}, 
      author={Sahil Khose and Anisha Pal and Aayushi Agarwal and Deepanshi and Judy Hoffman and Prithvijit Chattopadhyay},
      year={2023},
      eprint={2312.06719},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```