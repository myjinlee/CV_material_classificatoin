> This repository is part of a **group project for a 25-2 Computer Vision course**.  
> The project focuses on exploring multi-domain feature representations for material classification.

# Overview

Material recognition requires capturing **fine-grained texture patterns, global semantic context, and frequency-level statistics** that are often overlooked by conventional vision models.
To address this, we propose a **multi-domain fusion architecture** composed of three complementary branches:
- **Vision Transformer (ViT)** for global semantic reasoning
- **DenseNet-121 (CNN)** for local texture and structural cues
- **Frequency-domain encoder** based on the 2D Fourier Transform

Each branch produces a feature embedding aligned to a shared latent space, which are then fused via concatenation and jointly classified.



# Training and Evaluation
## Training
Training requires a pre-trained Vision Transformer checkpoint fine-tuned on the MINC dataset.
- Download the checkpoint from the following link: [Download Link](https://drive.google.com/file/d/1_ebbVffV9hOIYkgDNK7AI7KOZJ-i9kv0/view?usp=sharing)
- Navigate to Cell 18 in `train.ipynb`
- Update the following line with the correct path to the downloaded checkpoint:
  ```
  VIT_WEIGHT_PATH = "path/to/your/checkpoint.pth"
  ```

## Testing and Evaluation
Testing requires a trained fusion model checkpoint, obtained after training.
- Download the trained model checkpoint from the following link: [Download Link](https://drive.google.com/file/d/1Fvpa59NOVM7Sj-H1n2zGPU626UFo7mXc/view?usp=sharing)
- Navigate to Cell X in `test.ipynb`
- Set the path to the trained model checkpoint:
  ```
  model_path = "path/to/trained_fusion_model.pth" (temp)
  ```



