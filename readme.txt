If you have not used ros before, you can follow the steps in the pdf file and install it. (for ununtu 16.04)

If you already have ros kinetic installed on your computer, you can skip these steps. just put the a1_456_answer and a1_456_referee files into src inside catkin_ws, and a1_456_results_maps should be in the same directory as catkin_ws. Then you can run the ros environment Rviz simulator and code with commands specified in pdf. 

If you actually need only algorithm to using in a maze, it will be enough to examine the code in the explorer_node_a1_456_python.py file to see all the important pieces of code and the algorithm behind the robot's movement without crash.



The working logic of the code is simply as follows:

After the robot starts its movement, it moves to the right at a slow speed (rotational speed 0.1). The purpose of this movement is to find a wall. After finding the wall, when it is full, the left rotary sensors are emptied, so it takes the wall to the right, then it follows the wall straight with the follow_wall function.

For the nan value problem, which is the biggest problem, by keeping the previous value of the variable holding the distance to the wall, the pre_region was tried to be saved as much as possible from the possible hitting the wall.

For some special cases, pre_region was not assigned any value, for example starting from the middle of the large room, and since all region values would be nan, pre_region was initially assigned 10 values so that the wall discovery function could start.


Mehmet Calikus
