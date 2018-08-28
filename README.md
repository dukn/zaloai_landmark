# Zaloai_landmark
---

## What is it?
---
This project helps people submit the simplest way for the Zalo AI landmark identification challenge.

## What does it contain?
---
- Jupyter Notebook (Anaconda 3)
- Keras 
- Tensorflow 
- Python 2 and 3
- cuDNN (gpu version)

## How to install it?
---
### On Ubuntu 
1. Open a terminal
2. Install docker 
```
$ sudo apt-get install docker.io
```
3. Clone file from repository
```
$ git clone https://github.com/dukn/zaloai_landmark.git
```
4. Build the docker
With CPU only 
```
$ cd zaloai_landmark
$ sudo docker build -t zaloai/landmark -f Dockerfile.cpu . 
```
With GPU version
- install nvidia docker in [here](https://github.com/NVIDIA/nvidia-docker)
```
$ cd zaloai_landmark
$ sudo docker build -t zaloai/landmark -f Dockerfile.gpu . 
```

## How to user it?
---
With CPU version
```
$ sudo docker -it -p 8888:8888 zaloai/landmark
```
With GPU version
```
$ sudo docker --runtime=nvidia -it -p 8888:8888 zaloai/landmark
```