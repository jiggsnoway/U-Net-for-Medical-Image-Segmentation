🧠 U-Net for Medical Image Segmentation (Polyp Segmentation – Kvasir-SEG Dataset)

A Deep Learning Project by Jigyashman

📌 Overview

This project implements a full medical image segmentation pipeline using U-Net, a widely used architecture for biomedical image segmentation.
The model is trained on the Kvasir-SEG dataset to detect and segment colorectal polyps from colonoscopy images.

This repository includes:

✔ Full training pipeline

✔ Data preprocessing & augmentation

✔ PyTorch U-Net implementation

✔ Loss functions, Dice metric, and evaluation

✔ Random predictions & visualization plots

✔ Research-style performance report

✔ Final trained model weights

🧪 Dataset: Kvasir-SEG

1000 colonoscopy images

Each image has a corresponding segmentation mask

The masks highlight polyps, which are early signs of colorectal cancer

📥 Source: https://datasets.simula.no/kvasir-seg/

🧠 Model Architecture — U-Net

U-Net is perfect for medical segmentation because:

It captures detailed spatial information

Skip connections help recover fine boundaries

Works well even with small datasets

🏗 U-Net Structure (simple explanation)

1) Encoder (downsampling): learns “what” is in the image
2) Decoder (upsampling): learns “where” it is
3) Skip Connections: combine details + meaning

| Setting       | Value                            |
| ------------- | -------------------------------- |
| Image Size    | 256×256                          |
| Optimizer     | AdamW                            |
| Learning Rate | 1e-4                             |
| Epochs        | 50                               |
| Loss          | BCE + Dice Loss                  |
| Scheduler     | ReduceLROnPlateau                |
| Batch Size    | 8                                |
| Augmentation  | Flip, Rotate, Resize, Brightness |

📈 Final Model Performance
🏆 Validation Results (200 images)
| Metric         | Score               |
| -------------- | ------------------- |
| **Dice Score** | **0.8262 ± 0.1956** |
| IoU            | 0.7399 ± 0.2208     |
| Precision      | 0.8327 ± 0.2175     |
| Recall         | 0.8786 ± 0.1891     |

📊 Score Summary

Best Dice: 0.9810

Median Dice: 0.9039

Worst Dice: 0.0000 (tiny/no polyp images)

🔥 High-Quality Predictions

Dice > 0.80: 72.5% images

Dice > 0.90: 53.5% images

🥇 Comparison with Research Models
| Model                             | Dice Score |
| --------------------------------- | ---------- |
| **Your U-Net**                    | **0.8262** |
| Original U-Net (Ronneberger 2015) | ~0.75      |
| U-Net++                           | ~0.82      |
| ResUNet++                         | ~0.88      |
| PraNet (SOTA)                     | ~0.90      |

📬 Results Summary

This project demonstrates:
1) A full ML pipeline
2) Clean code, modular structure
3) Real biomedical application
4) Research-level evaluation
5) Strong performance

⭐ If you like this project, give it a star!
