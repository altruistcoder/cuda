
FROM cuda:10.0-devel-ubi7
LABEL maintainer "NVIDIA CORPORATION <sw-cuda-installer@nvidia.com>"

ENV CUDNN_VERSION 7.4.2.24
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

RUN yum install -y \
    libcudnn7-devel-${CUDNN_VERSION}-1.cuda10.0 \
    && yum clean all \
    && rm -rf /var/cache/yum/*
