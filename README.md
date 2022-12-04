# Ubuntu DinD(Docker in Docker) Image with cudagl

## Credits

This is a fork from [cruizba/ubuntu-dind](https://github.com/cruizba/ubuntu-dind).

The only difference is that the base image is changed to `nvidia/cudagl:11.3.0-devel-ubuntu20.04`.

I built this image because I need a DinD image with CUDA support.

For more information about the original image, please refer to the original repo.

## How to use it

```
docker pull kuangyuan1/ubuntu-cudagl-dind:ubuntu-20.04
nvidia-docker run -it --gpus all --privileged kuangyuan1/ubuntu-cudagl-dind:ubuntu-20.04
```

This will run a bash with a complete docker separated from your host to build, run and push docker images.

## !! WARNING !!

The option `--privileged` is not secure. I did this image just for little experiments, don't use for production. Just for dev or testing purposes.

To do this in the GOOD AND SECURE WAY just use: https://github.com/nestybox/sysbox



