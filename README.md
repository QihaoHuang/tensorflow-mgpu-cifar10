# tensorflow-mgpu-cifar10

## tensorflow env

```
# tensorflow 1.14
import tensorflow as tf
os.environ["CUDA_DEVICE_ORDER"]="PCI_BUS_ID"
os.environ["CUDA_VISIBLE_DEVICES"]="0"

from tensorflow.python.client import device_lib
print(device_lib.list_local_devices())

tf.test.is_gpu_available()
tf.test.gpu_device_name()
```

## running
```shell
git clone git@github.com:qihao96/tensorflow-mgpu-cifar10.git
cd tensorflow-mgpu-cifar10

export CUDA_VISIBLE_DEVICES=0,1
pip install tensorflow_datasets
pip install tensorflow-metadata

python cifar10_multi_gpu_train.py --num_gpus 2
```
