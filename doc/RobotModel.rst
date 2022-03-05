Setting Up Your Robot's Model
==============================

One of the features of the Robot Customizer ROS package is automatically adding models of sensors onto your robot's model. 

To use this feature, you will need to build your robot's model, include the Robot Customizer ROS package's sensor models in your robot's model, and broadcast your robot's updated model in ROS.

URDF
-----

1. Create a ``.urdf.xacro`` file that describes your robot's model. 

.. note::

  A ``.urdf.xacro`` file serves the same purpose as a regular ``.urdf`` file; that is, describing a robot's model through URDF. However, a ``.urdf.xacro`` file also enables the usage of ``xacro`` macros.

.. note::

  If you are unfamiliar with what URDF is, how URDF works, and/or how to use ``xacro`` to improve a ``.urdf`` file, check out `this tutorial on the ROS Wiki <http://wiki.ros.org/urdf/Tutorials>`_.

For the purpose of this tutorial, we will be using the example ``generic_robot.urdf.xacro`` file which can be found `here <https://github.com/clearpathrobotics/cpr_robot_customizer/blob/noetic-devel/example/generic_robot.urdf.xacro>`_. Upon closer inspection, you will notice that this file simply creates the links and joints for a generic robot. This file also leverages ``xacro`` to reuse properties, create macros, and most importantly, include other ``.urdf.xacro`` files!

2. Scroll to the bottom of the example ``generic_robot.urdf.xacro`` file and notice the following line responsible for including the Robot Customizer ROS package's sensor models:

.. code-block:: bash

  <xacro:include filename="$(find cpr_robot_customizer)/urdf/accessories.urdf.xacro" />

3. Add the line in step 2. to the bottom of your robot's ``.urdf.xacro`` file. 

Launch
-------

1. Create a ``.launch`` file that loads your robot's ``.urdf.xacro`` file into the ``robot_description`` parameter, and launches ``robot_state_publisher`` to broadcast your robot's ``tf`` transforms to ROS. If your robot has any non-fixed joints (e.g. wheels), your ``.launch`` file will also need to launch the ``joint_state_publisher`` to broadcast your robot's joints information. 

.. note::

  If you are unfamiliar with using ``robot_state_publisher`` to broadcast a robot's model from a ``.launch`` file, check out `this tutorial on the ROS Wiki <http://wiki.ros.org/robot_state_publisher/Tutorials/Using%20the%20robot%20state%20publisher%20on%20your%20own%20robot>`_.

For the purpose of this tutorial, we will be using the example ``description.launch`` file which can be found `here <https://github.com/clearpathrobotics/cpr_robot_customizer/blob/noetic-devel/example/description.launch>`_. Upon closer inspection, you will notice that this file simply loads the ``generic_robot.urdf.xacro`` file into the ``robot_description`` parameter, and launches both ``robot_state_publisher`` and ``joint_state_publisher``.

2. Scroll to the bottom of the example ``description.launch`` file and notice the following line responsible for including the Robot Customizer ROS package's sensor driver launch files:

.. code-block:: bash

  <include file="$(find cpr_robot_customizer)/launch/accessories.launch"/>

3. **DO NOT** add the line in step 2. to the bottom of your robot's ``.launch`` file yet! Please continue to :doc:`the next section <SensorDrivers>` to learn how to include the sensors' drivers launch files to your robot.