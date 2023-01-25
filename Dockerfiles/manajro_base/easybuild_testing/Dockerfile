# manjarolinux docker container for testing easybuild runs
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

#RUN wget https://sourceforge.net/projects/lmod/files/lua-5.1.4.9.tar.bz2 && \
#    tar xf lua-X.Y.Z.tar.bz2 && \
#    cd lua-X.Y.Z && \
#    ./configure --prefix=/opt/apps/lua/X.Y.Z && \
#    make; make install && \
#    cd /opt/apps/lua; ln -s X.Y.Z lua && \
#    mkdir /usr/local/bin; ln -s /opt/apps/lua/lua/bin/lua /usr/local/bin


RUN yay -Syu spack

RUN useradd --home-dir /home/myuser --create-home --user-group --shell /bin/sh myuser 
USER myuser

# write CMD option to set up the easybuild configuration for testing
CMD ["pip install easybuild","pip uninstall easybuild-framework']