# Image Classification with Jetson Inference

This Python script performs image classification using NVIDIA Jetson devices and the `jetson-inference` library. It loads an image, processes it with a specified neural network, and outputs the predicted class and confidence.

## 📦 Requirements

* NVIDIA Jetson device (e.g., Jetson Nano, Xavier)
* [jetson-inference](https://github.com/dusty-nv/jetson-inference) installed and configured
* Python 3
* ONNX model and label file (e.g., `resnet18.onnx`, `dataset/labels.txt`)

## 📄 Script Overview

classify.py

This script:

1. Loads an image file.
2. Runs image classification using a selected network (default: `resnet-18`).
3. Prints the classification result and confidence score.

## 🔧 Usage

python3 classify.py <image_filename> [--network <model_name>]

### Example

python3 classify.py dog.jpg --network resnet-18


### Arguments

| Argument    | Type | Description                                                                            |
| ----------- | ---- | -------------------------------------------------------------------------------------- |
| `filename`  | str  | Path to the image file you want to classify                                            |
| `--network` | str  | (Optional) Network to use, such as `googlenet`, `resnet-18`, etc. Default: `resnet-18` |

> 🔎 Check `--help` for additional supported models.

## 📁 Model and Labels

The script explicitly uses:

* `resnet18.onnx` as the ONNX model file
* `dataset/labels.txt` as the label file

Make sure these files are accessible from the script's working directory or adjust the paths accordingly.

## 🖼️ Output

The script prints the result in the following format:


image is recognized as <class_description> (class #<class_index>) with <confidence>% confidence


## 🔍 Example Output

image is recognized as golden retriever (class #207) with 89.23% confidence

## 📌 Notes

* Ensure the ONNX model and label files match the network architecture used.
* You can retrain or convert your own models compatible with Jetson using TensorRT tools.

## 📚 Resources

* [Jetson Inference Docs](https://github.com/dusty-nv/jetson-inference/blob/master/docs/imagenet-example.md)
* [NVIDIA Jetson Download Center](https://developer.nvidia.com/embedded/downloads)



