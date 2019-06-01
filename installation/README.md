# Installation

### cv2
```
sudo apt-get install python-opencv
```

### torch7

```
git clone https://github.com/torch/distro.git ~/torch --recursive
cd ~/torch; bash install-deps;
export TORCH_NVCC_FLAGS="-D__CUDA_NO_HALF_OPERATORS__"  # for cuda 9.0
./install.sh
source ~/.bashrc  # On Linux with bash
source ~/.zshrc  # On Linux with zsh
source ~/.profile  # On OSX or in Linux with none of the above.
```

### libsvm

```
# download libsvm from https://www.csie.ntu.edu.tw/~cjlin/libsvm/#download
make  # in libsvm/
make  # in libsvm/python/
```

when using libsvm, you need to:
```
import sys
sys.path.append('path/to/libsvm/python')
```
