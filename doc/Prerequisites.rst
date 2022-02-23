Prerequisites
==============

Before you can use the Generic Robot ROS package, there are a few prerequisites that must be met:

1. You have a robot and your robot's computer is running Ubuntu 20.04 (Focal) with ROS Noetic.

.. note::

  You can install Ubuntu 20.04 (Focal) and ROS Noetic on your robot's computer using `the Clearpath Robotics ISO image <https://packages.clearpathrobotics.com/stable/images/latest/noetic-focal/>`_. This ISO image specifically targets ``amd64`` Intel computers.

2. You have the physical sensors you wish to add to your robot and they are electromechanically integrated onto your robot already. The sensors you have must be on the :doc:`list of supported sensors <SupportedSensorsEnvars>`.

.. note::

  If you are unsure of which sensors to get for your robot, please check out `Clearpath Robotics' collection <https://store.clearpathrobotics.com/collections>`_.

3. You have a ``.urdf.xacro`` file that describes your robot's model. A ``.urdf.xacro`` file serves the same purpose as a regular ``.urdf`` file; that is, describing a robot's model through URDF. However, a ``.urdf.xacro`` file also enables the usage of ``xacro`` macros.

.. note::

  If you are unfamiliar with what URDF is, how URDF works, and/or how to use `xacro` to improve a ``.urdf`` file, check out `this tutorial on the ROS Wiki <http://wiki.ros.org/urdf/Tutorials>`_. You can also refer to `Clearpath Robotics' Jackal robot <https://github.com/jackal/jackal/blob/noetic-devel/jackal_description/urdf/jackal.urdf.xacro>`_ as an example.

4. You have a ``.launch`` file that loads your ``.urdf.xacro`` file into the ``robot_description`` parameter and launches ``robot_state_publisher`` to broadcast your robot's model (and state) to ``tf``.

.. note::

  If you are unfamiliar with using ``robot_state_publisher`` to broadcast a robot's model from a ``.launch`` file, check out `this tutorial on the ROS Wiki <http://wiki.ros.org/robot_state_publisher/Tutorials/Using%20the%20robot%20state%20publisher%20on%20your%20own%20robot>`_. You can also refer to `Clearpath Robotics' Jackal robot <https://github.com/jackal/jackal/blob/noetic-devel/jackal_description/launch/description.launch>`_ as an example.