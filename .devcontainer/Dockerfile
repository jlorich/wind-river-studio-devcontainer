FROM debian:bullseye

#
ENV USER=root
ENV INST_URL=https://distro.windriver.com/dist/wrstudio/wrstudio-cli-distro-cd/install-studio-cli.sh


# Prerequisites
RUN apt-get update -y && \
    apt-get install -y curl \
                       python3 \
                       python3-pip \
                       git \
                       cmake \
                       buildah

# Install CLI
RUN curl -f $INST_URL --output inst.sh
RUN bash inst.sh -u $INST_URL -y
RUN echo "complete -C studio-cli studio-cli" >> ~/.bashrc

