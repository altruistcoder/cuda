
FROM ${IMAGE_NAME}:9.2-runtime-centos7
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

ENV CUDNN_VERSION 7.6.0.64
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

# cuDNN license: https://developer.nvidia.com/cudnn/license_agreement
RUN CUDNN_DOWNLOAD_SUM=ff028e6f07349445c16fef704a90bccb0992c3e012bba66ab1da352bad55b304 && \
    curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v7.6.0/cudnn-9.2-linux-x64-v7.6.0.64.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-9.2-linux-x64-v7.6.0.64.tgz" | sha256sum -c - && \
    tar --no-same-owner -xzf cudnn-9.2-linux-x64-v7.6.0.64.tgz -C /usr/local --wildcards 'cuda/lib64/libcudnn.so.*' && \
    rm cudnn-9.2-linux-x64-v7.6.0.64.tgz && \
    ldconfig
