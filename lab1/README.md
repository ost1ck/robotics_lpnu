Terminal 1 (Starting the container and Gazebo simulation): 
cd ~/Labs/Lab1/robotics_lpnu
sudo ./scripts/cmd run
cd src/code/lab1
gz sim worlds/robot.sdf 
Terminal 2 (Sending movement commands to the robot): 
cd ~/Labs/Lab1/robotics_lpnu
sudo ./scripts/cmd bash
gz topic -t "/cmd_vel" -m gz.msgs.Twist -p "linear: {x: 0.5}, angular: {z: 0.0}»
