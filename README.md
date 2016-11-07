There are three suggested way for installing OpenCV.

#### Using bash script files
1. Install directly by going to [this link](https://github.com/astorfi/Caffe_Framework/tree/master/Installation/OpenCV_Installation) and using one of the "OpenCV.sh" or "OpenCV_Alternative.sh" bash script files available in this repository.
 * The second file is more abstract and installs less dependancies. This may lead to have less conflicts and incompatibilties.
2. Install as follows for the particular version:
 * The first two files are the edited version of the second method.
```
wget https://raw.githubusercontent.com/jayrambhia/Install-OpenCV/master/Ubuntu/2.4/opencv2_4_9.sh
chmod +x opencv2_4_9.sh 
./opencv2_4_9.sh
```
However by using this method, [unsupported gpu architecture](http://stackoverflow.com/questions/28010399/build-opencv-with-cuda-support) error has been reported. Most like this is due to requirements of some `OpenCV` installations to define the "CUDA_GENERATION" explicitly.
#### Install from the source
Install using the source from the [source](http://docs.opencv.org/2.4/doc/tutorials/introduction/linux_install/linux_install.html)

#### Alternative Solution

Alternatively by adding `python-opencv` to the following part commands(installing dependencies) the opencv can be installed 
and also is compatible with most of the distributions.


# Open-CV Installation Procedure

This folder is related to OpenCV installation which is a dependecy for the Caffe.

Here's is the procedure and considerations:

1. Download and run the "OpenCV.sh" file for installing OpenCV.
2. Installing "ffmpeg" can be ignore for two reason:
  * the package might not be available in Ubuntu(14.04) 
  * Other possible incompatibilities.
  * "ffmpeg" can be installed from the source in a more eficient way.
3. In the "OpenCV.sh" file the command "make -j16" in line 17 is for using all the CPUs(speed up the process). In the part -jX, X is dependent to the number of CPUs supported by the system.

**If the "OpenCV.sh" file has some issues you can alternatively install "OpenCV_Alternative.sh" file.**
