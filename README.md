# fblualib-docker
Dockerfile for a [Torch7 ](https://github.com/torch/distro) environment with [fblualib](https://github.com/facebook/fblualib) on x86_64 Ubuntu with v352.63 Nvidia drivers, CUDA 7.0 & cudnn 6.5. Includes fb.python and nltk (from pip), running on Ubuntu 14.04.

Works on my 15.10 install, comes with absolutely no warranty but maybe it's of use to someone.

```
cd fblualib-docker
docker build -t fblualib:0.1-nv352.63 .
docker run -it --rm --device /dev/nvidiactl --device /dev/nvidia-uvm --device /dev/nvidia0 fblualib:0.1-nv352.63 bash
```
