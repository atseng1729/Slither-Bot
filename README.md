# Environment set up instructions

## Installing and making conda environment
```sh
$ make folder with project and go into folder
$ install [conda](https://www.digitalocean.com/community/tutorials/how-to-install-anaconda-on-ubuntu-18-04-quickstart)
$ conda create --name slither python=3.5 pip (note: adding pip is necessary since you want a local version of pip here)
$ conda activate slither (try python -V and pip -V and confirm that they\'re python 3.5)
```

## Installing needed packages
```sh
$ sudo apt-get update
$ sudo apt-get install -y tmux htop cmake golang libjpeg-dev libgtk2.0-0 ffmpeg
$ pip install numpy
```

## Install universe (make sure you're doing everything in conda environment)
```sh
$ git clone https://github.com/openai/universe.git
$ cd universe
$ pip install -e .
```

## Follow instructions to install [docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04)

## If you get error (go_vncdriver was installed without OpenGL support) then do following:
```sh
$ sudo apt-get install -y python-dev make golang libjpeg-turbo8-dev
$ sudo apt-get install libx11-dev libxcursor-dev libxrandr-dev libxinerama-dev libxi-dev \
  libxxf86vm-dev libgl1-mesa-dev mesa-common-dev
$ git clone https://github.com/openai/go-vncdriver.git
$ cd go-vncdriver
$ sudo (your path to conda python 3.5) build.py
  For Example: my command - sudo /home/atseng1729/anaconda3/envs/slither/bin/python build.py
$ pip install -e .
```

## To test if everything works, create new file
```sh
$ python test.py
```
