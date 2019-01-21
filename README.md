# VisioTec Libraries #

This repository contains ready-to-use computer vision libraries developed at the VisioTec research group of the CTI Renato Archer. Further information about this group can be found [here](https://sites.google.com/site/geraldofsilveira/talks#TOC-Project-VISIOTEC-in-5-slides).

## Video Examples ##

Click on the thumbnails to watch the videos on YouTube. These videos were created using the VisioTec Libraries in our ROS environment. This environment is also publicly available [here](https://github.com/lukscasanova/vtec_ros).

* Intensity-based visual tracking with full 8-DoF homography

[![YouTube](https://img.youtube.com/vi/r7kZLqQ5xbI/0.jpg)](https://www.youtube.com/watch?v=r7kZLqQ5xbI)

* Intensity-based visual tracking with affine 6-DoF homography

[![YouTube](https://img.youtube.com/vi/W-7otD3THM4/0.jpg)](https://www.youtube.com/watch?v=W-7otD3THM4)

## Installation ##

### System Requirements ###

The master branch contains libraries that have been tested on Ubuntu 16.04. 
To compile and use that branch, you must satisfy the following requirements:

* GCC version 5.4.1 or later
* CMake version 2.8.3 or later
* Git

If you use an older system, we offer the [*legacy*](https://github.com/lukscasanova/vtec/tree/legacy) branch, which is based on c++98 standard.

### Download and Compiling ###

There are two ways of getting our libraries. You can either use the [releases](https://github.com/lukscasanova/vtec/releases) page or use **git** to clone the repo. We provide one version of our library based on the latest c++11 standard and another version based on the c++98 standard. The older c++98 version can be found on the *legacy* branch. 

#### Latest Release ####

Using the latest release version allows you to use the most stable version of our code. Follow the instructions on the [releases](https://github.com/lukscasanova/vtec/releases) page for the installation details.

#### Cloning The Repository ####

Cloning the repository allows you to be up-to-date with the latest -- but possibly unstable -- changes in our codebase. You should be familiar with Git to use this option. You can get more information about it in [here](https://help.github.com/articles/set-up-git). To clone and compile, use the following instructions.

```
git clone https://github.com/lukscasanova/vtec.git
```

**OPTIONAL**: If you want to use the *legacy* branch, which is based on the older c++98 standard, do the following command. Otherwise, skip the next command.

```
git checkout legacy
```

Compile the examples code with the following commands:

```
cd vtec
mkdir build
cd build
cmake ..
make
```

## Libraries ##

### Homography Optimizer ###

<<<<<<< HEAD
This library estimates the homography and photometric parameters that minimize the pixel intensity-based error between the reference the current images. This algorithm is called Intensity-Based Global Homography Optimizer (IBGHO), as it is uses a direct approach to the estimation, i.e. with no intermediate steps such as feature extraction or matching, and is robust to global illumination changes. We also offer 3 variants of the algorithm, which make different assumptions about the motion constraints involved.

#### Documentation and Citing ####

The technical report available [here](https://github.com/lukscasanova/vtec/blob/master/vtec_ibgho_TR.pdf) describes the software and its working principles. If you use this software, please cite the technical report using:

```
@TechReport{nogueira2017,
  author = {Lucas Nogueira and Ely de Paiva and Geraldo Silveira},
  title  = {{VISIOTEC} Intensity-based Homography Optimization Software: Basic Theory and Use Cases},
  number = {CTI-VTEC-TR-01-2017},
  institution = {CTI},
  year = {2017},
  address = {Brazil}
}

```

#### Examples ####

After compiling, run the following commands *from the root* of the repository.


* Homography Optimizer: 
```bash
  $ ./build/vtec_ibg_optimize_homography_example
```

* Visual Tracking:
```bash
  $ ./build/vtec_ibg_tracker_example
```

<<<<<<< HEAD
More details on the examples can be found on the [technical report](https://github.com/lukscasanova/vtec/blob/master/vtec_ibgho_RR.pdf).


## Resources ##

* Releases: [https://github.com/lukscasanova/vtec/releases](https://github.com/lukscasanova/vtec/releases)

* IBGHO Technical Report: [vtec_ibgho_TR.pdf](https://github.com/lukscasanova/vtec/blob/master/vtec_ibgho_TR.pdf)

* VisioTec ROS package: [https://github.com/lukscasanova/vtec_ros](https://github.com/lukscasanova/vtec_ros/)

* Geraldo Silveira's website: [https://sites.google.com/site/geraldofsilveira/](https://sites.google.com/site/geraldofsilveira/)


## Licensing ##

This software is being made available for research purposes only.  See
the [LICENSE](LICENSE.txt) file in this directory for conditions of use.

## Bugs & Feature Requests

Please report bugs and request features using the [Issue Tracker](https://github.com/lukscasanova/vtec/issues).
