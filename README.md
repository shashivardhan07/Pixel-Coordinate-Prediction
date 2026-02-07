Pixel Coordinate Prediction using Deep Learning
Project Overview

In this project, I built a deep learning model to predict the (x, y) position of a bright pixel in a 50×50 grayscale image. Each image contains only one pixel with value 255, while all other pixels are zero.
The task is treated as a supervised regression problem, and a Convolutional Neural Network (CNN) is used to learn the pixel location.

Problem Statement

The goal is simple: given a grayscale image where exactly one pixel is bright, the model should predict the coordinates of that pixel accurately.

Dataset Creation

Since there isn’t a real dataset for this specific problem, I generated a synthetic dataset:

Images are 50×50 grayscale.

One pixel is randomly assigned the value 255.

All other pixels are 0.

The pixel coordinates are stored as labels.

Why this approach?

It guarantees balanced spatial coverage.

It allows generating enough data quickly.

It helps focus purely on spatial learning without noise.

Preprocessing Steps

Pixel values were normalized to the range 0–1.

Images were reshaped to include a channel dimension for CNN input.

Data was split into training, validation, and test sets.

Model Used

I used a CNN because it handles spatial patterns in images well.

Model structure:

Convolution layers with ReLU activation

Max pooling layers

Flatten layer

Dense layer

Final Dense layer with 2 outputs → predicted (x, y)

Loss: Mean Squared Error (MSE)
Optimizer: Adam

Results

Training and validation loss decreased steadily.

Predictions closely matched actual pixel positions.

Average error was very small (less than a pixel).

This shows the model successfully learned how to locate the bright pixel.

Requirements

Install the required libraries:

pip install numpy tensorflow matplotlib scikit-learn

How to Run

Open Project.ipynb.

Run all cells step by step.

Training logs, graphs, and predictions will be generated automatically.

Project Files
Project.ipynb   → Main notebook with code and results
README.md       → Project documentation

Final Thoughts

This project helped me understand how CNNs can learn spatial relationships in images, even with simple synthetic data. It also demonstrates how regression can be applied to coordinate prediction problems.
