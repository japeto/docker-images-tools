FROM ubuntu:18.04

ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

#### ADD DEFAULT USER ####
ARG USER=japeto
ENV USER ${USER}
RUN adduser --disabled-password ${USER}

ENV USER_HOME /home/${USER}
RUN chown -R ${USER}:${USER} ${USER_HOME}

WORKDIR /home/${USER}

RUN apt-get --yes -qq update \
 && apt-get --yes -qq upgrade \
 && apt-get --yes -qq install \
                      bzip2 \
                      cmake \
                      cpio \
                      curl \
                      g++ \
                      gcc \
                      gfortran \
                      git \
                      gosu \
                      libblas-dev \
                      liblapack-dev \
                      libomp-dev \
                      libopenmpi-dev \
                      openmpi-bin \
                      python3-dev \
                      python3-pip \
                      virtualenv \
                      wget \
                      zlib1g-dev \
                      vim       \
                      htop      \
 && apt-get --yes -qq clean \
 && rm -rf /var/lib/apt/lists/*

USER ${USER}
CMD [ "/bin/bash" ]
