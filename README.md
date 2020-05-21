# Multiple-Version-of-CUDA-On-The-Same-Machine
1. Install all versions of CUDA you want
```bash
Do you accept the previously read EULA?
accept/decline/quit: accept

You are attempting to install on an unsupported configuration. Do you wish to continue?
(y)es/(n)o [ default is no ]: y

Install NVIDIA Accelerated Graphics Driver for Linux-x86_64 410.48?
(y)es/(n)o/(q)uit: n

Install the CUDA 10.0 Toolkit?
(y)es/(n)o/(q)uit: y

Enter Toolkit Location
 [ default is /usr/local/cuda-10.0 ]:

Do you want to install a symbolic link at /usr/local/cuda?
(y)es/(n)o/(q)uit: n

Install the CUDA 10.0 Samples?
(y)es/(n)o/(q)uit: n
```
2. Link the default version of CUDA you want to `cuda` in /usr/local/
3. Add all library directories to $LD_LIBRARY_PATH e.g.
```bash
export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64:/usr/local/cuda-9.0/lib64
```
That's it!
