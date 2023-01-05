FROM continuumio/conda-ci-linux-64-python3.8

USER root

# Install sudo
RUN apt-get update && \
    apt-get install -y sudo apt-utils


# make root path
RUN mkdir /home/onepose
# setup work directory
WORKDIR /home/onepose

# install conda config
COPY ./requirements.txt /home/onepose/requirements.txt
COPY ./environment.yaml /home/onepose/environment.yaml
RUN conda env create -f environment.yaml
RUN conda activate onepose

