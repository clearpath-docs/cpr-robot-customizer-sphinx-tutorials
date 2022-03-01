URDF
=====

One of the features of the Generic Robot ROS package is automatically adding models of sensors onto your robot's model.

To use this feature, you will need to create a ``.urdf.xacro`` file that describes your robot's model. A ``.urdf.xacro`` file serves the same purpose as a regular ``.urdf`` file; that is, describing a robot's model through URDF. However, a ``.urdf.xacro`` file also enables the usage of ``xacro`` macros.

.. note::

  If you are unfamiliar with what URDF is, how URDF works, and/or how to use ``xacro`` to improve a ``.urdf`` file, check out `this tutorial on the ROS Wiki <http://wiki.ros.org/urdf/Tutorials>`_.

For the purpose of this tutorial, we will be using the example ``generic_robot.urdf.xacro`` file which can be found `here <https://github.com/jyang-cpr/generic_robot/blob/noetic-devel/example/generic_robot.urdf.xacro>`_.

Upon closer inspection, you will notice that this file simply creates the links and joints for a generic robot. This file also leverages ``xacro`` to reuse properties, create macros, and most importantly, include other ``.urdf.xacro`` files!

After scrolling to the bottom of the example ``generic_robot.urdf.xacro`` file, you will notice the following line responsible for including the Generic Robot ROS package's various sensor models:

.. code-block:: bash

    <xacro:include filename="$(find generic_robot)/urdf/accessories.urdf.xacro" />

Simply add this line to the bottom of your robot's ``.urdf.xacro`` file as well!