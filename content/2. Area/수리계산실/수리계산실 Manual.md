```toc
```

이 메뉴얼은 수리계산실 컴퓨터의 Anaconda, CUDA, cuDNN을 활용한 Pytorch 환경을 구성하기 위한 메뉴얼입니다.

  

큰 틀은 Nvidia-driver 확인 및 설치, Anaconda 환경 구축, Pytorch 설치 순입니다.

이 메뉴얼도 같은 순서대로 구성되어있습니다.

  

# 0. PC

서버 컴퓨터 2대 [^1] 를 제외하고 모든 컴퓨터의 비밀번호는

`성균관`입니다.

  

## 0-1. Ubuntu

2023년 7월 20일 기준 모든 Ubuntu 컴퓨터는 22.04.02 LTS

  

만약 사용하는 컴퓨터가 Windows 11라면 바로 Anaconda 항목으로 이동.

  

## 0-2. Terminal 사용법

Ubuntu 기반의 OS는 기본적으로 Terminal을 사용합니다.

  

Terminal 사용법

- Ctrl + Alt + T을 누르면 Terminal 창이 뜹니다.

- Terminal에서는 복사, 붙여넣기가 Ctrl + Shift + C, V다

- Terminal에서 Ctrl + C는 쓰고 있는 command를 취소합니다.

  

<hr style="border:2px solid gray">

  

# 1. Nvidia Driver

## 1-1. 그래픽카드 확인하는 방법

  

```

lspci | grep -i VGA

```

  

