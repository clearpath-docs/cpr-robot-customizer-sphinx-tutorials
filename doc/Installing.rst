Installing
===========

There are two ways to install the Robot Customizer ROS package on your robot's computer and/or on your computer, both of which are covered in this section.

Installing the Debian Package
------------------------------

**Add Clearpath Debian Package Repository**

Before you can install the Robot Customizer ROS package, you need to configure Ubuntu's APT package manager to add Clearpath's package server:

1. Install the authentication key for the ``packages.clearpathrobotics.com`` repository. In terminal, run:

.. code-block:: bash

    wget https://packages.clearpathrobotics.com/public.key -O - | sudo apt-key add -

2. Add the debian sources for the repository. In terminal, run:

.. code-block:: bash

    sudo sh -c 'echo "deb https://packages.clearpathrobotics.com/stable/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/clearpath-latest.list'

3. Update the computer's package cache. In terminal, run:

.. code-block:: bash

    sudo apt-get update

**Installing Debian Package**

1. You should now be able to install the Robot Customizer ROS package. In terminal, run:

.. code-block :: bash

    sudo apt-get install ros-noetic-cpr-robot-customizer

Installing from Source
-----------------------

The Robot Customizer ROS package is available on `GitHub <https://github.com/clearpathrobotics/cpr_robot_customizer>`_, and can be compiled and installed from source if desired:

1. Create a workspace directory. In terminal, run:

.. code-block:: bash

    mkdir -p ~/catkin_ws/src

2. Clone the Robot Customizer repository into your workspace directory. In terminal, run:

.. code-block:: bash

    cd ~/catkin_ws_ws/src
    git clone -b noetic-devel https://github.com/clearpathrobotics/cpr_robot_customizer
    cd ..

3. Install additional dependencies. In terminal, run:

.. code-block:: bash

    rosdep install --from-paths src --ignore-src --rosdistro=$ROS_DISTRO -r -y

4. Build the workspace. In terminal, run:

.. code-block:: bash

    catkin_make

5. You can now source your workspace to make use of the Robot Customizer ROS package you just built. In terminal, run:

.. code-block:: bash

    source devel/setup.bash
