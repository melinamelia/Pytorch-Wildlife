![improv logo copy](https://github.com/melinamelia/Pytorch-Wildlife/assets/159795416/168c62c0-c827-4c7e-953b-3093b68c8a2b) &nbsp; &nbsp; &nbsp; ![image](https://github.com/melinamelia/Pytorch-Wildlife/assets/159795416/e3f007b9-53c5-433c-be00-5240e4438bd2)

# Pytorch-Wildlife
  A Collaborative Deep Learning Framework for Conservation
## 🐾 Introduction

At the core of our mission is the desire to create a harmonious space where conservation scientists from all over the globe can unite. Where they're able to share, grow, use datasets and deep learning architectures for wildlife conservation.
>[!NOTE]
>We are expanding the CameraTraps repo to introduce **Pytorch-Wildlife**, a Collaborative Deep Learning Framework for Conservation.

We've been inspired by the potential and capabilities of Megadetector, and we deeply value its contributions to the community. **As we forge ahead with Pytorch-Wildlife, under which Megadetector now resides, please know that we remain committed to supporting, maintaining, and developing Megadetector, ensuring its continued relevance, expansion, and utility.**

To use the newest version of MegaDetector with all the exisitng functionatlities, you can use our newly developed [user interface](https://github.com/microsoft/CameraTraps?tab=readme-ov-file#explore-pytorch-wildlife-and-megadetector-with-our-user-interface) or simply load the model with **Pytorch-Wildlife** and the weights will be automatically downloaded:
```
from PytorchWildlife.models import detection as pw_detection
detection_model = pw_detection.MegaDetectorV5()
```
For those interested in accessing the previous MegaDetector repository, which utilizes the same `MegaDetector v5` model weights and was primarily developed by Dan Morris during his time at Microsoft, please visit the [archive](https://github.com/microsoft/CameraTraps/blob/main/archive) directory, or you can visit this [forked repository](https://github.com/agentmorris/MegaDetector/tree/main) that Dan Morris is actively maintaining.

If you have any questions regarding MegaDetector and Pytorch-Wildlife, please [email us](zhongqimiao@microsoft.com)!

## 👋 Welcome to Version 1.0

**PyTorch-Wildlife** is a platform to create, modify, and share powerful AI conservation models. These models can be used for a variety of applications, including camera trap images, overhead images, underwater images, or bioacoustics. Your engagement with our work is greatly appreciated, and we eagerly await any feedback you may have.

The **Pytorch-Wildlife** library allows users to directly load the `MegaDetector v5` model weights for animal detection. We've fully refactored our codebase, prioritizing ease of use in model deployment and expansion. In addition to `MegaDetector v5`, **Pytorch-Wildlife** also accommodates a range of classification weights, such as those derived from the Amazon Rainforest dataset and the Opossum classification dataset. Explore the codebase and functionalities of **Pytorch-Wildlife** through our interactive `Gradio` web app and detailed Jupyter notebooks, designed to showcase the practical applications of our enhancements at [PyTorchWildlife](https://github.com/microsoft/CameraTraps/blob/main/INSTALLATION.md). You can find more information in our [documentation](https://cameratraps.readthedocs.io/en/latest/).

👇 Here is a brief example on how to perform detection and classification on a single image using `PyTorch-wildlife`
```
import torch
from PytorchWildlife.models import detection as pw_detection
from PytorchWildlife.models import classification as pw_classification

img = torch.randn((3, 1280, 1280))

# Detection
detection_model = pw_detection.MegaDetectorV5() # Model weights are automatically downloaded.
detection_result = detection_model.single_image_detection(img)

#Classification
classification_model = pw_classification.AI4GAmazonRainforest() # Model weights are automatically downloaded.
classification_results = classification_model.single_image_classification(img)
```
## 🕵️ Explore Pytorch-Wildlife and MegaDetector with our User Interface

If you want to directly try **Pytorch-Wildlife** with the AI models available, including `MegaDetector v5`, you can use our **Gradio** interface. This interface allows users to directly load the `MegaDetector v5` model weights for animal detection. In addition, **Pytorch-Wildlife** also has two classification models in our initial version. One is trained from an Amazon Rainforest camera trap dataset and the other from a Galapagos opossum classification dataset (more details of these datasets will be published soon). To start, please follow the [installation instructions](https://github.com/microsoft/CameraTraps/blob/main/INSTALLATION.md) on how to run the Gradio interface! We also provide multiple [**Jupyter** notebooks](https://github.com/microsoft/CameraTraps/tree/main/demo) for demonstation.

![image](https://github.com/melinamelia/Pytorch-Wildlife/assets/159795416/81419fb5-9a7e-41f4-9581-856838d5ea55)


## 🛠️ Core Features
   What are the core components of Pytorch-Wildlife?

### 🌐 Unified Framework:
  Pytorch-Wildlife integrates **four pivotal elements:**

▪ Machine Learning Models<br>
▪ Pre-trained Weights<br>
▪ Datasets<br>
▪ Utilities<br>

### 👷 Our work:
  In the provided graph, boxes outlined in red represent elements that will be added and remained fixed, while those in blue will be part of our development.
<br>

### 🚀 Inaugural Model:
  We're kickstarting with YOLO as our first available model, complemented by pre-trained weights from `MegaDetector v5`. This is the same `MegaDetector v5` model from the previous repository.
<br>

### 📚 Expandable Repository:
  As we move forward, our platform will welcome new models and pre-trained weights for camera traps and bioacoustic analysis. We're excited to host contributions from global researchers through a dedicated submission platform.
<br>

### 📊 Datasets from LILA:
  Pytorch-Wildlife will also incorporate the vast datasets hosted on LILA, making it a treasure trove for conservation research.
<br>

### 🧰 Versatile Utilities:
  Our set of utilities spans from visualization tools to task-specific utilities, many inherited from Megadetector.
<br>

### 💻 User Interface Flexibility:
  While we provide a foundational user interface, our platform is designed to inspire. We encourage researchers to craft and share their unique interfaces, and we'll list both existing and new UIs from other collaborators for the community's benefit.
<br>

Let's shape the future of wildlife research, together! 🙌

### 📈 Progress on core tasks

#### ▪️ Tasks

- [ ]  Animal detection<br>
- [x] Mega detector<br>
- [x] User submitted weights<br>
- [ ] Animal classification<br>
- [x] Amazon Rainforest Datasets<br>
- [x] Amazon Opossum calssification<br>
- [ ] User submitted weights<br>

#### ▪️ Utility Toolkit

- [x] Visualization tools<br>
- [ ] Megadetector utils<br>
- [ ] User submitted utils<br>

#### ▪️ Datasets

- [ ] Animal Datasets<br>
- [x] LILA datasets<br>

#### ▪️ Accesibilty

- [x] Basic user interface<br>
- [ ] UI Dev tools<br>
- [ ] List of available UIs<br>

### 🗺️ Development roadmap

#### October 0.1
✔️ Packaging

- [x] 1.1.1 Add the YOLOv5 detection model.<br>
- [x] 1.1.1 Add the Megadetector pretrained weights.<br>
- [x] 1.1.3 Add a Notebook to create, load and run inference on the YOLOv5 detection model using Megadetector pretrained weights.<br>
- [x] 1.3.1-1.3.2 Add an animal species classification model and pretrained weights.

#### November 0.2
✔️ Packaging

- [x] 1.4.2-1.4.3 Add a documented animal video detection pipeline.<br>
- [x] 1.5.1 Add a user-friendly interface for animal detection.<br>
- [x] 1.2.2 Add a module for custom datasets.<br>
- [x] 1.3.3 Add a Jupyter notebook for the video detection tutorial.

#### December 0.3
✔️ Packaging

- [x] 1.5.2 Add the video detection pipeline to the user interface.<br>
- [x] 1.5.3 Add animal classification to the user interface.<br>
- [x] 1.5.4 Complete documentation on how to use the user-interface.<br>
- [x] 1.1.2 Add a module for fine-tuning and training from scratch.<br>
- [x] 1.2.1 Add a dataset module to download LILA subsets.<br>
- [x] 1.2.1 Add visualization functions for LILA subsets.

- [ ] 
