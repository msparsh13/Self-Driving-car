# Udacity Self-Driving Car Project

This project implements a self-driving car simulation using **Deep Learning** and **Socket.IO**. The goal is to enable the vehicle to autonomously navigate through a track using a deep neural network (DNN) trained with behavioral cloning. The model is integrated with a web server using Socket.IO to facilitate real-time communication between the server and the simulation.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Training the Model](#training-the-model)
- [Running the Simulation](#running-the-simulation)
- [Project Structure](#project-structure)
- [License](#license)

## Project Overview

In this project, a deep learning model is trained to drive a car in a simulated environment. The model is developed using **Convolutional Neural Networks (CNN)** for image processing and behavior cloning to mimic human driving behavior. 

The car is trained to navigate the road autonomously by predicting steering angles from camera input. **Socket.IO** is used to handle the real-time communication between the simulation and the model for predicting control commands.

### Key Objectives:
1. **Data Collection**: Collect images and steering angles while driving in the simulator.
2. **Model Training**: Use a convolutional neural network to predict steering angles from images.
3. **Simulation Testing**: Test the trained model in the Udacity self-driving car simulator using real-time communication via Socket.IO.

## Installation

### Prerequisites

- Python 3.8+
- Udacity Self-Driving Car Simulator
- [Socket.IO] library
- TensorFlow/Keras for Deep Learning
- OpenCV for image processing
- NumPy for numerical computations

### Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/msparsh13/Self-Driving-car.git
  
    ```

2. Download the Udacity self-driving car simulator and open it.

3. Start the server to handle the car's communication:
    ```bash
    python drive.py model.h5
    ```

4. Run the simulator in autonomous mode.

## Technologies Used

- **Python**
- **Deep Learning**: TensorFlow/Keras
- **Socket.IO**: For real-time client-server communication
- **OpenCV**: For image processing
- **NVIDIA CNN Architecture**: For behavioral cloning model
- **Udacity Self-Driving Car Simulator**

## Dataset

The dataset consists of images and the corresponding steering angles recorded from the simulator. You can use the simulator in "Training Mode" to collect your dataset:

- **Images**: 3 front-facing camera images (left, center, right).
- **Steering Angle**: A value representing the steering angle at the time the image was captured.

### Data Preprocessing

- Crop the image to remove irrelevant parts (sky, hood of the car).
- Resize the image for faster processing.
- Normalize the pixel values to a range of -1 to 1.

## Training the Model

The model is based on NVIDIA's CNN architecture, which consists of the following layers:

- **Convolutional Layers**: For feature extraction from images.
- **Fully Connected Layers**: For predicting the steering angle.
- **Dropout Layers**: To reduce overfitting.

To train the model, run:

```bash
python train.py
```
