Launch
=======

Another one of the features of the Generic Robot ROS package is automatically launching the driver launch files of the sensors attached to your robot.

To use this feature, you will need to create a ``.launch`` file that loads your robot's ``.urdf.xacro`` file into the ``robot_description`` parameter, and launches ``robot_state_publisher`` to broadcast your robot's ``tf`` transforms to ROS. Furthermore, if your robot has any non-fixed joints (i.e. wheels), your ``.launch`` file will also need to launch the ``joint_state_publisher`` to broadcast your robot's joints information. 

.. note::

  If you are unfamiliar with using ``robot_state_publisher`` to broadcast a robot's model from a ``.launch`` file, check out `this tutorial on the ROS Wiki <http://wiki.ros.org/robot_state_publisher/Tutorials/Using%20the%20robot%20state%20publisher%20on%20your%20own%20robot>`_.

For the purpose of this tutorial, we will be using the example ``description.launch`` file which can be found `here <https://github.com/jyang-cpr/generic_robot/blob/noetic-devel/example/description.launch>`_.

Upon closer inspection, you will notice that this file simply loads the ``generic_robot.urdf.xacro`` file into the ``robot_description`` parameter, and launches both ``robot_state_publisher`` and ``joint_state_publisher``. 

After scrolling to the bottom of the example ``description.launch`` file, you will notice the following line responsible for including the Generic Robot ROS package's various sensor driver launch files:

.. code-block:: bash

    <include file="$(find generic_robot)/launch/accessories.launch"/>

Simply add this line to the bottom of your robot's ``.launch`` file as well!