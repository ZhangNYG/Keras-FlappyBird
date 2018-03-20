# Keras-FlappyBird

A single 200 lines of python code to demostrate DQN with Keras

Please read the following blog for details

https://yanpanlau.github.io/2016/07/10/FlappyBird-Keras.html

![](animation1.gif)

# Installation Dependencies:

* Python 2.7
* Keras 1.0 
* pygame
* scikit-image

# How to Run?

**CPU only**

```
git clone https://github.com/yanpanlau/Keras-FlappyBird.git
cd Keras-FlappyBird
python qlearn.py -m "Run"
```

**GPU version (Theano)**

```
git clone https://github.com/yanpanlau/Keras-FlappyBird.git
cd Keras-FlappyBird
THEANO_FLAGS=device=gpu,floatX=float32,lib.cnmem=0.2 python qlearn.py -m "Run"
```

If you want to train the network from beginning, delete the model.h5 and run qlearn.py -m "Train"

# model

We finish building the model
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 20, 20, 32)        8224      
_________________________________________________________________
activation_1 (Activation)    (None, 20, 20, 32)        0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 10, 10, 64)        32832     
_________________________________________________________________
activation_2 (Activation)    (None, 10, 10, 64)        0         
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 10, 10, 64)        36928     
_________________________________________________________________
activation_3 (Activation)    (None, 10, 10, 64)        0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 6400)              0         
_________________________________________________________________
dense_1 (Dense)              (None, 512)               3277312   
_________________________________________________________________
activation_4 (Activation)    (None, 512)               0         
_________________________________________________________________
dense_2 (Dense)              (None, 2)                 1026      
=================================================================
Total params: 3,356,322
Trainable params: 3,356,322
Non-trainable params: 0
_________________________________________________________________
None