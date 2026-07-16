# Neural Style Transfer using Adaptive Instance Normalization (AdaIN)

## Project Overview

This project implements **Neural Style Transfer (NST)** using the **Adaptive Instance Normalization (AdaIN)** technique in **PyTorch**. The model combines the **content** of one image with the **artistic style** of another, producing a stylized image while preserving the original scene structure.

Unlike optimization-based neural style transfer methods, AdaIN performs **real-time style transfer** by directly aligning the feature statistics of the content and style images, making the process significantly faster and more efficient.

## How It Works

The project follows an **encoder–AdaIN–decoder** architecture:

1. **Encoder (VGG-19)** extracts deep feature representations from the content and style images.
2. **Adaptive Instance Normalization (AdaIN)** adjusts the content feature statistics (mean and standard deviation) to match those of the style image.
3. **Decoder Network** reconstructs a new image from the transformed features, generating a stylized output.

## Features

* Real-time arbitrary style transfer
* Pre-trained VGG-19 encoder
* Trainable decoder network
* Supports custom content and style datasets
* GPU acceleration using PyTorch and CUDA
* Easy inference using a pre-trained decoder model

## Dataset

The model can be trained using:

* **MS COCO 2017** dataset as the content image dataset.
* **Painter by Numbers** dataset as the style image dataset.

## Technologies Used

* Python
* PyTorch
* Torchvision
* Pillow (PIL)
* NumPy
* OpenCV
* CUDA (GPU acceleration)
* tqdm

## Project Workflow

1. Load content and style images.
2. Extract image features using a pre-trained VGG encoder.
3. Apply Adaptive Instance Normalization (AdaIN).
4. Reconstruct the stylized image using the decoder.
5. Save the generated output image.

## Results

The model successfully transfers artistic styles from paintings onto natural images while preserving the original content structure. By using a pre-trained decoder, style transfer can be performed efficiently without retraining the network.

## Future Improvements

* Support multiple style blending.
* High-resolution image generation.
* Interactive Streamlit web application.
* Video style transfer.
* Model optimization for faster inference.
