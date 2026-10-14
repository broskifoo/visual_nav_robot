# Plan (OC = OpenCode, USER = me)
## Block 0: Setup check
OC: verify ROS 2 Jazzy, Gazebo Harmonic, ros_gz, colcon, rviz2, a Python venv, and that PyTorch sees the GPU in WSL. Set up the workspace structure and git.
USER: run the verification commands myself and read the report.
## Block 1: Robot and world in Gazebo
OC: differential-drive robot with RGB-D camera, IMU, wheel odometry; a world with walls and obstacles; ros_gz bridge; launch file; rviz2 view; keyboard teleop.
USER: drive the robot, inspect topics, draw the TF tree in my notes.
## Block 2: Logging and evaluation tools
OC: rosbag recording script, ground-truth pose extraction from Gazebo, trajectory plot and ATE error scripts.
USER: understand each metric and explain ATE in my own words.
## Block 3: Visual odometry node
OC: node skeleton, camera intrinsics handling, image subscribers, pose publisher, debug visualization.
USER WRITES: feature detection/matching (ORB), essential matrix, pose recovery, scale from depth. OC gives TODO skeleton and reviews only.
## Block 4: Sensor fusion
OC: set up robot_localization EKF (wheel odom + IMU + my VO). Compare 3 runs: wheel only, VO only, fused.
USER WRITES: covariance choices and tuning, with a written explanation of what changed and why.
## Block 5: Dataset generation
OC: script to drive the robot automatically in many places, save RGB + depth + auto-generated drivable-floor labels (Gazebo segmentation camera or depth-based ground plane), train/val/test split.
USER: inspect 50 random samples and note label mistakes.
## Block 6: Train the vision model
OC: PyTorch data loader, training loop skeleton, IoU metric, logging, checkpointing.
USER WRITES: model choice (small U-Net or MobileNet-based), loss, augmentations, hyperparameters. I run and record experiments.
## Block 7: Deploy the model in ROS 2
OC: ONNX export, inference node, latency and FPS measurement, publish the segmentation mask.
USER: explain why accuracy alone is not enough and what latency does to a moving robot.
## Block 8: Mapping and navigation
OC: SLAM Toolbox mapping, turn my models mask into a costmap layer, Nav2 config, goal sending script.
USER: tune costmap and planner parameters and record what breaks.
## Block 9: Experiments
OC: automate runs (N goals per setup) and collect success rate, path length, collisions, time. Compare depth-only vs my model, lighting/texture randomization, noisy sensors.
USER: analyze results and write conclusions.
## Block 10: Extra ML module (language commands OR anomaly detection, decided later)
Plan first, then build, same rules.
## Block 11: Final write-up
OC: README, architecture diagram, demo script, results tables.
USER: write the  resusc;?s what I learned and  resusc;?s what failed sections in my own words.
