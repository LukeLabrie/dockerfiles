# manjarolinux docker container for testing aur runs

# NOTE: You may need to build and/or run with `--ulimit nofile=1024:10240` in order to avoid hanging on fakeroot 

FROM archlinux

# install dependencies for openmc pkgbuild files 
RUN pacman -Syy
RUN pacman -S --noconfirm sudo
RUN useradd --home-dir /home/myuser --create-home --user-group --shell /bin/sh -p password myuser 
RUN usermod -aG wheel myuser
RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

RUN sudo pacman -Syy
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



USER myuser
RUN export PATH=/home/myuser/.local/bin:$PATH
