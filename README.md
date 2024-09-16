# tortoisebot_webapp

---

This package implement a web application to interact with a tortoisebot.
Using this web interface you will be able to control the robot using different control method and have feedback from the robot.

Control:
    - Manual control using a joystcik
    - Send 'move to waypoint X' command

Feedback:
    - Front camera
    - Map generated with SLAM algorythm
    - 3D model of the robot


## Instalation
---

### prerequisites

- ROS
- Gazebo
- webbrowser         

### Install

 1- Clone the repository inside your workspace:  
`git clone https://github.com/maxime-cognie/tortoisebot_webapp.git`  


## Test the web-app
---

To test the web-app:    
- Launch the simulation:   
`roslaunch tortoisebot_gazebo tortoisebot_docking.launch`

- Launch ROSBridge + the video servers:      
`roslaunch course_web_dev_ros web.launch`    

- Launch the mapping node:
`roslaunch tortoisebot_slam mapping.launch`

- Launch the waypoints action server:
`rosrun course_web_dev_ros tortoisebot_action_server.py`

- Start the web-app:
```
cd ~/webpage_ws/tortoisebot_webapp
python -m http.server 7000
```
