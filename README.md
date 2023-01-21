# Prebuilt wheels for PyTorch 2.0 for Cuda 11.8

# UPDATE:

Pytorch has official cuda 11.8 build now: https://download.pytorch.org/whl/nightly/cu118

# DOWNLOADS CAN BE FOUND IN RELEASES -->

**Why?**

Because it makes RTX 4090 do inference significantly faster

### Information on the system it was built for

This was done on a fresh installation of Ubuntu 22.04.1 LTS

Nvidia drivers installed through apt from Nvidia's repo (`cuda-11-8`)

```
# lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 22.04.1 LTS
Release:        22.04
Codename:       jammy

# nvidia-smi
Wed Jan 18 10:42:08 2023
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 525.60.13    Driver Version: 525.60.13    CUDA Version: 12.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA GeForce ...  On   | 00000000:2D:00.0 Off |                  Off |
|  0%   35C    P8     7W / 450W |     0 MiB / 24564MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+

# nvcc --version
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2022 NVIDIA Corporation
Built on Wed_Sep_21_10:33:58_PDT_2022
Cuda compilation tools, release 11.8, V11.8.89
Build cuda_11.8.r11.8/compiler.31833905_0

# date
Wed Jan 18 10:43:06 AM UTC 2023

# python --version
Python 3.10.6

# uname -a
Linux sd 5.15.0-58-generic #64-Ubuntu SMP Thu Jan 5 11:43:13 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux

# update-alternatives --display cuda
cuda - auto mode
  link best version is /usr/local/cuda-11.8
  link currently points to /usr/local/cuda-11.8
  link cuda is /usr/local/cuda
/usr/local/cuda-11.8 - priority 118

# echo $PATH
/usr/local/cuda-11.8/bin:/mnt/tank/venv/bin:/usr/local/cuda-11.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin

# echo $LD_LIBRARY_PATH
/usr/local/cuda-11.8/lib64:/usr/local/cuda-11.8/lib64:
```

