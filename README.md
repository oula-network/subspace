# Subspace farmer

## Download
https://github.com/oula-network/subspace/releases

## Reference Platform
- Ubuntu 22.04
- NVIDIA GPU

## Running
```sh
# set CUDA_VISIBLE_DEVICES = "x" before running a subspace-farmer to designate a single GPU to a subspace-farmer.
export CUDA_VISIBLE_DEVICES=0 GPU_CONCURRENCY=15

./subspace-farmer farm --reward-address <YOUR_ADDRESS> --node-rpc-url <YOUR_NODE> --record-encoding-concurrency=32 path=/data01,size=7T path=/data02,size=7T
```

## Notes
If you have more paths to configure, you need to increase the values of `GPU_CONCURRENCY` and `--record-encoding-concurrency` accordingly.
The higher the value of `GPU_CONCURRENCY`, the more GPU memory is required.
