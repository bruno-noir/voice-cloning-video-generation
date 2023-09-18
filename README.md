# Voice Cloning and Realistic Video Generation

## Table of Contents
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Solution Architecture](#solution-architecture)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Introduction

Welcome to our Voice Cloning and Realistic Video Generation project. This project was developed to create near-real-time digital twins using advanced voice cloning and video generation techniques. The solution combines cutting-edge AI technologies to produce lifelike digital replicas of individuals, complete with their voices, expressions, and speech.

## Problem Statement

The challenge presented in the hackathon required us to develop AI models with the following capabilities:

1. **Advanced Neural Architectures**: We leveraged state-of-the-art deep learning techniques, including recurrent neural networks (RNNs), convolutional neural networks (CNNs), and generative adversarial networks (GANs), for voice cloning and realistic video generation.

2. **Expressiveness**: Our goal was to create models that could accurately convey a wide range of emotions, accents, and speaking styles. This enables expressive voice cloning and natural video generation from 2D images.

3. **Naturalness**: We focused on making the generated voice clones sound completely natural and human-like. Additionally, we paid close attention to achieving precise lip-sync and realistic video corresponding to the cloned audio.

4. **Real-Time Nature**: We built an ensemble of voice cloning and video generation models designed to operate in near real-time. This makes our solution suitable for various conversational AI applications.

## Solution Architecture

Our approach to solving this challenge involved two distinct components:

### Voice Cloning and Text-to-Speech (TTS)

We utilized the [Tortoise-TTS](https://github.com/neonbjb/tortoise-tts) repository to implement both voice cloning and text-to-speech capabilities. This component allows users to upload audio samples for voice cloning and specify text prompts for generating cloned voices.

### Realistic Video Generation

For the generation of lifelike videos with precise lip-sync, we integrated the [SadTalker](https://github.com/OpenTalker/SadTalker) repository. This component takes an input image, an audio file from the voice cloning step, and produces a video with seamless lip-sync.

To handle processing requirements efficiently and prevent crashes, we employed separate Google Colab instances for each component. Additionally, we configured ngrok with Flask to create user-friendly URLs for easy integration with a Streamlit application.

## Getting Started

### Prerequisites

Before you begin, ensure you have met the following requirements:

| Requirement       | Version    |
|-------------------|------------|
| Python            | >= 3.6     |
| TensorFlow        | >= 2.0     |
| PyTorch           | >= 1.0     |

### Installation

To install the required dependencies, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/bruno-noir/voice-cloning-video-generation.git
   
2. Install the necessary packages:

   ```bash
   pip install -r requirements.txt

## Usage

To run the entire system, follow these steps:

1. Upload the `TorTTS_API.ipynb` notebook to one Colab instance and the `Vid_API.ipynb` notebook to another Colab instance.

2. Configure ngrok APIs in both instances.

3. Enter the ngrok URLs generated in step 2 into the `app.py` file.

4. Launch the Streamlit application using the command: `streamlit run app.py`.

5. In the Streamlit application, users can perform the following actions:
   - Upload a sample audio file (.wav) with a duration of 10 to 15 seconds for voice cloning.
   - Specify a text prompt for generating speech.
   - Upload an image (.png) of the person whose voice is to be cloned.
   - Witness the magic as the system crafts a video with seamless lip-sync using the provided audio and image.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

