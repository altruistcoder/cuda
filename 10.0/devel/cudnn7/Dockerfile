
FROM ${IMAGE_NAME}:10.0-devel-centos7
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

ENV CUDNN_VERSION 7.6.0.64
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

# cuDNN license: https://developer.nvidia.com/cudnn/license_agreement
RUN CUDNN_DOWNLOAD_SUM=c4e1ee4168f4cadabaa989487a47bed09f34d34e35398b6084a2699d11bd2560 && \
    curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v7.6.0/cudnn-10.0-linux-x64-v7.6.0.64.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-10.0-linux-x64-v7.6.0.64.tgz" | sha256sum -c - && \
    tar --no-same-owner -xzf cudnn-10.0-linux-x64-v7.6.0.64.tgz -C /usr/local && \
    rm cudnn-10.0-linux-x64-v7.6.0.64.tgz && \
    ldconfig
