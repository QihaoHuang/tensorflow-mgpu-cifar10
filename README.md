# tensorflow-mgpu-cifar10

```shell
git clone git@github.com:qihao96/tensorflow-mgpu-cifar10.git
cd tensorflow-mgpu-cifar10

export CUDA_VISIBLE_DEVICES=0,1
python cifar10_multi_gpu_train.py --num_gpus 2
```
