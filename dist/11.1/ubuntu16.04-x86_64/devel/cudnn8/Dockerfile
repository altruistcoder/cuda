
FROM cuda:11.1-devel-ubuntu16.04
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

ENV CUDNN_VERSION 8.0.4.30

LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

RUN apt-get update && apt-get install -y --no-install-recommends \
    libcudnn8=$CUDNN_VERSION-1+cuda11.1 \
    libcudnn8-dev=$CUDNN_VERSION-1+cuda11.1 \
    && apt-mark hold libcudnn8 && \
    rm -rf /var/lib/apt/lists/*
