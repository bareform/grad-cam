# Gradient-weighted Class Activation Mapping

Grad-CAM (Gradient-weighted Class Activation Mappings) is a method to create visual explanations for decisions from CNN-based models.

## Installation

```console
git clone https://github.com/bareform/dependencies.git
conda update -n base -c defaults conda
conda env create -f dependencies/environment.yml
conda activate bareform

git clone https://github.com/grad-cam/vit.git
cd grad-cam
```

<details>
  <summary> Dependencies (click to expand) </summary>
  
  ## Dependencies
  - Python 3.10
  - datasets
  - numpy
  - torch
  - torchvision
    
</details>

## Quick Start

You can download TorchVision pre-trained models and use the provided Jupyter Notebook `inference.ipynb` to visualize gradient weightings.

## Method

[Visual Explanations from Deep Networks via Gradient-based Localization](https://arxiv.org/abs/1610.02391)

Ramprasaath R. Selvaraju<sup>1</sup>, Michael Cogswell<sup>1</sup>, Abhishek Das<sup>1</sup>, Ramakrishna Vedantam<sup>1</sup>, Devi Parikh<sup>1</sup><sup>2</sup>, Dhruv Batra<sup>1</sup><sup>2</sup>

<sup>1</sup>Georgia Institute of Technology, <sup>2</sup>Facebook AI Research

> We propose a technique for producing "visual explanations" for decisions from a large class of CNN-based models, making them more transparent. Our approach - Gradient-weighted Class Activation Mapping (Grad-CAM), uses the gradients of any target concept, flowing into the final convolutional layer to produce a coarse localization map highlighting important regions in the image for predicting the concept. Grad-CAM is applicable to a wide variety of CNN model-families: (1) CNNs with fully-connected layers, (2) CNNs used for structured outputs, (3) CNNs used in tasks with multimodal inputs or reinforcement learning, without any architectural changes or re-training. We combine Grad-CAM with fine-grained visualizations to create a high-resolution class-discriminative visualization and apply it to off-the-shelf image classification, captioning, and visual question answering (VQA) models, including ResNet-based architectures. In the context of image classification models, our visualizations (a) lend insights into their failure modes, (b) are robust to adversarial images, (c) outperform previous methods on localization, (d) are more faithful to the underlying model and (e) help achieve generalization by identifying dataset bias. For captioning and VQA, we show that even non-attention based models can localize inputs. We devise a way to identify important neurons through Grad-CAM and combine it with neuron names to provide textual explanations for model decisions. Finally, we design and conduct human studies to measure if Grad-CAM helps users establish appropriate trust in predictions from models and show that Grad-CAM helps untrained users successfully discern a 'stronger' nodel from a 'weaker' one even when both make identical predictions.

## Citation

The original paper can be found at:
```
@misc{selvaraju2017gradcam,
    title={Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization},
    author={Ramprasaath R. Selvaraju and Michael Cogswell and Abhishek Das and Ramakrishna Vedantam and Devi Parikh and Dhruv Batra},
    year={2017},
    eprint={1610.02391},
    archivePrefix={arXiv},
    primaryClass={cs.CV},
}
```
