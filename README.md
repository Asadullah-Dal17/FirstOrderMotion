# FirstOrderMotion
## Nvidia Drivers Installation For Ubuntu 20.04 and Windows 10

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

## if want to install cuda

then go to this link: https://www.tensorflow.org/install/gpu
 
# Download Anaconda 

https://www.anaconda.com/products/individual

## how to create Environment using conda

conda create --name FOMM python==3.7
## Activate Environment

conda activate FOMM

## Repository of First order motion

git clone https://github.com/AliaksandrSiarohin/first-order-model

## Installation of packages

conda install numpy==1.15

conda install --file filename.txt

## pytorch installation command for Anaconda

conda install pytorch torchvision cudatoolkit=10.1 -c pytorch

https://pytorch.org/

## Setup Face-Alignment

git clone https://github.com/1adrianb/face-alignment

cd face-alignment

pip install -r requirements.txt

python setup.py install

## ffmpeg installation 

sudo apt install ffmpeg

pip install ffmpeg

# input image must have size of 256x256
in case you want increase the size than crop video(Driving Video) must have same size as input image(Source Image)

## command for croping the video

python crop-video.py --inp some_youtube_video.mp4

when croping will be completed, it generate a command in the terminal in oder to crop the video copy and paste that command and crop.mp4 will save into First order motion directory

by defualt it crops video in 256x256 size

## already crop video and picture are available on this google drive link:
https://drive.google.com/drive/folders/1kZ1gCnpfU0BnpdU47pLM_TQ6RypDDqgw?usp=sharing

## Google drive link of pre-trained model of first order motion model

https://drive.google.com/drive/folders/1PyQJmkdCsAkOYwUyaj_l-l0as-iLDgeH
## Command to generate animated video

python demo.py  --config config/dataset_name.yaml --driving_video path/to/driving --source_image path/to/source --checkpoint path/to/checkpoint --relative --adapt_scale

======================================================================================================
###                     The end
