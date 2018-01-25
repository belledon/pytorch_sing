BootStrap: docker
From: nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04



%post
    # Set up some required environment defaults

    apt-get -y update && apt-get -y install git \
                                            cmake \
                                            python3 \
                                            python3-pip
    pip3 install numpy pyyaml mkl setuptools cmake cffi

    mkdir /repo-src && cd /repo-src
    git clone --recursive https://github.com/pytorch/pytorch
    cd pytorch
    python3 setup.py install

    apt-get clean
