Supported Sensors and Environment Variables
============================================

Below is a list of sensors currently supported by the Generic Robot ROS package, as well as the configurable environment variables for each sensor.

2D Lasers
----------

- SICK LMS1xx Series
- Hokuyo UST-10LX

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_LASER``                ``0``                   ``1``              Enable/disable sensor
``CPR_LASER_MODEL``          ``lms1xx``              ``ust10``          Desired sensor model
``CPR_LASER_PARENT``         ``base_link``           Any link           Mount link for sensor
``CPR_LASER_TOPIC``          ``scan``                Any topic          ROS topic for sensor data
``CPR_LASER_XYZ``            ``"0 0 0"``             Any XYZ            Position of sensor
``CPR_LASER_RPY``            ``"0 0 0"``             Any RPY            Orientation of sensor
``CPR_LASER_IP``             ``192.168.131.20``      Any IP             IP address of sensor
===========================  ======================  =================  ===========================

3D Lasers
----------

- Velodyne VLP-16
- Velodyne HDL-32E

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_LASER_3D``             ``0``                   ``1``              Enable/disable sensor
``CPR_LASER_3D_MODEL``       ``vlp16``               ``hdl32e``         Desired sensor model
``CPR_LASER_3D_PARENT``      ``base_link``           Any link           Mount link for sensor
``CPR_LASER_3D_TOPIC``       ``scan``                Any topic          ROS topic for sensor data
``CPR_LASER_3D_XYZ``         ``"0 0 0"``             Any XYZ            Position of sensor
``CPR_LASER_3D_RPY``         ``"0 0 0"``             Any RPY            Orientation of sensor
``CPR_LASER_3D_IP``          ``192.168.131.20``      Any IP             IP address of sensor
===========================  ======================  =================  ===========================

GPS
----------

- NovAtel SMART7
- Garmin 18x

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_GPS``                  ``0``                   ``1``              Enable/disable sensor
``CPR_GPS_MODEL``            ``smart7``              ``18x``            Desired sensor model
``CPR_GPS_PARENT``           ``base_link``           Any link           Mount link for sensor
``CPR_GPS_XYZ``              ``"0 0 0"``             Any XYZ            Position of sensor
``CPR_GPS_RPY``              ``"0 0 0"``             Any RPY            Orientation of sensor
``CPR_GPS_PORT``             ``/dev/clearpath/gps``  Any port           Name of sensor device port
``CPR_GPS_BAUD``             ``57600``               Any baud rate      Baud rate of sensor
===========================  ======================  =================  ===========================

IMU
----------

- LORD MicroStrain GX3 Series
- LORD MicroStrain GX4 Series
- LORD MicroStrain GX5 Series
- LORD MicroStrain CX3 Series
- LORD MicroStrain RQ1 Series
- LORD MicroStrain GQ7 Series

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_MICROSTRAIN``          ``0``                   ``1``              Enable/disable sensor
``CPR_MICROSTRAIN_PARENT``   ``base_link``           Any link           Mount link for sensor
``CPR_MICROSTRAIN_XYZ``      ``"0 0 0"``             Any XYZ            Position of sensor
``CPR_MICROSTRAIN_RPY``      ``"0 0 0"``             Any RPY            Orientation of sensor
``CPR_MICROSTRAIN_PORT``     ``/dev/microstrain``    Any port           Name of sensor device port
===========================  ======================  =================  ===========================

Cameras
----------

- Teledyne FLIR Blackfly
- Intel RealSense D400 Series
- Intel RealSense L515

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_BLACKFLY``             ``0``                   ``1``              Enable/disable sensor
``CPR_BLACKFLY_PARENT``      ``base_link``           Any link           Mount link for sensor
``CPR_BLACKFLY_XYZ``         ``"0 0 0"``             Any XYZ            Position of sensor
``CPR_BLACKFLY_RPY``         ``"0 0 0"``             Any RPY            Orientation of sensor
``CPR_BLACKFLY_SERIAL``      ``0``                   Any serial no.     Serial number of sensor
``CPR_BLACKFLY_CALIB``       ``0``                   ``1``              If calibration file exists
===========================  ======================  =================  ===========================

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_REALSENSE``            ``0``                   ``1``              Enable/disable sensor
``CPR_REALSENSE_MODEL``      ``d435``                ``d435i``          Desired sensor model
                                                     ``d415`` 
                                                     ``d455`` 
                                                     ``l515`` 

``CPR_REALSENSE_PARENT``     ``base_link``           Any link           Mount link for sensor
``CPR_REALSENSE_TOPIC``      ``realsense``           Any topic          ROS topic for sensor data
``CPR_REALSENSE_XYZ``        ``"0 0 0"``             Any XYZ            Position of sensor
``CPR_REALSENSE_RPY``        ``"0 0 0"``             Any RPY            Orientation of sensor
===========================  ======================  =================  ===========================

Arms
-----

Coming soon!