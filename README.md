![maintenance-status](https://img.shields.io/badge/maintenance-deprecated-red.svg)

# JointTransformationPytorch 🔦
Generalize Pytorch transforms to an arbitrary number of channels by replacing PIL Images with Numpy Arrays and OpenCV (i.e., rewrite part of the pytorch library with numpy).

--------------

# Nota Bene 🗒️

This is mostly for experimental purpose. Wiser alternatives may be created based on transforms lambda and the functional interface from Pytorch. These alternatives should be easier to setup and probably easier to understand (higher level, simple verbosity). 

Check [this link](https://discuss.pytorch.org/t/transforms-compose-and-transforms-lambda-are-just-empty-wrapper/3635). 


In a nutshell:
For random operations with lambda transforms / custom transforms, 

1. generate a random number (e.g. ```import random \ nb = random.random()``` ), 
2. generate transform parameters (e.g., for random crop, generate the bounding box coordinates randomly, once)
3. apply a not random transform on each image /channel you would like to process passing the transform parameters as argument (e.g., the coordinates that you generated randomly)
