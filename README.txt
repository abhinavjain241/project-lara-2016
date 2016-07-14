Please follow the steps below very carefully:
============================================

1. Boot up a computer running Linux or a Virtual Machine. The documentation has been written while using the following configuration:
	- Ubuntu 14.04
	- ROS Indigo
	- git

2. Open up a new terminal (Ctrl + Alt + T) and copy-paste or type the following command: (Omit the '$', just for reference)
	$ git clone https://github.com/abhinavjain241/comm_tcp.git

3. Once you run the above command, there will be a folder that is created in the directory with the name 'comm_tcp'. If the command fails, then you may not have git installed, for that go to Step 1. At this step, you can 'cd' in to the 'comm_tcp' directory. 

4. Run the following command to start the ROS Master: (Omit the '$', just for reference)
	$ roscore

If the above command fails, and shows something like 'roscore' not found, then either you don't have ROS installed, or you haven't configured your ~/.bashrc file to have the path to the ROS installation. 

5. Once ROS master is up and running, now you can either run the server or the client depending on what you want to test/check out.

6. To run the server, follow steps (7-10) and if you want to run the client, follow steps (11-_)

7. To start the server, make sure you follow steps `1-5' above, and then open a new terminal window (Ctrl + Alt + T or Ctrl + Shift + T), and run the following:
	$ ./scripts/l-runServer.sh

8. There should be a message saying 'Hello there! This node is listening on port 1024 for incoming connections'. If you get it, then the start was successful, else repeat the above steps again. 

9. Now you can connect to the server from another device (client), by specifying the IP address. To get the IP address in Unix, run the command: 
	$ ifconfig

in any terminal, and see the IP address for the particular network adapter. (eth0, eth1, wlan0)

10. To kill the above process, either close the terminal (safest option) or run another terminal and call the following command: (experimental)
	$ ./scripts/killServer.sh 

11. To start the server, make sure you follow steps `1-5' above, and then open a new terminal window (Ctrl + Alt + T or Ctrl + Shift + T), and run the following:
	$ ./scripts/l-runClient.sh <ip_address_of_server>

Make sure to specify the IP Address of the server. Communication will happen on port 1024.

12. If the server is running, and the connection is established, hopefully you'll recieve a message saying the following:

"How do you want the client to behave?:
1. Be able to send messages manually
2. Subscribe to /client_messages and send whatever's available there
"

If not, then the server might not be running on the other computer, or the IP address might have been input incorrectly.



Now for running the simulator on Gazebo,

1. Make sure you're in the Catkin workspace directory (i.e where ROS path is set). Mostly it might be ~/catkin_ws 

2. Open up a new terminal (Ctrl + Alt + T) and copy-paste or type the following command: (Omit the '$', just for reference)
	$ git clone https://github.com/abhinavjain241/RH-Y.git

3. Change the branch to 'package_dev', by running the following:
	$ git checkout package_dev

4. Go to the previous directory (catkin workspace) by running:
	$ cd ..

5. Run the catkin_make command:
	$ catkin_make

6. Run the following command to launch the simulator:
	$ roslaunch rhy_basic test.launch

7. To run the node which recieves messages on /server_messages, type the following command:
	$ rosrun rhy_basic rhyTest
