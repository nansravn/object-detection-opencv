# Deploying Python ML models using Containers


## Abstract

**Case Study:** Deep learning with OpenCV, a deployment of YOLO Object Detection algorithm

This tutorial is designed to provide exposure to Azure Databricks and Azure Machine Learning Service, two solutions that can be leveraged by Professional Data Science Teams for Machine Learning experimentation and deployment requirements.

In this tutorial we will learn how to use these two services for exposing a YOLO v3 object detection algorithm as a webservice. Docker containers will be used, allowing this deployment to achieve enterprise-grade scalability and to be easily exposed on IoT + Edge Computing applications.


## Solution architecture
Below is a diagram of the solution architecture you will build in this tutorial. Please study this carefully so you understand the whole of the solution as you are working on the various components.

![](./media/media-architecture-deployment.png 'YOLO deployment overview diagram')


## Requirements

- Microsoft Azure subscription must be pay-as-you-go or MSDN
  - Trial subscriptions will not work

- Main dependencies *(python code)*
  - opencv-python==3.4.3.18
  - azureml-core==1.0.2

- **Python 2.x is not supported**


## OpenCV and YOLO Overview

OpenCV `dnn` module supports running inference on pre-trained deep learning models from popular frameworks like Caffe, Torch and TensorFlow. 

When it comes to object detection, popular detection frameworks are:
 * YOLO
 * SSD
 * Faster R-CNN
 
 Support for running YOLO/DarkNet has been added to OpenCV dnn module recently.

 You only look once (YOLO) is a state-of-the-art, real-time object detection system. On a Pascal Titan X it processes images at 30 FPS and has a mAP of 57.9% on COCO test-dev.
  

## Step-by-step tutorial

### **Step 1:** Configuration of the Development Environment
- Follow [these environment configuration steps](./01%20-%20Environment%20Configuration.md).

### **Step 2:** Deployment of the YOLO algorithm

- Import [this code](./02%20-%20Deploying%20Python%20ML%20models%20using%20Containers.ipynb) in the Azure Databricks Workspace and run it. 
  - If you have any doubts on how to import a code into an Azure Databricks Workspace, follow [this explanation](https://docs.azuredatabricks.net/user-guide/notebooks/notebook-manage.html#import-a-notebook).


#### Sample output of the deployed webservice:
![](./media/object-detection.png 'Sample image after the object detection')