# Pixel Coordinate Prediction using Deep Learning

## Project Overview
In this project, I built a deep learning model to predict the (x, y) position of a bright pixel in a 50×50 grayscale image. Each image contains only one pixel with value 255, while all other pixels are zero.

This problem is treated as a supervised regression task and solved using a Convolutional Neural Network (CNN).

---

## Problem Statement
Given a grayscale image where exactly one pixel is bright (value = 255), the goal is to predict the coordinates of that pixel accurately.

---

## Dataset Creation
Since no real dataset exists for this problem, I generated a synthetic dataset:

- Images are 50×50 grayscale  
- One pixel randomly set to 255  
- Remaining pixels set to 0  
- Label = pixel coordinates (x, y)

### Rationale
- Ensures unbiased spatial distribution  
- Allows generating sufficient training data  
- Focuses on spatial learning without noise

---

## Data Preprocessing
- Pixel values normalized to 0–1 range  
- Added channel dimension for CNN input  
- Dataset split into training, validation, and test sets

---

## Model Architecture
A Convolutional Neural Network (CNN) was used because it performs well on spatial image data.

Model structure:

- Conv2D + ReLU activation  
- MaxPooling layers  
- Flatten layer  
- Dense hidden layer  
- Final Dense layer with 2 outputs (x, y coordinates)

Loss Function: Mean Squared Error (MSE)  
Optimizer: Adam

---

## Results
- Training and validation loss decreased steadily  
- Predictions closely matched ground truth coordinates  
- Average prediction error was very small (less than a pixel)

This shows the model successfully learned to locate the bright pixel.

---

## Requirements

Install dependencies using:

pip install numpy tensorflow matplotlib scikit-learn

---

## How to Run

1. Open `Project.ipynb`
2. Run all cells sequentially
3. Training logs, graphs, and prediction outputs will be generated automatically

---

## Project Structure

Project.ipynb  → Main notebook with code and results  
README.md      → Project documentation  

---

## Conclusion
This project demonstrates how deep learning models, especially CNNs, can learn spatial relationships in images and accurately predict pixel coordinates using synthetic data.
