^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package robot_pose_ekf
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.14.4 (2018-06-19)
-------------------
* Merge pull request `#713 <https://github.com/ros-planning/navigation/issues/713>`_ from garethellis0/kinetic-devel
  Added handling for NaN linear.z components of GPS in `robot_pose_ekf`
  Added a check in `odom_estimation_node.cpp` that checks if `linear.z`
  values in the GPS `odom` message are `NaN` (something common in such
  messages), and if so, sets it to 0, and sets the corresponding variance
  to a very high value so we ignore it.
* Contributors: Gareth Ellis, Michael Ferguson

1.14.3 (2018-03-16)
-------------------
* Merge pull request `#672 <https://github.com/ros-planning/navigation/issues/672>`_ from ros-planning/email_update_kinetic
  update maintainer email (kinetic)
* Fixes `#313 <https://github.com/ros-planning/navigation/issues/313>`_ (kinetic) (`#654 <https://github.com/ros-planning/navigation/issues/654>`_)
* Merge pull request `#648 <https://github.com/ros-planning/navigation/issues/648>`_ from aaronhoy/kinetic_add_ahoy
  Add myself as a maintainer.
* added message_generation to build deps to prevent failing generation of GetStatus, MakeNavPlan and SetCostmap (`#640 <https://github.com/ros-planning/navigation/issues/640>`_)
* Contributors: Aaron Hoy, David V. Lu!!, Leroy Rügemer, Michael Ferguson

1.14.2 (2017-08-14)
-------------------

1.14.1 (2017-08-07)
-------------------
* Fix CMakeLists + package.xmls (`#548 <https://github.com/ros-planning/navigation/issues/548>`_)
* Initialization of filter with GPS and odometry.
* Contributors: Martin Günther, Vincent Rabaud, azaganidis

1.14.0 (2016-05-20)
-------------------
* add to install script/ directory
* add execute bit to scripts/wtf.py
* robot_pose_ekf/src/odom_estimation_node.cpp: add to print gps sensor and used/not used in getStatus
* Contributors: Kei Okada

1.13.1 (2015-10-29)
-------------------

1.13.0 (2015-03-17)
-------------------

1.12.0 (2015-02-04)
-------------------
* update maintainer email
* Contributors: Michael Ferguson

1.11.15 (2015-02-03)
--------------------
* Fix bfl includes in robot_pose_ekf
* Contributors: Jochen Sprickerhof

1.11.14 (2014-12-05)
--------------------

1.11.13 (2014-10-02)
--------------------

1.11.12 (2014-10-01)
--------------------
* Fix EKF topic name so that it is unaffected by tf_prefix
* Install launch files, closes `#249 <https://github.com/ros-planning/navigation/issues/249>`_
* Fixed hardcoded tf frames issue by fetching base_footprint_frame_ value from param server and using it in OdomEstimation filter
* Fixed hardcoded tf frames issue by adding variables for output and base_footprint frames along with mutator methods
* Contributors: Jochen Sprickerhof, Michael Ferguson, Murilo FM

1.11.11 (2014-07-23)
--------------------

1.11.10 (2014-06-25)
--------------------

1.11.9 (2014-06-10)
-------------------
* fix robot_pose_ekf test
* Contributors: Michael Ferguson

1.11.8 (2014-05-21)
-------------------
* fix build, was broken by `#175 <https://github.com/ros-planning/navigation/issues/175>`_
* Contributors: Michael Ferguson

1.11.7 (2014-05-21)
-------------------
* Even longer Time limit for EKF Test
* make rostest in CMakeLists optional
* Contributors: David Lu!!, Lukas Bulwahn

1.11.5 (2014-01-30)
-------------------
* check for CATKIN_ENABLE_TESTING
* Download test data from download.ros.org instead of willow
* Change maintainer from Hersh to Lu

1.11.4 (2013-09-27)
-------------------
* Package URL Updates
* upgrade depracated download data calls.
* use tf_prefix to lookup and send transforms
