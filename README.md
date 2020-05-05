# Multiple-Version-of-CUDA-On-The-Same-Machine
1. Install all versions of CUDA you want
2. Link the default version of CUDA you want to `cuda` in /usr/local/
3. Add all library directories to $LD_LIBRARY_PATH e.g.
```bash
export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64:/usr/local/cuda-9.0/lib64
```
That's it!
