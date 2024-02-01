from ubuntu:22.04

ARG CACHEBUST=0

RUN apt update &&\
    apt install -y python3-pip

RUN apt-get install -y libsuitesparse-dev

RUN pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2

# Install the Visual DNA package
RUN pip install vdna