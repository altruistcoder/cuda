
FROM ${IMAGE_NAME}:10.1-base-centos6
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

RUN yum install -y \
        cuda-libraries-$CUDA_PKG_VERSION \
        cuda-nvtx-$CUDA_PKG_VERSION && \
    rm -rf /var/cache/yum/*
