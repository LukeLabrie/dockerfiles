# manjarolinux docker container for testing easybuild runs
FROM manjarolinux/base

# install dependencies for openmc pkgbuild files 
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
                                 yay                       

#RUN useradd --home-dir /home/myuser --create-home --user-group --shell /bin/sh myuser && passwd myuser AlvinWeinberg
#USER myuser

# RUN yay -Ssy
# RUN yay -S --noconfirm 	gmsh \
#                       python-pyparsing \
#	                    python-cadquery \
 #                       python-numpy \
  #                      ocp \
   #                     python-meshio \
    #                    python-trimesh \
     #                   python-networkx \
      #                  cython \
       #                 python-pytest \
        #                mmg     


