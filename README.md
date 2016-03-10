# RobotArt-Columbia-2016

Elliott Ison (eci2109)

Hyun Seung Hong (hh2473)

Sheng Qian (sq2168)

Shengjia Zhang (sz2547)

## RobotArt
For our project, we would like to enable Baxter to automatically paint an artwork of our choice. This project is based on the RobotArt competition (http://robotart.org/), which is happening from October 2015 to May 2016.
We will be implementing a fully-automated execution of painting (Category 1 of RobotArt Competition), where the robot will be able to use visual feedback, image processing, and machine learning to paint a desired painting of our choice. The robot is assumed to be holding a brush and will have multiple colors of paint available to it. It will paint on a flat tabletop canvas using a reference picture.

For more information on the details of the competition guidelines, please visit RobotArt’s site.

### Milestones:
#### End of February:
- Learn and setup ROS and workspace: Try the ROS tutorial. Learn to use existing trajectory planners.
- Paper study in computer vision and robot painting.

#### Early March:
- Complete basic trajectory planning (get paint, draw a line): Use simulator to do the trajectory planning. Given the robot the starting point, end point and the constraints, enable it to finish the stroke.

#### Middle of March:
- Complete line segment painting algorithm (advanced trajectory planning). Try the trajectory planning in Baxter when the simulation is successful.
- Test on a circle or star(using more complicate stroke).

#### End of March:
- Coordinate calibration
- Visual feedback and image processing system to detect and correct error (pyramid segmentation). Based on the target painting and current painting, let the robot choose a set of best strokes(predefined) that will minimize the difference between the two paintings. First we may tune the parameters by experiments.

#### Early April:
- Machine learning (tier 2) (Image processing, feedback, and checking for correctness, possibly using K-Means Clustering): Use some learning methods to enable the Baxter learn how to get the best strokes.

#### Middle of April:
- Testing: Choose some paintings, let the Baxter take a picture of them and duplicate them.
- Submit our video and painting design to RobotArt

#### End of April:
- Presentation

### Possible division of work:
- Work will likely be done in programming pairs or as a group
- All team members should learn ROS, figure out how ROS works and set the simulation environment up.
- All: Trajectory planning
  * one pair can do the stroke realization
  * another pair can do the brush grasping and paint getting
* Each person can switch off the following jobs:
  * Understanding and researching algorithms
  * Coding the algorithm (up to two people)
  * Testing and calibration (up to two people)
  * Potential leaders for individual parts:
- Elliott & Sheng: understanding/researching visual feedback and image processing
- Shengjia: understanding image processing and machine learning
- Sheng & Hyun Seung: understanding trajectory planning

### Background references:
- Painter Robot: Manipulation of Paintbrush by Force and Visual Feedback:
  * http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.396.7903&rep=rep1&type=pdf
- Humanoid Robot Painter Assisted by a Human: 
  * http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6213403
- e-David Painting Robot:
  * http://www.informatik.uni-konstanz.de/en/edavid/
  * video:
    * https://vimeo.com/68859229 

### Possible options for paintings:
* http://www.dhresource.com/0x0s/f2-albu-g3-M01-BB-6B-rBVaHVQ4jpSAQ2aqAACh5xLWPj0726.jpg/simple-art-painting-owl-by-pablo-picasso.jpg by Pablo Picasso
* http://corioblog.com/lewitt_3.jpg by Sol LeWitt
* http://ecx.images-amazon.com/images/I/51zcbWqkXpL._SX258_BO1,204,203,200_.jpg by Sol LeWitt
* https://cdn.thinglink.me/api/image/410681348190109698/1024/10/scaletowidth Quia by Keith Haring

## Setup instructinos
For every new terminal, we must initialize the catkin worspace:
<pre>$ soruce /opt/ros/indigo/setup.bash
$ cd src
$ catkin_init_workspace
$ cd ../
$ catkin_make
$ source devel/setup.bash
</pre>

