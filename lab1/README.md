Terminal 1: Starting the Container and Gazebo
This terminal initializes the world and the physics engine.

cd ~/Labs/Lab1/robotics_lpnu
sudo ./scripts/cmd run
# Inside the container shell:
cd src/code/lab1
gz sim worlds/robot.sdf

Terminal 2: Sending Movement Commands
Use this terminal to manually control the robot's movement.

cd ~/Labs/Lab1/robotics_lpnu
sudo ./scripts/cmd bash
gz topic -t "/cmd_vel" -m gz.msgs.Twist -p "linear: {x: 0.5}, angular: {z: 0.0}"