![lspci](..//images/lspci.png) 정상적으로 작동하는 화면

  

or

  

```

nvidia-smi

```

![nvidia-smi](../images/nvidia-smi.png)가 되면 정상적으로 작동하는 것입니다.

잘 된 사진이 뜨면 Anaconda로 이동

  

## 1-2. Driver 업데이트

 `nvidia-smi` 입력했을 때

![error](../images/nvidia-smi%20error.png)

 처럼 뜨면 2가지 해결법이 있습니다.

1. Driver만 설치[^2]

  

```

sudo add-apt-repository ppa:graphics-drivers/ppa

sudo apt-get update

sudo apt-get ubuntu-drivers devices

```

  

입력하면 아래와 같은 결과값이 나옵니다.


![[drivers update.png]]
 이때 Recommended가 쓰여있는 nvidia-driver-{버전}을 확인하고

  

```linux

sudo apt-get install nvidia-driver-VERSION

```

  

이후 `sudo reboot` 하면 Driver 설치가 완료됩니다.

  

그래도 안 되면 CUDA로 이동

  

<hr style="border:2px solid gray">

  

# 2. Anaconda

이후 편의를 위해 Anaconda는 Conda로 표기하겠습니다.

  

Terminal을 켜고

사진의 (base)가 보이면 Conda가 설치 되어있는 것입니다.

  

(base)가 보이지 않는다면 `conda env list`를 입력합니다.

1. `conda : command not found` 라는 문구가 보이면 [설치](##Conda설치)로 이동

![conda not found](../images/conda%20env%20list.png)

2. 아니라면

![conda env](../images/env%20list%20without%20test.png)

  

## 2-1. 가상환경

  

### 2-1-1. 가상환경 생성

```

conda create -n 원하는 환경이름

```

 >추가적인 parameter에 관해서는 [docs](https://docs.conda.io/projects/conda/en/latest/commands/env/create.html)참고

 >보통 원하는 python version을 parameter로 사용함

  

가상환경을 생성하고 나면

  

![env list test](../images/conda%20env%20list%20ok.png)

처럼 뜨는 것을 확인할 수 있습니다.

  

### 2-1-2. ***가상환경 활성화***

  

```

conda activate 환경이름

```

***활성화 안 하면 내가 작업하는 환경이 되지 않습니다.***

  

Pytorch로 이동

  

## 2-2. Conda설치

```

sudo apt update

sudo apt install curl -y

curl --output anaconda.sh https://repo.anaconda.com/archive/Anaconda3-2022.10-Linux-x86_64.sh

sha256sum anaconda.sh

bash anaconda.sh

```

위의 코드를 차례대로 입력한뒤 입력하는 줄이 나오면 차례대로 yes/Enter키/yes를 입력합니다.

  

```

source ~/.bashrc

```

입력하면

![source](../images/source.png)

처럼 (base)가 등장합니다.

  

<hr style="border:2px solid gray">

  

# 3. Pytorch 설치

  

***conda environment가 활성화된 상태로 한다***

```

conda install pytorch

```

를 사용하면 높은 확률로 CUDA를 사용할 수 없을 겁니다.

  

다음과 같은 방법을 이용합시다.

><https://pytorch.org/get-started/locally/>

  

에서 Linux, Conda, Python, CUDA 11.8을 선택하고 밑에 나온 `Run this command`를 복사해서 Terminal에 입력합니다.

  

대부분 이 과정에서 CUDA와 cuDNN에 필요한 Driver가 설치됩니다.

  

## 3-1.확인

  

이 메뉴얼에서는 Jupyter lab을 이용해서 확인합니다.

  

```

conda install ipykernel

python -m ipykernel install --user --name=가상환경 이름

conda install jupyter -y

jupyter lab

```

을 차례대로 입력하면

![jupyter](../images/jupyter.png)창이 뜨고

  

현재 "test"라는 이름으로 만들었기 때문에 가장 위의 test를 눌러 아래의 코드들을 실행해보면 확인할 수 있습니다.

  

```python

import torch

print(torch.cuda.is_available())

print(torch.cuda.device_count())

print(torch.cuda.get_device_name())

print(torch.backends.cudnn.enabled())

print(torch.backens.cuda.is_built())

```

  

![pycuda](../images/pycuda.png)

처럼 출력되면 pytorch-CUDA setting이 완료된것(GPU는 컴퓨터마다 상이할 수 있습니다).

  

여기까지 왔다면 대부분 Pytorch-CUDA setting은 되어있을 것 혹은 위의 과정을 따라왔다면 설치되어있을 것입니다.

  

<hr style="border:2px solid gray">

<hr style="border:2px solid gray">

<hr style="border:2px solid gray">

  
  

***이곳부터는 추천하지 않습니다.***

  

> 추천하지 않는 이유

앞으로 할 셋팅은 환경변수를 사용하여 Global하게 할 셋팅이기 때문에 다른 환경들과 충돌이 날 수 있습니다.

  

공식 문서는 [NVIDIA-CUDA](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/#network-repo-installation-for-ubuntu)

, [Nvidia-cuDNN-Docs](https://docs.nvidia.com/deeplearning/cudnn/install-guide/index.html)를 확인하시면 됩니다.

  

# 4. CUDA

현재 2023년 7월 20일 기준으로 CUDA 12.2, cuDNN 8.9.버전을 기준으로 합니다.

  

## 4.0 기존 파일 삭제

먼저 기존에 있던 nvidia에 관련된 것들을 지웁니다.

  

기존에 설치되어 있는 NVIDIA-CUDA-Toolkit 제거

```

sudo rm /etc/apt/sources.list.d/cuda*

sudo apt remove --autoremove nvidia-cuda-toolkit -y

sudo apt-get --purge remove 'cuda*' -y

sudo apt-get autoremove --purge 'cuda*' -y

```

  

NVIDIA 의존성 삭제

```

sudo apt-get purge nvidia*

sudo apt remove nvidia-*

sudo rm /etc/apt/sources.list.d/cuda*

sudo apt-get autoremove && sudo apt-get autoclean

sudo rm -rf /usr/local/cuda*

sudo reboot

```

  

>Draft

  

## 4.1 CUDA 다운로드

[CUDA Toolkit Download](https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=deb_local)에서

*Linux, x86_64, Ubuntu, 22.04, deb(local)*을 선택하고

  

![cuda](../images/cuda%20homepage.png)에 나온 한줄씩 Terminal에 복사, 붙여넣기 합니다.

  

```vim

sudo vi ~/.bashrc

export CUDA_HOME=/usr/local/cuda-{version}

export PATH=/usr/local/cuda-{version}/bin:$PATH

export LD_LIBRARY_PATH=/usr/local/cuda-{version}/lib64:$LD_LIBRARY_PATH

source ~/.ba

```

{version} 자리에는 설치하는 version을 적습니다.

위의 링크는 CUDA Toolkit 12.2 기준입니다.

설치가 완료되면 재부팅.

  

------------------

  

# 5. cuDNN

이 항목부터는 NVIDIA 계정이 필요합니다. 홈페이지

[cuDNN](https://developer.nvidia.com/rdp/cudnn-archive)

에서 Local Installer for **Linux x86_64 (Tar)**를 다운로드 받습니다.

![cudnn](../images/cudnn.png)

  

**다음 Command를 입력합니다.**

```

cd ~

cd Downloads

tar -xvf cudnn-linux-x86_64-8.9.3_cuda12.2-archive.tar.xz

sudo cp cudnn-*-archive/include/cudnn*.h /usr/local/cuda/include

sudo cp -P cudnn-*-archive/lib/libcudnn* /usr/local/cuda/lib64

sudo chmod a+r /usr/local/cuda/include/cudnn*.h /usr/local/cuda/lib64/libcudnn*

```

이후 pytorch 설치하고 확인을 동일하게 하시면 됩니다.

  
  
  
  

[^1]: 서버 컴퓨터 사용 문의는 fkrkty93@g.skku.edu

[^2]: 대부분 여기서 끝남