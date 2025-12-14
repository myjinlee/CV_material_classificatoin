# Multi-domain Fusion Network for Robust Material Classification
> This repository is part of a **group project for a 25-2 Computer Vision course**.  
> The project investigates robust material classification by learning and fusing multi-domain visual representations.

# Overview
Material classification relies on subtle visual cues that are highly sensitive to appearance variations, such as texture degradation, color loss, and illumination changes.
To address this challenge, we propose a **Multi-domain Fusion Network (MdF)** that explicitly integrates complementary visual representations across different domains.

The proposed architecture consists of three parallel branches:

- **Vision Transformer (ViT)** for global semantic and contextual relationships
- **DenseNet-121 (CNN)** for fine-grained local texture and structural patterns
- **Frequency-domain encoder** for frequency-level statistics

Each branch produces a feature embedding aligned to a shared latent space.
These embeddings are then fused via concatenation and jointly optimized for material classification, enabling robust recognition under diverse appearance degradations.



## Training
Training requires a pre-trained Vision Transformer checkpoint fine-tuned on the MINC dataset.
- Download the checkpoint from the following link: [Download Link](https://drive.google.com/file/d/1_ebbVffV9hOIYkgDNK7AI7KOZJ-i9kv0/view?usp=sharing)
- Navigate to Cell 18 in `train.ipynb`
- Update the following line with the correct path to the downloaded checkpoint:
  ```
  VIT_WEIGHT_PATH = "path/to/your/checkpoint.pth"
  ```

## Evaluation
Evaluation requires a trained Multi-domain Fusion Network (MdF) checkpoint, obtained after training.
- Download the trained model checkpoint from the following link: [Download Link](https://drive.google.com/file/d/1Fvpa59NOVM7Sj-H1n2zGPU626UFo7mXc/view?usp=sharing)
- Navigate to Cell 36 in `demo.ipynb`
- Set the path to the trained model checkpoint:
  ```
  MODEL_PATH = "path/to/trained_fusion_model.pth"
  ```
- Set the path to the original (clean) test image to be used for perturbation:
  We provide an example image in the root directory of this repository.
  ```
  SPECIFIC_SAMPLE_PATH = "./brick_000006.jpg"
  ```



