# Installation

### Mujoco

1. Obtain a 30-day free trial on the MuJoCo website or free license if you are a student. The license key will arrive in an email with your username and password.
2. Download the MuJoCo version 2.0 binaries for [Linux](https://www.roboti.us/download/mujoco200_linux.zip) or [OSX](https://www.roboti.us/download/mujoco200_macos.zip).
3. Unzip the downloaded `mujoco200` directory into `~/.mujoco/mujoco200`, and place your license key (the `mjkey.txt` file from your email) at `~/.mujoco/mjkey.txt`.

Run `pip3 install -U 'mujoco-py<2.1,>=2.0'`. But before doing so, note that mujoco doesn't support the latest GCC compiler, so if you encountered `RuntimeError: Could not find GCC executable.` like me, you should install an older GCC compiler using `brew install gcc@6`(on MAC OS).

> https://github.com/openai/mujoco-py/issues/254

### cv2
```
sudo apt-get install python-opencv
pip install opencv-python
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
