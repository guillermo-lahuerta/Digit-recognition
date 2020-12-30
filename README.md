# Digit recognition

## About this app

This app allows you to recognize digits (i.e., numbers from 0 to 9) manually drawn on your screen.

## LeNet-5

Convolutional Neural Networks is the standard architecture for solving tasks associated with images (e.g., image classification). Some of the well-known deep learning architectures for CNN are LeNet-5 (7 layers), GoogLeNet (22 layers), AlexNet (8 layers), VGG (16–19 layers), and ResNet (152 layers).

For this project, we use LeNet-5, which has been successfully used on the MNIST dataset to identify handwritten-digit patterns. The LeNet-5 architecture is presented in the following schema.

![screenshot](img/lenet.png)

## Data

The dataset used to train, validate and test the model, correpsond to the [MNIST](http://yann.lecun.com/exdb/mnist/) dataset.
It is composed by a training set of 60,000 examples, and a test set of 10,000 examples.
The digits have been pre-processed to be size-normalized and centered in a fixed-size image of 28x28 pixels.

![screenshot](img/mnist.png)

## Requirements

* Python 3
* Tensorflow
* Dash

## How to run this app

Clone this repository and navigate to the main folder. To do so, open your Terminal (for MacOS/Linux) or your Command Prompt (for Windows) and run the following commands:
```
git clone https://github.com/Guille1899/Digit_recognition.git
cd ./Digit_recognition/
```

I strongly suggest to create a virtual environment with Conda to manage dependencies and isolate projects. After installing [Miniconda](https://docs.conda.io/en/latest/miniconda.html), run the following commands to update the base conda packages:
```
conda update conda
conda update python
conda update --all
```

Now, we can create a new conda environment, called "*digit_recognition*", that will store all the dependencies related to this repo. This can be easily achieved by loading the "*environment.yaml*" file, which contains an environment already created with all the packages needed to run the code in this repo.

```
conda env create --file environment.yaml
```

Now, you can open the jupyter notebook locally:
```
conda activate digit_recognition
jupyter notebook
```

Finally, to run the app locally, use these commands:
```
conda activate digit_recognition
python app.py
```

## Video

!(img/video.gif)

## Notes on TensorFlow

When installing *tensorflow*, note that if you have a NVIDIA graphics card on your machine, you should consider installing *tensorflow-gpu* (instead of the regular *tensorflow-cpu*), to speed up your deep learning models.

In both cases, rather than using *pip* or *conda* to try to figure out which version of TensorFlow you need, I recommend finding the exact "*.whl*" file from [TensorFlow](https://www.tensorflow.org/install/pip#package-location)’s site.
Once you have the *url* of the corresponding TensorFlow version that you need, run the following command (substite *<whl_url>* by the exact url):
```
python -m pip install <whl_url>
```

## Resources

* [Dash](https://dash.plot.ly/)
* [TensorFlow](https://www.tensorflow.org/)
