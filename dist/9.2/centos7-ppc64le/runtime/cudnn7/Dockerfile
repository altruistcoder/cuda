
FROM cuda:9.2-runtime-centos7
LABEL maintainer "NVIDIA CORPORATION <sw-cuda-installer@nvidia.com>"

ENV CUDNN_VERSION 7.6.5.32
LABEL com.nvidia.cudnn.version="${CUDNN_VERSION}"

# cuDNN license: https://developer.nvidia.com/cudnn/license_agreement
RUN CUDNN_DOWNLOAD_SUM=a11f44f9a827b7e69f527a9d260f1637694ff7c1674a3e46bd9ec054a08f9a76 && \
    curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v7.6.5/cudnn-9.2-linux-ppc64le-v7.6.5.32.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-9.2-linux-ppc64le-v7.6.5.32.tgz" | sha256sum -c - && \
    tar --no-same-owner -xzf cudnn-9.2-linux-ppc64le-v7.6.5.32.tgz -C /usr/local --wildcards 'cuda/targets/ppc64le-linux/lib/libcudnn.so.*' && \
    rm cudnn-9.2-linux-ppc64le-v7.6.5.32.tgz && \
    ldconfig
