# Project: Learning-Based Visual Navigation Robot in Gazebo

## Goal
A simulated robot that localizes and navigates using camera input, with a vision model I train myself. The main goal is for ME to LEARN CV, ML and robotics. Finishing fast is not the goal.

## Environment
- Windows 11 + WSL2 Ubuntu 24.04, ROS 2 Jazzy, Gazebo Harmonic (ros_gz)
- Project root: ~/visual_nav_robot (this is also the ROS workspace, packages go in src/)
- GPU: RTX 3050 Laptop, 4GB VRAM -> small models, low resolution, mixed precision
- Python for nodes and training. Free tools only.

## About me
Beginner in robotics and CV. Explain in simple English with the reasoning behind each decision. Casual, direct tone. English only. I also use a separate tutor (GPT) for the parts I write myself, so I may paste my code here for review.

## How to work
1. Work in BLOCKS from PLAN.md. ONE block at a time. Never start the next block until I say "approved".
2. Before each block: give a short plan (what, why, which files) and wait for my OK.
3. While working: send short status updates (what you are doing, what worked, what failed). Tell me every decision or assumption you make.
4. Commit to git after every working step with a clear message.
5. Keep code minimal and paste-ready, with descriptive names. No fancy abstractions.
6. Parts marked "USER WRITES" are mine. Do NOT write the solution. Create a skeleton with TODO comments and explain what each TODO needs. Review my code when I share it, and give hints before answers.
7. If something fails, explain the cause in simple terms before fixing it.

## After EVERY block write a report
Create reports/blockN_report.md containing:
- What was done and which files were created/changed
- Commands to run and the output that proves it works
- New concepts used, each explained simply (what, why needed, where in the code)
- Problems hit and how they were fixed
- 5 revision questions for me (answers at the bottom)
- What I must do or understand before approving
Also add a short entry to PROGRESS.md (block, status, date, next step).
Then STOP and wait for my "approved".