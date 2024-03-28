FROM ros:humble

SHELL ["/bin/bash", "-c"]

ENV SHELL /bin/bash

# Install basics
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y \
    sudo \
    nano \
    git \
    python3-pip

# Sourceing
RUN echo "#ros" >> /root/.bashrc && \
    echo "source /opt/ros/humble/setup.bash" >> /root/.bashrc && \
    echo "#colcon autocomplete" >> /root/.bashrc && \
    echo "source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash" >> /root/.bashrc