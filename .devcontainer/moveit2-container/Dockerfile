FROM moveit/moveit2:main-humble-tutorial-source

RUN ["/bin/bash", "-c"]

ENV SHELL /bin/bash

# Install basics
RUN apt-get update && apt-get upgrade && \
    apt-get install \
    sudo \
    nano \
    git \
    python3-pip

# Creating workspace
RUN mkdir -p /root/ws/src

# Sourceing
RUN echo "#ros" >> /root/.bashrc && \
    echo "source /opt/ros/humble/setup.bash" >> /root/.bashrc && \
    echo "#colcon autocomplete" >> /root/.bashrc && \
    echo "source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash" >> /root/.bashrc && \
    echo "#moveit" >> /root/.bashrc && \
    echo "source /root/ws_moveit/install/setup.bash" >> /root/.bashrc && \
    echo "#workspace" >> /root/.bashrc && \
    echo "source /root/ws/install/setup.bash" >> /root/.bashrc
