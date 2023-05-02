# debian dockerfile for easybuild testing
FROM debian

# create dummy user
RUN apt-get update
RUN apt-get install sudo 
RUN useradd --home-dir /home/myuser --create-home --user-group --shell /bin/sh -p password myuser 
RUN addgroup wheel
RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
RUN usermod -aG wheel myuser
USER myuser

# installing required packages
RUN sudo apt-get install --yes lmod \\
                               pip \\
                               vim \\
                               libssl-dev \\
                               git \\
                               binutils \\
                               file \\
                               unzip
RUN pip install easybuild

# adding paths to easybuild, lmod, & file executables
# note, lmod version number is hardcoded in its path, may need to adjust
RUN export PATH=$PATH:/home/myuser/.local/bin:/usr/share/lmod/6.6/libexec/:/usr/lib/apt/methods