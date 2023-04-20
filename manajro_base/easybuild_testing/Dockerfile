# manjarolinux docker container for testing easybuild runs

# NOTE: You may need to build and/or run with `--ulimit nofile=1024:10240` in order to avoid hanging on fakeroot 

FROM manjarolinux/base

# install osdependencies 
RUN sudo pacman -Syu --noconfirm openssl \
                                 rdma-core \
                                 pam \
                                 base-devel \
                                 python-pip \
                                 git \
                                 yay \
                                 wget \
                                 tcl \
                                 lua

RUN useradd --home-dir /home/myuser --create-home --user-group --shell /bin/sh -p password myuser 
RUN usermod -aG wheel myuser
RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
USER myuser

RUN pip install easybuild
RUN export PATH=$PATH:/home/myuser/.local/bin:/usr/share