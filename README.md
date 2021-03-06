# SmallNetworkPlusPlus
A small network in keras with additional technics.

## Table of contents
* [Topology](#Topoloty)
* [Technologies added](#technologies-added)
* [Possible improvements](#possible-improvements)

## Topology
This project is simple network low on parameters (18,211)
``` python
Input((100,100,1))
MaxPooling2D(pool_size=(2,2))

Conv2D (16, kernel_size=(3,3), strides=1, padding='same')
ReLU()
Conv2D (16, kernel_size=(3,3), strides=1, padding='same')
ReLU()
AveragePooling2D(pool_size=(2, 2))

Conv2D (24, kernel_size=(3,3), strides=1, padding='same')
ReLU()
Conv2D (24, kernel_size=(3,3), strides=1, padding='same')
ReLU()
AveragePooling2D(pool_size=(2, 2))

Conv2D (32, kernel_size=(3,3), strides=1, padding='same')
GlobalAveragePooling2D()
Flatten()
Dense(3)
Softmax()
```

## Technologies added
Project is created with additional technics:
* Weight decay
* SGD with momentum
* Gradnorm = 1.0
* Small batchsize 16, 32
