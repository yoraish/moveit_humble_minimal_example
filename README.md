A minimal example for MoveIt!2 on ROS Humble. 
This example comes as a quickstart-example, complementing the first C++ MoveIt!2 tutorial. Here, all we want is to move a Panda arm via C++ commands without building "code for the rest of MoveIt" :).

Most if not all of the code in this repo is from the MoveIt!2 docs. This is an attempt to compile it compactly and nothing more.

I followed the following steps, and you may do so too:
1. Install ROS Humble (see the ROS docs).
2. Install MoveIt!2 binaries using `sudo apt install ros-humble-moveit`, as specified [here](https://moveit.ros.org/install-moveit2/binary/).
3. Create a new workspace, say call it `moveit2_ws`, a `src` directory within it, and set the files of this repository to live there.
4. Build the workspace. From the `.../moveit2_ws` call `colcon build --mixin debug`.
5. Source the workspace `source moveit2_ws/install/setup.<your_shell>`.
6. In one terminal, start RViz and the main MoveIt!2 components with `ros2 launch hello_moveit demo.launch.py`. And in a second terminal run the motion request with `ros2 run ros2 run hello_moveit hello_moveit`.

This _should_ work! Building only a few packages and not 56 of them.

Note: this repo also includes a copy (yes, a copy, not a submodule) of the MoveIt!2 [`moveit_resources` package](https://github.com/ros-planning/moveit2/tree/humble). I had some issues with ROS version mismatch and MoveIt!2 branches, so I just copied it over for faster setup.
