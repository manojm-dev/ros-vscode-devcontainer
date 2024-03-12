FROM ros:humble

CMD [ "/bin/bash","-c" ]

ENV ROS_DISTRO=humble
ENV SHELL /bin/bash

RUN apt update && apt upgrade -y && apt install -y \
    python3-pip \
    python3-colcon-common-extensions

RUN apt install -y \
    ros-humble-rosbridge-server

RUN mkdir -p /root/ws/src

RUN echo "#ros" >> /root/.bashrc && \
    echo "source /opt/ros/$ROS_DISTRO/setup.bash" >> /root/.bashrc && \
    echo "#colcon autocomplete" >> /root/.bashrc && \
    echo "source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash" >> /root/.bashrc
