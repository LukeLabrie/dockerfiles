# manjarolinux docker container for testing aur runs
FROM manjarolinux/base

# install dependencies for openmc pkgbuild files 
RUN sudo pacman -Ssy
RUN sudo pacman -Syu --noconfirm openssl \
                                 rdma-core \
                                 pam \
                                 base-devel \
                                 python-numpy \
                                 blas \
                                 lapack \
                                 eigen \
                                 netcdf \
                                 hdf5 \
                                 git \
                                 python \
                                 cmake \
                                 binutils \
                                 make \
                                 gcc-fortran \
                                 python-setuptools \
                                 yay \
                                 python-pip \
                                 libx11 \
                                 libgl \
                                 ipython \
                                 man \
                                 python-lxml \
                                 python-scipy \
                                 python-pandas \
                                 python-matplotlib \
                                 python-uncertainties \
                                 embree \
                                 libxrender \
                                 libxcursor \
                                 libxft \
                                 libxinerama \
                                 freecad \
                                 glu \
                                 openssh \
                                 vim


RUN useradd --home-dir /home/myuser --create-home --user-group --shell /bin/sh -p password myuser 
RUN usermod -aG wheel myuser
RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
USER myuser

RUN pip install pytest docutils
RUN export PATH=/home/myuser/.local/bin:$PATH



