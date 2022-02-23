Supported Sensors and Environment Variables
============================================

2D Lasers
----------

- SICK LMS1xx Series
- Hokuyo UST-10LX

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_LASER``                ``0``                   ``1``
``CPR_LASER_MODEL``          ``lms1xx``              ``ust10``
``CPR_LASER_PARENT``         ``base_link``           Any link
``CPR_LASER_TOPIC``          ``scan``                Any topic
``CPR_LASER_XYZ``            ``"0 0 0"``             Any XYZ
``CPR_LASER_RPY``            ``"0 0 0"``             Any RPY
``CPR_LASER_IP``             ``192.168.131.20``      Any IP
===========================  ======================  =================  ===========================

3D Lasers
----------

- Velodyne VLP-16
- Velodyne HDL-32E

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_LASER_3D``             ``0``                   ``1``
``CPR_LASER_3D_MODEL``       ``vlp16``               ``hdl32e``
``CPR_LASER_3D_PARENT``      ``base_link``           Any link
``CPR_LASER_3D_TOPIC``       ``scan``                Any topic
``CPR_LASER_3D_XYZ``         ``"0 0 0"``             Any XYZ
``CPR_LASER_3D_RPY``         ``"0 0 0"``             Any RPY
``CPR_LASER_3D_IP``          ``192.168.131.20``      Any IP
===========================  ======================  =================  ===========================

GPS
----------

- NovAtel SMART7
- Garmin 18x

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_GPS``                  ``0``                   ``1``
``CPR_GPS_MODEL``            ``smart7``              ``18x``
``CPR_GPS_PARENT``           ``base_link``           Any link
``CPR_GPS_XYZ``              ``"0 0 0"``             Any XYZ
``CPR_GPS_RPY``              ``"0 0 0"``             Any RPY
``CPR_GPS_PORT``             ``/dev/clearpath/gps``  Any port
``CPR_GPS_BAUD``             ``57600``               Any baud rate
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
``CPR_MICROSTRAIN``          ``0``                   ``1``
``CPR_MICROSTRAIN_PARENT``   ``base_link``           Any link
``CPR_MICROSTRAIN_XYZ``      ``"0 0 0"``             Any XYZ
``CPR_MICROSTRAIN_RPY``      ``"0 0 0"``             Any RPY
``CPR_MICROSTRAIN_PORT``     ``/dev/microstrain``    Any port
===========================  ======================  =================  ===========================

Cameras
----------

- Teledyne FLIR Blackfly
- Intel RealSense D400 Series
- Intel RealSense L515

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_BLACKFLY``             ``0``                   ``1``
``CPR_BLACKFLY_PARENT``      ``base_link``           Any link
``CPR_BLACKFLY_XYZ``         ``"0 0 0"``             Any XYZ
``CPR_BLACKFLY_RPY``         ``"0 0 0"``             Any RPY
``CPR_BLACKFLY_SERIAL``      ``0``                   Any serial no.
``CPR_BLACKFLY_CALIB``       ``0``                   ``1``
===========================  ======================  =================  ===========================

===========================  ======================  =================  ===========================
Environment Variables        Default Values          Other Values       Description
===========================  ======================  =================  ===========================
``CPR_REALSENSE``            ``0``                   ``1``
``CPR_REALSENSE_MODEL``      ``d435``                ``d435i`` 
                                                     ``d415`` 
                                                     ``d455`` 
                                                     ``l515`` 

``CPR_REALSENSE_PARENT``     ``base_link``           Any link
``CPR_REALSENSE_TOPIC``      ``realsense``           Any topic
``CPR_REALSENSE_XYZ``        ``"0 0 0"``             Any XYZ
``CPR_REALSENSE_RPY``        ``"0 0 0"``             Any RPY
===========================  ======================  =================  ===========================

Arms
-----

Coming soon!