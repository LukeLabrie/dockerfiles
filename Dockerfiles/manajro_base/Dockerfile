# manjarolinux docker container for testing easybuild runs
FROM manjarolinux/base

# install osdependencies 
RUN sudo pacman -Syu --noconfirm openssl \
                                 rdma-core \
                                 pam \
                                 base-devel \
                                 python-numpy \
                                 

RUN useradd --home-dir /home/myuser --create-home --user-group --shell /bin/sh myuser 
USER myuser
