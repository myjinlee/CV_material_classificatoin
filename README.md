> This repository is part of a **group project for a 25-2 Computer Vision course**.  
> The project focuses on exploring multi-domain feature representations for material classification.

# 📌 Overview

Material recognition requires capturing **fine-grained texture patterns, global semantic context, and frequency-level statistics** that are often overlooked by conventional vision models.
To address this, we propose a **multi-domain fusion architecture** composed of three complementary branches:
- **Vision Transformer (ViT)** for global semantic reasoning
- **DenseNet-121 (CNN)** for local texture and structural cues
- **Frequency-domain encoder** based on the 2D Fourier Transform

Each branch produces a feature embedding aligned to a shared latent space, which are then fused via concatenation and jointly classified.
