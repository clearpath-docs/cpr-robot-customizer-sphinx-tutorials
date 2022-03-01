Setting Environment Variables
==============================

Once you have completed the :doc:`<Installing>`, :doc:`<URDF>`, and :doc:`<Launch>` tutorial sections, you are now ready to use the Environment Variable interface provided by the Generic Robot ROS package!

The complete list of supported sensors and environment variables can be found :doc:`here <SupportedSensorsEnvars>`.

In this section of the tutorial, we will go through an example usage of the Environment Variable interface for a Hokuyo UST-10LX 2D laser scanner.

1. Enable the Hokuyo UST-10LX 2D laser scanner. In terminal, run:

.. code-block:: bash

  export CPR_LASER=1
  export CPR_LASER_MODEL=ust10

2. Choose a link in your robot model (defined in your robot's ``.urdf.xacro`` file) to mount the Hokuyo UST-10LX 2D laser scanner. Feel free to adjust the XYZ and RPY coordinates of the Hokuyo UST-10LX 2D laser scanner relative to the chosen link. For example, we will mount it on the ``box`` link in the ``generic_robot.urdf.xacro`` file, offset slightly in the negative x and positive z directions. In terminal, run:

.. code-block:: bash

  export CPR_LASER_PARENT=box
  export CPR_LASER_XYZ="-0.1 0 0.12"
  export CPR_LASER_RPY="0 0 0"

3. Choose a ROS topic that the driver launch file will publish 2D laser scan data to. For example, we will choose to have the 2D laser scan data published to the ``/scan`` ROS topic. In terminal, run:

.. code-block:: bash

  export CPR_LASER_TOPIC=scan

4. Choose the IP address assigned to the Hokuyo UST-10LX 2D laser scanner. This will let the driver launch file know where to detect it, and allow it to start retrieving 2D laser scan data. From factory, the IP address of the Hokuyo UST-10LX 2D laser scanner is set to ``192.168.0.10``. In terminal, run:

.. code-block:: bash

  export CPR_LASER_IP=192.168.0.10

5. At this point, you can try launching your robot's ``.launch`` file. The ``description.launch`` file used in

.. code-block:: bash

  roslaunch generic_robot description.launch

If your Hokuyo UST-10LX 2D laser scanner is connected to your robot's computer and with the IP address configured correctly, then launching the ``.launch`` file should automatically launch the Hokuyo UST-10LX 2D laser scanner's driver. You can verify this by checking the output in your terminal, and also by checking the 2D laser scan data currently being published in ROS. In terminal, run:

.. code-block:: bash

  rostopic echo /scan

The state of your robot (based on your robot's model) will also be published to ROS; however, you currently will not be able to visually verify this.