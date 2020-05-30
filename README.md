# FirstOrderMotion
## Nvidia Drivers Installation commands For Ubuntu

### Add NVIDIA package repositories

wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.1.243-1_amd64.deb

sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub

sudo dpkg -i cuda-repo-ubuntu1804_10.1.243-1_amd64.deb

sudo apt-get update

wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb

sudo apt install ./nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb

sudo apt-get update

### Install NVIDIA driver

sudo apt-get install --no-install-recommends nvidia-driver-440

### Reboot. Check that GPUs are visible using the command:

nvidia-smi

it will show the detail of your GPU 
 
## Repository of First order motion

git clone https://github.com/AliaksandrSiarohin/first-order-model

## pytorch installation command for Anaconda

conda install pytorch torchvision cudatoolkit=10.1 -c pytorch

https://pytorch.org/


### pip command for Opencv

pip install opencv-python

