# quick_reference

Quick Reference Sheets

## Setting Up Linux Development Environment

- Ubuntu 22.04 LTS
- Google Chorme installed at browser. This allows syncing of my Google account.
- Enable Adblock Plus Premium
- `sudo apt install git`
- a repos directory is created `mkdir ~/repos`
- ssh key added to github see these [notes](https://www.dennisfgardner.com/notes/add-ssh-key-to-git-sever) for more details
- VS Code installed see these [notes](https://www.dennisfgardner.com/notes/vs-code) for the extensions I like
- `sudo apt install build-essential`
- to get manual pages `sudo apt-get install manpages-dev`
- the standalone Intel IPP is downloaded installed with `sudo ./l_ipp_oneapi_p_2021.7.0.25396.sh `
- `sudo apt install cmake`
- `sudo apt install -y make`
- `sudo apt install -y wget unzip`
- `sudo apt install cmake-qt-gui`
- `sudo apt install ffmpeg`
- `sudo apt install curl`

## For pyenv

`sudo apt install libedit-dev`
`curl https://pyenv.run | bash`
follow instructions after install to modify `~./bashrc`
then install python build dependencies
```bash
sudo apt update; sudo apt install build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev curl \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```

## For OpenCV

The instructions from [here](https://docs.opencv.org/4.x/d7/d9f/tutorial_linux_install.html) are followed to build contrib verson but these configurations are used:

```bash
cmake -DOPENCV_EXTRA_MODULES_PATH=../opencv_contrib-4.x/modules -DOPENCV_GENERATE_PKGCONFIG=ON -DOPENCV_DOWNLOAD_PATH=/tmp/opencv-cache ../opencv-4.x
```

followed by `sudo make install`
