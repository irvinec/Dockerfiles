# Start with anaconda image
FROM continuumio/anaconda3

LABEL version="0.0.1"
LABEL imagename="ml-base"

WORKDIR /

# Make bash the default shell
SHELL ["/bin/bash", "-c"]

RUN conda update -y conda
RUN conda config --add channels conda-forge
RUN conda update -y pip

# Make sure the conda bin is in the path
ENV PATH /opt/conda/bin:$PATH

# install basic ML and DS tools
RUN conda install --yes --name root python=3.6 tensorflow tensorboard numpy matplotlib pandas jupyter scipy

# For Tensorboard
EXPOSE 6006
# tensorboard --logdir=<logdir>



