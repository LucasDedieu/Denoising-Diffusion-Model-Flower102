# Denoising Diffusion Model for Flower102 Dataset Image Generation

This repository contains a notebook that implements a simple diffusion model from scratch on Flower102 dataset using PyTorch. The goal of this project is to train a Unet model to generate flower images from random noise.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)

## Introduction

The Denoising Diffusion Model is a powerful technique for generating high-quality images by removing noise from noisy inputs. It belongs to the family of generative models and leverages the concept of diffusion processes to iteratively refine images over multiple steps.

In image generation tasks, noise removal is a critical step as it helps produce clean and realistic images. The Denoising Diffusion Model addresses this challenge by treating the generation process as a diffusion process. It gradually transforms a noisy input image into a clean and visually appealing output image.

The model achieves this by applying a series of noise levels to the input image, and at each step, it progressively reduces the noise to reveal more details and structure. The diffusion process is controlled by a noise schedule that determines how the noise level evolves over time.

## Installation

You can install these dependencies by running the following command:

```
pip install -r requirements.txt
```

## Usage

1. Clone the repository and navigate to the project directory.

2. Launch Jupyter Notebook.

3. Open the `diffusion_model.ipynb` notebook.

4. Follow the instructions in the notebook to execute the code cells.

## Results

The notebook will guide you through the following steps:

1. Data exploration

2. Forward Process of denoising diffusion models (add noise to an image using linear or cosine scheduler)

3. Backward process of denoising diffusion models (remove noise from an image using a Unet neural network)

4. Training of the model

5. Evaluate the model both visually and using FID

## Results

I have train the Unet model using a Nvidia 3080ti GPU. But with only 12GB of vram I had to resize my images to only 64x64 resolution and use a batch size of 128. It took me around 700 epochs and a few dozen hours to get good results.

Here are some examples of generated images :

![alt text](https://github.com/LucasDedieu/Denoising-Diffusion-Model-Flower102/blob/main/results.PNG?raw=true)


## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
