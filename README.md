# Multiple-Version-of-CUDA-On-The-Same-Machine
## Install CUDA
Since .deb file might override your current CUDA driver, I recommend installing it with runfile at [NVIDIA Official Website](https://developer.nvidia.com/cuda-toolkit-archive)
After downloading CUDA runfile, run 
```bash
sudo sh cuda_10.0.130_410.48_linux.run --silent --toolkit --override
```
where `--silent` means do everything without any interactive prompt and `--override` means set the cuda to default.

You may set any version of cuda to default by
```bash
sudo ln -nsf /usr/local/cuda-10.0 /usr/local/cuda
```

## Install CuDNN
Download cuDNN .tgz file at [CUDNN](https://developer.nvidia.com/rdp/cudnn-archive) 
then
```bash
tar -xzvf cudnn-10.0-linux-x64-v7.6.4.38.tgz
sudo cp cuda/include/cudnn.h /usr/local/cuda/include
sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64
sudo chmod a+r /usr/local/cuda/include/cudnn.h /usr/local/cuda/lib64/libcudnn*
```
## Export LD_LIBRARY_PATH
Add all CUDA library paths to `$LD_LIBRARY_PATH`
```bash
export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64:/usr/local/cuda-10.0/lib64
```
That's it!
