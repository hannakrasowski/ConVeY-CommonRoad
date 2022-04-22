# CommonRoad Search: Search-based Motion Planner with Motion Primitives

This is based on the programing exercise of the lecture **Techniques in Artificial Intelligence (IN2062)** delivered at the Department of Informatics, TUM. The task in this exercise is to implement a heuristic function and/or a search algorithm with motion primitives to solve [CommonRoad](https://commonroad.in.tum.de/) scenarios. The following search algorithms have been implemented as examples:
- Breadth First Search
- Depth First Search
- Depth-limited Search
- Uniform Cost Search (aka Dijkstra's algorithm)
- Greedy Best First Search
- A* Search

The code is written in Python 3.7 and has been tested on Ubuntu 18.04. **The original repository can be cloned with:**

```sh
$ git clone https://gitlab.lrz.de/tum-cps/commonroad-search.git
```
For an easy start we created a binder image:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/hannakrasowski/ConVeY-CommonRoad/main)

## Ways to install locally

You can either run the code locally, in a virtual machine, or in a docker container.

1. **Ubuntu, MacOS, Windows**: a [VirtualBox](https://www.virtualbox.org/) image is available in which all the necessary packages have been installed. The virtual machine image can be downloaded via [this](https://nextcloud.in.tum.de/index.php/s/2BspiYon9KmHf75) link. The downloading and the default login passwords are both `commonroad`. You can update to the latest commit with typing the command in the `commonroad-search/` folder:

   ```sh
   $ git pull
   ```

2. **Ubuntu, MacOS, Windows**: a docker file and a docker image is available if you wish to run the code in a docker container. Refer to `docker/README.md` for further instructions. Minimum system requirements are listed [here](https://docs.docker.com/desktop/).

3. **Ubuntu 18.04/20.04, MacOS**: If you wish to install the code locally, proceed with the installation guide below.

## Installation Guide

**skip this section if you intend to run the code in the virtual machine or in the docker container.**

We recommend using [Anaconda](https://www.anaconda.com/) to manage your environment so that even if you mess something up, you can always have a safe and clean restart. A guide for managing python environments with Anaconda can be found [here](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).

After installing Anaconda, create a new environment with:
``` sh
$ conda create -n commonroad-py37 python=3.7 -y
```

Here the name of the environment is called **commonroad-py37**. You may also change this name as you wish. In such case, don't forget to change it in the following commands as well. **Always activate** this environment before you do anything related:

```sh
$ conda activate commonroad-py37
or
$ source activate commonroad-py37
```
Install `Jupyter Notebook` and supplementary modules:
```sh
$ conda install jupyter ipykernel ipywidgets sphinx scipy -y
$ jupyter nbextension install --py widgetsnbextension --user
$ jupyter nbextension enable widgetsnbextension --user --py
```
Then, install the dependencies with:

```sh
$ pip install -r requirements.txt
```

This will install related dependencies specified in `requirements.txt`. 

We install `Imagemagick` (required for saving GIF animations of solutions) with the following commands:

```sh
# Ubuntu
$ sudo apt-get install imagemagick imagemagick-doc -y

# MacOS
$ brew install imagemagick
```


## Getting Started

To proceed with the tutorials, open a terminal in `commonroad-search/` folder, and launch Jupyter Notebook kernel with:

```shell
$ jupyter notebook
```

In the pop-up tab (or: open http://localhost:9000/ if ran with docker, otherwise http://localhost:8888/, in the explorer), navigate to `tutorials/` and follow the tutorials one by one. After that, you may proceed with the exercise itself (see exercise guide for more detail).

## Useful Tools
If you are new here, it's worth to take a look at the following tools:
- [Jupyter Notebook](): an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. An introduction can be found [here](https://realpython.com/jupyter-notebook-introduction/).
- [PyCharm](https://www.jetbrains.com/pycharm/): one of the best Python IDEs on the market. It is free for students. A tutorial video can be seen [here](https://www.youtube.com/watch?v=56bPIGf4us0&list=PLX4nwNAsU8OJUuLvmUvxpg-bdPqYVODGU).
- [GitKraken](https://www.gitkraken.com/): a powerful and elegant multi-platform graphical interface for Git, as an alternative to the command line. It is free for students (with GitHub account). An introduction to GitKraken can be found [here](https://www.youtube.com/c/Gitkraken/playlists).

## Questions & Answers 

If you encountered any problem, please raise it in the [CommonRoad Forum](https://commonroad.in.tum.de/forum/) so that other students can also benefit from the answers to your questions.
