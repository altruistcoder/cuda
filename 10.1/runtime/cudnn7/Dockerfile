
FROM ${IMAGE_NAME}:10.1-runtime-centos6
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

ENV CUDNN_VERSION 7.6.0.64
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

# cuDNN license: https://developer.nvidia.com/cudnn/license_agreement
RUN CUDNN_DOWNLOAD_SUM=e956c6f9222fcb867a10449cfc76dee5cfd7c7531021d95fe9586d7e043b57d7 && \
    curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v7.6.0/cudnn-10.1-linux-x64-v7.6.0.64.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-10.1-linux-x64-v7.6.0.64.tgz" | sha256sum -c - && \
    tar --no-same-owner -xzf cudnn-10.1-linux-x64-v7.6.0.64.tgz -C /usr/local --wildcards 'cuda/lib64/libcudnn.so.*' && \
    rm cudnn-10.1-linux-x64-v7.6.0.64.tgz && \
    ldconfig
