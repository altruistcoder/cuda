
FROM cuda:11.1-base-ubuntu16.04

LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

ENV NCCL_VERSION 2.7.8

RUN apt-get update && apt-get install -y --no-install-recommends \
    cuda-libraries-11-1=11.1.0-1 \
    libnpp-11-1=11.1.1.269-1 \
    cuda-nvtx-11-1=11.1.74-1 \
    libcublas-11-1=11.2.1.74-1 \
    libnccl2=$NCCL_VERSION-1+cuda11.1 \
    && apt-mark hold libnccl2 \
    && rm -rf /var/lib/apt/lists/*

