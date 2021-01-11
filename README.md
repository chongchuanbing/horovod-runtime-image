# horovod-runtime-image

### GPU
#### build
```
docker build --build-arg REGISTRY=docker.io/chongchuanbing \
             --build-arg HOROVOD_VERSION=0.19.0 \
             --build-arg CUDA_VERSION=10.0 \
             --build-arg CUDNN_VERSION=7 \
             --build-arg PYTHON_VERSION=3.6 \
             --build-arg UBUNTU_VERSION=18.04 \
             -t horovod-mpi-runtime:0.19.0-cuda10.0-cudnn7-mpi4.0-py3.6-ubuntu18.04 \
             -f Dockerfile.gpu .
```
#### image
```
docker pull docker.io/chongchuanbing/horovod-mpi-runtime:0.19.0-cuda10.0-cudnn7-mpi4.0-py3.6-ubuntu18.04
```

### CPU
#### build
```
docker build --build-arg HOROVOD_VERSION=0.19.0 \
             --build-arg PYTHON_VERSION=3.6 \
             --build-arg UBUNTU_VERSION=18.04 \
             -t horovod-mpi-runtime:0.19.0-mpi4.0-py3.6-ubuntu18.04 \
             -f Dockerfile.cpu .
```
#### image
```
docker pull docker.io/chongchuanbing/horovod-mpi-runtime:0.19.0-mpi4.0-py3.6-ubuntu18.04
```