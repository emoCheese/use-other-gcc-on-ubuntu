# Ubuntu-gcc
Ubuntu使用更高版本的gcc相关命令

## 一、更新和安装必要依赖
```bash
# 更新
sudo apt update
sudo apt upgrade -y

# 安装必要依赖
sudo apt install -y \
build-essential \
software-properties-common \
curl \
wget \
git \
cmake \
ninja-build \
pkg-config \
python3 \
python3-pip \
mesa-utils \
libgl1-mesa-dev \
libegl1-mesa-dev \
libxkbcommon-dev \
libwayland-dev \
libfontconfig1-dev \
libfreetype6-dev \
libx11-dev \
libx11-xcb-dev \
libxext-dev \
libxfixes-dev \
libxi-dev \
libxrender-dev \
libxcb1-dev \
libxcb-glx0-dev \
libxcb-keysyms1-dev \
libxcb-image0-dev \
libxcb-shm0-dev \
libxcb-icccm4-dev \
libxcb-sync-dev \
libxcb-xfixes0-dev \
libxcb-shape0-dev \
libxcb-randr0-dev \
libxcb-render-util0-dev \
libxcb-util-dev \
libxcb-xinerama0-dev \
libxcb-xkb-dev \
libxkbcommon-x11-dev \
libxcb-cursor-dev \
libxcb-cursor0
```

## 二、安装其他版本的 GCC

```bash
# 安装其他源
sudo add-apt-repository ppa:ubuntu-toolchain-r/test -y

sudo apt update
# 安装GCC
sudo apt install -y \
gcc-13 \
g++-13

# 验证
g++-13 --version
```

## 三、不要替换系统 gcc 

禁止：
```bash
sudo update-alternatives --config gcc
```
禁止：
```bash
sudo ln -sf /usr/bin/gcc-13 /usr/bin/gcc
```
Ubuntu 系统组件默有认绑定 gcc。

## 四、设置新安装的gcc环境变量

```bash
# 打开配置文件
vim ~/.bashrc

# 设置环境变量
export CC=gcc-13
export CXX=g++-13

# 更新
source ~/.bashrc
```


