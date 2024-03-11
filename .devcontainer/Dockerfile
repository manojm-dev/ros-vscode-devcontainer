FROM moveit/moveit2:main-humble-tutorial-source

CMD [ "/bin/bash","-c" ]

ENV ROS_DISTRO=humble
ENV SHELL /bin/bash

RUN mkdir -p /root/ws/src

RUN echo "#ros" >> /root/.bashrc && \
    echo "source /opt/ros/$ROS_DISTRO/setup.bash" >> /root/.bashrc && \
    echo "#colcon autocomplete" >> /root/.bashrc && \
    echo "source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash" >> /root/.bashrc && \
    echo "#workspace" >> /root/.bashrc && \
    echo "source /root/ws_moveit/install/setup.bash" >> /root/.bashrc