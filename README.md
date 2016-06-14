# Summer Project @ LaRA, 2016
Summer Internship Project at LaRA, HEIG-VD.

### Things in my ambit:
- Model of RH-Y robot in Gazebo (v0.0.1 done :heavy_check_mark:) ![Progress](http://progressed.io/bar/33?title=progress)
- ROS Node and Package for the same in Gazebo ![Progress](http://progressed.io/bar/0?title=untouched)
- A world file for Lab #C38 in Gazebo (v0.0.1 done :heavy_check_mark:) ![Progress](http://progressed.io/bar/33?title=progress)
- Communication between C++ and C# chat application ![Progress](http://progressed.io/bar/10?title=progress)
- Piaget as a ROS node, and ROS as a driver provider for Piaget

### Questions:
- Why do we need a chat application at all? What is it's use in connecting different robots to Piaget?

### Todo:
- Figure out a middleware for communication between C# and Linux.
  * [This](https://zeroc.com/distributions/ice) may be helpful.
  * Have a look at [XML-RPC](http://xmlrpc.scripting.com/) as well.
  * Look at [this](http://ros-users.122217.n3.nabble.com/communicating-with-windows-td895215.html) forum discussion.
  * [Hello World from Windows](http://wiki.ros.org/rosserial_windows/Tutorials/Hello%20World).
- Make differential drive controller on the RH-Y robot work, using the ROS node, i.e rhy_basic to send commands.
- Study documentation for Piaget (C++, C#)
- Get answers to above questions

### Work in Progress
- Writing a Server and Client implementation using Ice middleware for C# and C++. Links [#1](https://doc.zeroc.com/display/Ice36/Writing+an+Ice+Application+with+C-Sharp), [#2](https://doc.zeroc.com/display/Ice36/Writing+a+Slice+Definition), [#3](https://doc.zeroc.com/display/Ice36/The+Slice+Language), [#4](https://doc.zeroc.com/pages/viewpage.action?pageId=14030991), [#5](https://doc.zeroc.com/display/Ice36/Server-Side+Slice-to-C-Sharp+Mapping), [#6](https://doc.zeroc.com/display/Ice36/Client-Side+Slice-to-C-Sharp+Mapping), [#7](https://doc.zeroc.com/display/Ice36/Hello+World+Application)
- Folder called AJ in Ubuntu Virtual Box on C38PC09 at home directory. Some ice definitions with generated C# files.
