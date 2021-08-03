# Robot_arm-in-ROS
In this Repository will create and simulate robot arm using robot operating system (ROS).                                                                                           
It is concerned with preparing the required environment to run a robot arm simulation created by @smart-methods.                                                                 

ROS you can installed on Ubuntu by using Virtua Box or VMware, also you can using Online website : https://www.theconstructsim.com ,                                             
 For my project i using the website online.


# Start a new project 
After creating an account at: https://www.theconstructsim.com website, Must click on "create new project"                                                                   
 Start filling the blanks by choosing the version ROS such as melodic which I used,                                                                                           
 Then Writing the name of your project and description then click "create" . 



# Installing the package arduino_robot_arm 
Firstly, Open the "shell web"   

Add the "arduino_robot_arm " package "src"folder

Then use the command ($ sudo apt install git) to clone the robot arm package from GitHub by using the path,     

$ cd ~/catkin_ws/src           

$ sudo apt install git                                          

$ git clone https://github.com/smart-methods/arduino_robot_arm   

as shown in the picture :

<img width="959" alt="f1" src="https://user-images.githubusercontent.com/85851678/127936870-80992ad0-7f6e-4823-a2fd-a57984cb8f10.png">


# Install all the dependencies 
To run the packge we need some dependencies like (Movelt, joint state publisher, gazebo ...) so will used this commands :

 $ cd ~/catkin_ws
 
 $ rosdep install --from-paths src --ignore-src -r -y
 
 $ sudo apt-get install ros-melodic-moveit
 
 $ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
 
 $ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
 
 $ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
  
<img width="959" alt="f1" src="https://user-images.githubusercontent.com/85851678/127936870-80992ad0-7f6e-4823-a2fd-a57984cb8f10.png">
<img width="949" alt="f2" src="https://user-images.githubusercontent.com/85851678/127938031-36b420aa-1577-433d-a426-d8e72647d54a.png">


# Controlling the motors
Now will run the robot arm packge using this command ($ roslaunch robot_arm_pkg check_motors.launch ) the click on graphical tools which will open the window show the simulate arm , as shown in the picture :

<img width="948" alt="f3" src="https://user-images.githubusercontent.com/85851678/127938258-5cccf20c-372a-4503-8e67-f349f0eeb3c5.png">
<img width="577" alt="confing" src="https://user-images.githubusercontent.com/85851678/127938348-c9834510-209d-4a07-84f0-96bf879ca48f.png">

  
# Controlling the motors in simulation 
This commands will run the arm simulation on RVis and Gazebo 

$ roslaunch robot_arm_pkg check_motors.launch

$ roslaunch robot_arm_pkg check_motors_gazebo.launch

$ rosrun robot_arm_pkg joint_states_to_gazebo.py

As shown in the pictures 

<img width="948" alt="s1" src="https://user-images.githubusercontent.com/85851678/127938473-f18522d6-5a61-4259-a7af-7a4ea96b44ac.png">

<img width="950" alt="th1" src="https://user-images.githubusercontent.com/85851678/127938486-9d1f82da-5650-459b-8cee-a837840065a7.png">

<img width="949" alt="fro1" src="https://user-images.githubusercontent.com/85851678/127938492-975c987a-353e-43dd-a50a-fe9c761ea949.png">

<img width="948" alt="ff1" src="https://user-images.githubusercontent.com/85851678/127938620-c31cae52-f646-403a-a606-21bea653cd89.png">


# Movelt in Rvis 
To define the positioning and movements of the arm will using movelt which is simulate the arm movement in different directions, By Using this command ($ roslaunch moveit_pkg demo.launch), As shown in the pictures : 

<img width="949" alt="fro1" src="https://user-images.githubusercontent.com/85851678/127938907-c64fe49e-a313-4e0d-80d3-be91e27a9fec.png">

<img width="460" alt="movement" src="https://user-images.githubusercontent.com/85851678/127939253-fa54fd7a-601a-4c0f-8f8b-6ab3d22d0eb6.png">


