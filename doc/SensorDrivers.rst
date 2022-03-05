Including Sensors' Drivers Launch Files
========================================

One of the features of the Robot Customizer ROS package is automatically launching the drivers launch files of the sensors attached to your robot.

.. note::

  You will only be able to use this feature if you have the physical sensors electromechnically integrated onto your physical robot! You will not be able to launch the sensors' drivers otherwise (e.g. if you are simulating your robot and the sensors).

1. Continuing from the :doc:`previous section <RobotModel>`, add the following line to the bottom of your robot's ``.launch`` file:

.. code-block:: bash

  <include file="$(find cpr_robot_customizer)/launch/accessories.launch"/>