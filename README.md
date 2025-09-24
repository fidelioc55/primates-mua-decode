
## 📘 Notebooks Overview

### `monkeys_retrieve.ipynb`: Analysis & Decoding

1. **Image Extraction**
   - Loading and visual inspection of visual stimuli.

2. **Neural Response Collections**
   - Using a 200 ms post-stimulus window, temporally aligned with stimulus onset.
  
3. **Average Activity Over Repetitions**
   - Averaging across stimulus repetitions to reduce noise.

4. **Time Neural Network**
   - Simple Temporal attention network to aggregate dynamic neural patterns.

5. **PCA on Channels (Scaling Law)**
   - Dimensionality reduction and scaling behavior inspection over input channels.

6. **Random Subsampling (Scaling Law)**
   - Analysis of training set size impact on decoding performance.

### `monkeys_gener.ipynb`: Generative Decoding Pipeline

1. **Neural Data Preprocessing**
   - Feature preparation from averaged neural signals.

2. **Soft Mapping Model**
   - Light MLP with attention for mapping neural activity to visual and structural latent space.

3. **Structural Decoding**
   - Image generation via Stable Diffusion XL using predicted latents.

4. **Rejection Sampling**
   - Ranking multiple generated images by structural similarity to the predicted latent representation.

5. **Final Reconstruction**
   - Selection of the most plausible reconstruction based on SSIM.

---

## 📊 Key Results & Visualizations

- 🔥 **Attention Heatmaps**  
  - Visual attention across timepoints reveals model focus during decoding.

- 🧠 **Latent Reconstructions**  
  - Predicted latent vectors compared with true latents, visualized via SSIM or cosine similarity.

- 🖼️ **Generated Images**  
  - Output of the generative pipeline using Stable Diffusion XL, with visual comparison to target or retrieved images.

---

## ✅ Conclusion

This pipeline demonstrates that:

- Simple attention-based models can outperform more complex architectures in neural decoding.
- Modeling temporal structure in neural activity is key to decoding accuracy.
- A modular generative decoder with latent reconstruction and semantic ranking produces plausible image reconstructions.
