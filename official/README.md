<div align="center">
  <img src="https://storage.googleapis.com/tf_model_garden/tf_model_garden_logo.png">
</div>

# TensorFlow Official Models

The TensorFlow official models are a collection of models
that use TensorFlow’s high-level APIs.
They are intended to be well-maintained, tested, and kept up to date
with the latest TensorFlow API.

They should also be reasonably optimized for fast performance while still
being easy to read.
These models are used as end-to-end tests, ensuring that the models run
with the same or improved speed and performance with each new TensorFlow build.

## More models to come!

The team is actively developing new models.
In the near future, we will add:

* State-of-the-art language understanding models.
* State-of-the-art image classification models.
* State-of-the-art object detection and instance segmentation models.
* State-of-the-art video classification models.

## Table of Contents

- [Models and Implementations](#models-and-implementations)
  * [Computer Vision](#computer-vision)
    + [Image Classification](#image-classification)
    + [Object Detection and Segmentation](#object-detection-and-segmentation)
    + [Video Classification](#video-classification)
  * [Natural Language Processing](#natural-language-processing)
  * [Recommendation](#recommendation)
- [How to get started with the official models](#how-to-get-started-with-the-official-models)
- [Contributions](#contributions)

## Models and Implementations

### Computer Vision

#### Image Classification

| Model | Reference (Paper) |
|-------|-------------------|
| [MNIST](legacy/image_classification) | A basic model to classify digits from the [MNIST dataset](http://yann.lecun.com/exdb/mnist/) |
| [ResNet](vision/MODEL_GARDEN.md) | [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385) |
| [ResNet-RS](vision/MODEL_GARDEN.md) | [Revisiting ResNets: Improved Training and Scaling Strategies](https://arxiv.org/abs/2103.07579) |
| [EfficientNet](legacy/image_classification) | [EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks](https://arxiv.org/abs/1905.11946) |
| [Vision Transformer](vision/MODEL_GARDEN.md) | [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929) |

#### Object Detection and Segmentation

| Model | Reference (Paper) |
|-------|-------------------|
| [RetinaNet](vision/MODEL_GARDEN.md) | [Focal Loss for Dense Object Detection](https://arxiv.org/abs/1708.02002) |
| [Mask R-CNN](vision/MODEL_GARDEN.md) | [Mask R-CNN](https://arxiv.org/abs/1703.06870) |
| [ShapeMask](legacy/detection) | [ShapeMask: Learning to Segment Novel Objects by Refining Shape Priors](https://arxiv.org/abs/1904.03239) |
| [SpineNet](vision/MODEL_GARDEN.md) | [SpineNet: Learning Scale-Permuted Backbone for Recognition and Localization](https://arxiv.org/abs/1912.05027) |
| [Cascade RCNN-RS and RetinaNet-RS](vision/MODEL_GARDEN.md) | [Simple Training Strategies and Model Scaling for Object Detection](https://arxiv.org/abs/2107.00057)|

#### Video Classification

| Model | Reference (Paper) |
|-------|-------------------|
| [Mobile Video Networks (MoViNets)](projects/movinet) | [MoViNets: Mobile Video Networks for Efficient Video Recognition](https://arxiv.org/abs/2103.11511) |

### Natural Language Processing

| Model | Reference (Paper) |
|-------|-------------------|
| [ALBERT (A Lite BERT)](nlp/MODEL_GARDEN.md#available-model-configs) | [ALBERT: A Lite BERT for Self-supervised Learning of Language Representations](https://arxiv.org/abs/1909.11942) |
| [BERT (Bidirectional Encoder Representations from Transformers)](nlp/MODEL_GARDEN.md#available-model-configs) | [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805) |
| [NHNet (News Headline generation model)](projects/nhnet) | [Generating Representative Headlines for News Stories](https://arxiv.org/abs/2001.09386) |
| [Transformer](nlp/MODEL_GARDEN.md#available-model-configs) | [Attention Is All You Need](https://arxiv.org/abs/1706.03762) |
| [XLNet](nlp/xlnet) | [XLNet: Generalized Autoregressive Pretraining for Language Understanding](https://arxiv.org/abs/1906.08237) |
| [MobileBERT](projects/mobilebert) | [MobileBERT: a Compact Task-Agnostic BERT for Resource-Limited Devices](https://arxiv.org/abs/2004.02984) |

### Recommendation

Model                            | Reference (Paper)
-------------------------------- | -----------------
[DLRM](recommendation/ranking)   | [Deep Learning Recommendation Model for Personalization and Recommendation Systems](https://arxiv.org/abs/1906.00091)
[DCN v2](recommendation/ranking) | [Improved Deep & Cross Network and Practical Lessons for Web-scale Learning to Rank Systems](https://arxiv.org/abs/2008.13535)
[NCF](recommendation)            | [Neural Collaborative Filtering](https://arxiv.org/abs/1708.05031)

## How to get started with the official models

* The models in the master branch are developed using TensorFlow 2,
and they target the TensorFlow [nightly binaries](https://github.com/tensorflow/tensorflow#installation)
built from the
[master branch of TensorFlow](https://github.com/tensorflow/tensorflow/tree/master).
* The stable versions targeting releases of TensorFlow are available
as tagged branches or [downloadable releases](https://github.com/tensorflow/models/releases).
* Model repository version numbers match the target TensorFlow release,
such that
[TensorFlow-models v2.5.0](https://github.com/tensorflow/models/releases/tag/v2.5.0)
is compatible with
[TensorFlow v2.5.0](https://github.com/tensorflow/tensorflow/releases/tag/v2.5.0).

Please follow the below steps before running models in this repository.

### Requirements

* The latest TensorFlow Model Garden release and the latest TensorFlow 2
  * If you are on a version of TensorFlow earlier than 2.2, please
upgrade your TensorFlow to [the latest TensorFlow 2](https://www.tensorflow.org/install/).

```shell
pip3 install tf-nightly
# pip3 install tensorflow # for latest stable version
```

* Python 3.7+

Our integration tests run with Python 3.7. Although Python 3.6 should work, we
don't recommend earlier versions.

### Installation

Please check the installation instructions [here](https://github.com/tensorflow/models#Installation)

## Contributions

If you want to contribute, please review the [contribution guidelines](https://github.com/tensorflow/models/wiki/How-to-contribute).
