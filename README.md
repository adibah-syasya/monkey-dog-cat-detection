# YOLOv5 Monkey, Dog and Cat Detection Project
This repository contains scripts and configuration files for detecting dogs, monkeys and cats using the YOLOv5 object detection framework.

## Table of Contents
1. Project Overview
2. Getting Started
3. Dataset Preparation
4. Leveraging the trained model
5. Result
6. Credits

## 1.0 Project Overview
This project focuses on detecting dogs, monkeys, and cats. Given the recent increase in monkey and dog attacks in university dormitories, this initiative aims to enhance the safety of the university community by identifying these animals promptly.

## 2.0 Getting Started
### 2.1 Clone This Repository
First, clone this repository to your local machine:
git clone https://github.com/adibah-syasya/monkey-dog-cat-detection
cd monkey-dog-cat-detection

## 2.2 Clone Yolov5 Ultralytics
Second, clone this repo to leverage yolov5
git clone https://github.com/ultralytics/yolov5.git
cd yolov5
pip install -r requirements.txt  # install
cd ..

## 3.0 Dataset Preparation 
Dataset : https://www.kaggle.com/datasets/tarunbisht11/yolo-animal-detection-small/data
Dataset cleaning and preparation can be seen in monkeyDogCatDetection.ipynb file 
class0:monkey, class1:dog, class2:cat
Place dataset.yaml in yolov5 folder

## 4.0 Leveraging the trained model
Run the following code to leveraged trained model:
import torch
model = torch.hub.load('ultralytics/yolov5', 'custom', path='best.pt')  # Load the trained model
result = model('path/to/image.jpg')  # Run inference on an image
%matplotlib inline
plt.imshow(np.squeeze(result.render()))
results.show() 

## 5.0 Result and sample
Result of training model can be seen in results.png and sample training batch can be seen in train_batch1.png

## 6.0 Credits
This project uses the YOLOv5 framework developed by Ultralytics.

