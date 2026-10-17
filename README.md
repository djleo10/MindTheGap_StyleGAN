# Mind the Gap — One-Shot Domain Adaptation for StyleGAN

A hands-on reproduction and exploration of **"Mind the Gap: Domain Gap Control for Single Shot Domain Adaptation for Generative Adversarial Networks"**, plus the related **Retrieve in Style** method for local, part-based style transfer.

*Dheemant Jallepalli (B20BB015) — course project, IIT Jodhpur*

## What the method does

Given **one reference image** from a new domain (a painting, a cartoon, a sketch), Mind the Gap adapts a pre-trained StyleGAN2 face generator so that every face it produces can be rendered in that style, while keeping each person's identity. It builds on StyleGAN2, CLIP, StyleGAN-NADA and II2S image inversion, and adds regularisers that control the domain gap and prevent over-fitting.

## What's in the notebook

1. **Setup** — clones the official MTG code and downloads the pre-trained models (FFHQ StyleGAN2 and others)
2. **Embed your own face** — aligns an uploaded photo and inverts it into StyleGAN's latent space with II2S (better quality) or e4e (near real-time)
3. **Pre-trained styles** — applies ready-made domains (Picasso, Moana, Joker, sketch and more) to the embedded face
4. **Train on your own style image** — runs the MTG optimisation and plots the training loss
5. **Retrieve in Style** — clusters StyleGAN features into face parts (eyes, nose, mouth, hair…) to transfer style locally

## Repository contents

| File | What it is |
|---|---|
| `Mind_The_Gap_StyleGAN.ipynb` | Colab notebook with all the experiments above (needs a GPU) |
| `B20BB015_Major_Exam.pdf` | Presentation: paper summary, implementation, changes made and results |

## Credits

Original methods and code: [ZPdesu/MindTheGap](https://github.com/ZPdesu/MindTheGap) and [mchong6/RetrieveInStyle](https://github.com/mchong6/RetrieveInStyle).
