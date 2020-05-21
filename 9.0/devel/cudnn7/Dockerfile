
FROM ${IMAGE_NAME}:9.0-devel-centos6
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

ENV CUDNN_VERSION 7.6.0.64
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

# cuDNN license: https://developer.nvidia.com/cudnn/license_agreement
RUN CUDNN_DOWNLOAD_SUM=90659ea77734b7b671afe930c9898d21a13b888998f1dd3940cc57d6b2f29b86 && \
    curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v7.6.0/cudnn-9.0-linux-x64-v7.6.0.64.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-9.0-linux-x64-v7.6.0.64.tgz" | sha256sum -c - && \
    tar --no-same-owner -xzf cudnn-9.0-linux-x64-v7.6.0.64.tgz -C /usr/local && \
    rm cudnn-9.0-linux-x64-v7.6.0.64.tgz && \
    ldconfig
