# Linux Basics
## Metadata
- ItemType: book
- Authors: 
- Collection: [[C++]]
- Date: 2022
- PDF Attachments: [《鸟哥的Linux私房菜-基础篇》第四版.pdf](zotero://open-pdf/library/items/D9D36QWX)
- Tags: 

👣➿👣

#### Turtlebot
- roslaunch turtlebot_bringup minimal.launch
- roslaunch turtlebot_teleop keyboard_teleop.launch
- roslaunch kinect2_bridge kinect2_laser.launch

### ROS
- ros composition:![[Pasted image 20220927235212.png]]
- 通信机制 - 计算图：
	- 节点：椭圆；代表功能，图像采集、处理、驱动，SLAM导航相关算法
	- 箭头：节点之间数据的流向，标注了数据的内容![[Pasted image 20220927235554.png|800]]
- 开发工具（仿真环境gazebo，TF坐标变化，Rviz可视化工具，QT工具）
- 生态系统（发行版dist，软件仓库repo
- Node节点：![[Pasted image 20220928230416.png]]
- Topic话题通信：Publisher - Subscriber![[Pasted image 20220928230040.png]]
- Service服务通信：![[Pasted image 20220928230123.png]]
- Quick Overview of Graph Concepts![[Pasted image 20220929144738.png]]
- 文件系统![[Pasted image 20220928003355.png]]
- ros命令行工具：
	- `roscore`= ros+core : master (provides name service for ROS) + rosout (stdout/stderr) + parameter server (parameter server will be introduced later)
	- `rosrun [package_name] [node_name]` :rosrun allows you to use the package name to directly run a node within a package (without having to know the package path).
		- `rosrun turtlesim turtlesim_node`
	- `rqt_graph`: check the node and topic
	- `rosnode list`: list all the nodes
	- `rosnode info /[node]`: get the info of node
	- `rostopic list`
	- `rostopic echo`: print the message of the topic
	- `rostopic pub`: pass message to the topic
		- rostopic pub /turtle1/cmd_vel geometry_msgs/Twist "linear:
			  x: 0.0
			  y: 0.0
			  z: 0.0
			angular:
			  x: 0.0
			  y: 0.0
			  z: 0.0"
		- (topic name) (data structure of the message) (message content) m/s, rad/s
	- `rosservice call` : make a request of the serivice
	- `rosbag record -a -o [path/filename]`: pack all message of topics in file
	- `rosbag play [filename].bag`
- catkin workspace:
	- `mkdir -p ~/catkin_ws/src`  // create two directories
	- `cd ~/catkin_ws/src/`
	- `catkin_init_workspace`  // under the src, to create `CMakeLists.txt`
	- `catkin_create_pkg test_pkg std_msgs rospy roscpp`  // only create package in src directory
	- `catkin_make`   // only make in workspace directory
	- `source devel/setup.bash`   //  set up the environment variable, source command executes a program in the current shell, to let system find this ws and pkg, to avoid error when rospack
	- `echo $ROS_PACKAGE_PATH`   // get the path of package 
	- `rospack depends1 test_pkg ` // check depends1 of a package (must source first, and must cd to src)
- catkin package:
	- `package.xml` provides the metadata for the package: e.g., name, version, dependency
	- `CMakeLists.txt` 描述package的编译规则，使用cmake语法（cmake是基于gcc(GNU Compiler Collection)的编译器），设置怎么样编译cpp代码，放入编译内容，注意是package里的
		- `add_executable([target] src/[script].cpp)` 把cpp文件**编译**为可执行文件
		- `target_link_libraries([target] ${catkin_LIBRARIES})` 把可执行文件和ros相关库文件做链接，本质上就是做连接
	- `/include` C++ header files
	- `/src` source files
add_executable(velocity_publisher src/velocity_publisher.cpp)
target_link_libraries(velocity_publisher ${catkin_LIBRARIES})







### 计算机概论
- x86架构的CPU：
	- 由于 AMD、Intel、VIA 所开发出来的 x86 架构 CPU 被大量使用于个人计算机(Personal computer)用途 上面， 因此，个人计算机常被称为 x86 架构的计算机！那为何称为 x86 架构(注 8)呢？ 这是因为最 早的那颗 Intel 发展出来的 CPU 代号称为 8086，后来依此架构又开发出 80286, 80386...， 因此这种架 构的 CPU 就被称为 x86 架构了。
	- 在 2003 年以前由 Intel 所开发的 x86 架构 CPU 由 8 位升级到 16、32 位，后来 AMD 依此架构修改新 一代的 CPU 为 64 位， 为了区别两者的差异，因此 64 位的个人计算机 CPU 又被统称为 x86_64 的架 构喔
- 64 位 CPU：
	- 所谓的位指的是 CPU 一次数据读取的最大量！64 位 CPU 代表 CPU 一次可以读写 64bits 这么多的数据，32 位 CPU 则是 CPU 一次只能读取 32 位的意思

![[Pasted image 20220918171719.png|450]]


👣➿👣