FROM ubuntu:14.04@sha256:64483f3496c1373bfd55348e88694d1c4d0c9b660dee6bfef5e12f43b9933b30
RUN apt-get update && apt-get install -y \
        csh \
        gfortran \
        build-essential
ADD charmm.tar.gz /
RUN cd charmm && tool/NewCharmmTree c40b1_gnu && cd c40b1_gnu && ./install.com gnu gfortran || cat /charmm/c40b1_gnu/build/gnu/gnu.log
