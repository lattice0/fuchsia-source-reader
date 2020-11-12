FROM ubuntu:focal

RUN apt-get update -o Acquire::Retries=30 \ 
&& DEBIAN_FRONTEND=noninteractive apt-get install -o Acquire::Retries=30 -y --no-install-recommends \
clang gcc build-essential wget git python unzip ca-certificates

WORKDIR /home/project

RUN mkdir fuchsia && cd fuchsia && wget https://fuchsia.googlesource.com/fuchsia/+archive/master.tar.gz && tar -xvzf master.tar.gz