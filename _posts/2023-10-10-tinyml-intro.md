---
layout: post
title: TinyML
subtitle: An Introduction and my understanding!
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [books, test]
---

# TinyML – An Overview

## Introduction

The Internet of Things (IoT) has revolutionized the way we interact with technology by enabling seamless and real-time processing of data from millions of interconnected sensors and devices. Edge computing, a computing paradigm that operates near the user, plays a crucial role in IoT. In this context, TinyML emerges as a powerful tool for on-device analytics, particularly for sensing modalities such as audio, vision, and speech. TinyML models are designed to have low power, memory, and computing requirements, making them ideal for embedded networks and battery-powered devices. Let's delve into the basics of TinyML and its workflow.

## Basic Flowchart and Workflow

### 1. Dataset
- **Collection**: Start by aggregating and classifying your dataset. For tasks like object detection, labeling tools like LabelImg can be invaluable.
- **Source**: Datasets are available from sources like Kaggle and Roboflow, or you can create a custom dataset for specific requirements.

### 2. Model Training
- **Choose Model**: Decide whether to use a custom or pretrained model. Pretrained models like YOLO, VGG-16, or DenseNet are quick to train and often highly accurate.
- **Metrics**: Evaluate model performance using metrics like Accuracy, Loss, F1 Score, Precision, AUC, etc.

### 3. Model Conversion
- **Optimization**: Given the constraints of edge devices, optimize your model to reduce its size and convert it into a lightweight format known as a TFLite model.
- **Hexadecimal Conversion**: Convert the TFLite model to a hexadecimal array of bytes, which microcontrollers can understand. Store this as a C header file (.h).

### 4. Deployment
- **Implementation**: Deploy the model binaries onto the microcontroller, allowing it to perform on-device inference. This completes the TinyML workflow.

## Advantages of TinyML

1. **Decentralization**: TinyML empowers microcontrollers to make decisions independently, reducing server workload and costs.
2. **Latency**: On-device processing eliminates the need to transfer data to a server, reducing latency.
3. **Energy Savings**: Microcontrollers consume minimal power, extending device battery life and reducing server infrastructure costs.
4. **Reduced Bandwidth**: With on-device sensors, there's no constant transfer of raw sensor data to servers, conserving bandwidth.
5. **Data Privacy**: Data remains on the edge device, enhancing data privacy.

## Disadvantages of TinyML

1. **Security**: Ensuring TinyML model security may require complex and risky firmware updates, especially in distributed IoT environments.
2. **Performance and Accuracy**: Limited processing power, memory, and energy on edge devices can restrict model complexity, potentially reducing performance and accuracy.
3. **Service and Maintenance**: TinyML models may need periodic updates or retraining, which can be resource-intensive.

## Applications

### Automotive
- **Driver Drowsiness Detection System**: Utilize TinyML to monitor driver alertness in real-time, enhancing road safety.
- **Automobile Blind Spot Management System**: Manage blind spots efficiently without the need for continuous cloud connectivity.

### Non-Automotive
- **Agriculture**: Use TensorFlow Lite to diagnose plant ailments without internet connectivity, benefiting farmers in remote areas.
- **Retail**: Implement TinyML to monitor inventory levels and send alerts when stock is low, aiding inventory management.

## Tools and Techniques

1. **Data Collection using Sensors**: Collect data from sensors, providing input to the microcontroller.
2. **ML Model Embedded with Microcontroller**: Deploy the trained ML model in a microcontroller-friendly format.
3. **Input from Sensor -> Microcontroller Decision**: Process sensor data with the embedded ML model to make decisions.
4. **Actuators Perform Based on Decision**: Actuators execute actions based on the microcontroller's decisions, controlling various output devices.

TinyML is a promising technology with the potential to transform IoT by enabling intelligent, low-power edge devices. As it continues to evolve, TinyML will find applications across various domains, addressing the challenges and opportunities presented by the IoT landscape.
