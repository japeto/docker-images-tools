FROM gcc:12.4.0-bookworm

ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

#### ADD DEFAULT USER ####
ARG USER=japeto
ENV USER ${USER}
RUN adduser --disabled-password ${USER}

ENV USER_HOME /home/${USER}
RUN chown -R ${USER}:${USER} ${USER_HOME}

# Install vim and nano
RUN apt-get update && apt-get install -y vim nano git\
    && apt-get --yes -qq clean \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /home/${USER}

USER ${USER}
CMD ["/bin/bash"]