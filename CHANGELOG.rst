^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package scitos_2d_navigation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.6 (2014-12-17)
------------------
* Merge pull request `#53 <https://github.com/strands-project/scitos_2d_navigation/issues/53>`_ from bfalacerda/hydro-devel
  same params as the new strands_movebase. merging
* mirroring strands movebase params where possible
* new nav params
* Merge pull request `#52 <https://github.com/strands-project/scitos_2d_navigation/issues/52>`_ from BFALacerda/hydro-devel
  getting config of common costmap params to mirror strands_movebase
* removing params that arent used
* getting config of common costmap params to mirror strands_movebase
* Contributors: BFALacerda, Bruno Lacerda, bfalacerda

0.0.5 (2014-11-09)
------------------
* Merge pull request `#51 <https://github.com/strands-project/scitos_2d_navigation/issues/51>`_ from Jailander/hydro-devel
  final and tested version of loader
* final and tested version of loader
* Merge pull request `#50 <https://github.com/strands-project/scitos_2d_navigation/issues/50>`_ from Jailander/hydro-devel
  latest machine tag versions
* latest machine tag versions
* Merge pull request `#49 <https://github.com/strands-project/scitos_2d_navigation/issues/49>`_ from nilsbore/hydro-devel2
  Added amcl as a run dependency
* Added amcl as a run dependency
* Contributors: Jaime Pulido Fentanes, Marc Hanheide, Nils Bore

0.0.4 (2014-10-23)
------------------
* Merge branch 'release_cleanup2' of https://github.com/nilsbore/scitos_2d_navigation into nilsbore-release_cleanup2
  Conflicts:
  launch/move_base_3d.launch
  scitos_move_base_params_3d/costmap_common_params.yaml
  scitos_move_base_params_3d/local_costmap_params.yaml
  src/remove_edges_cloud.cpp
* Merge branch 'hydro-devel' of https://github.com/strands-project/scitos_2d_navigation into hydro-devel
* Merge pull request `#40 <https://github.com/strands-project/scitos_2d_navigation/issues/40>`_ from nilsbore/newtry
  This adds an extra obstacle layer in the local costmap that can be used for backtracking
* Changed to only depend on move_base in package.xml as well
* Removed unnecessary dependencies, now only relying on move_base.
* Merge remote-tracking branch 'upstream/hydro-devel' into release_cleanup2
* Removed the build configuration from the Cmake file
* Removed the stuff that is now in strands_movebase
* Forgot to remove the cliff sensor, which is not there anymore
* Changed some thresholds mostly
* Removed cliff detection from the head sensor since this can cause problems
* Forgot to remove the sensor inputs from the normal obstacle layer
* Only having head observations in one layer now
* Changed the maximum height of obstacles added from head so that they can be cleared from chest sensor
* Merged the latest changes
* Merge remote-tracking branch 'upstream/hydro-devel' into hydro-devel
* Added the head sensor the be activated when needed
* Added the sensors to the planning
* Changed heights of head sensor
* Added the head sensor that will be publishing only when the robot gets stuck
* Contributors: Marc Hanheide, Nils Bore, Rares Ambrus, strands

0.0.3 (2014-10-23)
------------------
* Merge pull request `#46 <https://github.com/strands-project/scitos_2d_navigation/issues/46>`_ from strands-project/install_targets
  added install targets to work towards `#43 <https://github.com/strands-project/scitos_2d_navigation/issues/43>`_
* added install targets to work towards `#43 <https://github.com/strands-project/scitos_2d_navigation/issues/43>`_
* Merge pull request `#45 <https://github.com/strands-project/scitos_2d_navigation/issues/45>`_ from Jailander/hydro-devel
  setting ~use_map_topic parameter
* setting ~use_map_topic parameter this commit solves `#44 <https://github.com/strands-project/scitos_2d_navigation/issues/44>`_
* Merge pull request `#42 <https://github.com/strands-project/scitos_2d_navigation/issues/42>`_ from Jailander/hydro-devel
  bug fix
* bug fix
* Merge pull request `#41 <https://github.com/strands-project/scitos_2d_navigation/issues/41>`_ from Jailander/hydro-devel
  adding remapping for cmd_vel_mux
* adding remapping for cmd_vel_mux
* Merge pull request `#39 <https://github.com/strands-project/scitos_2d_navigation/issues/39>`_ from Jailander/hydro-devel
  Adding camera_ip arg so 3D obstacle avoidance can run on a different PC
* Adding camera_ip argument so 3D obstacle avoidance can run on a different PC
* Merge pull request `#38 <https://github.com/strands-project/scitos_2d_navigation/issues/38>`_ from Jailander/hydro-devel
  Adding Machine tags to launch files
* Adding Machine tags to launch files
* Merge pull request `#37 <https://github.com/strands-project/scitos_2d_navigation/issues/37>`_ from nilsbore/cliff
  Changed stuff in the cliff detection to remove printouts and make it cleaner. I'm merging this since it's a simple one.
* Restoring publishing frequency, I'll try it out later
* Small changes
* Only looking for the transform after getting the cloud now
* Increased the frequency of the obstacle avoidance cloud
* Merge pull request `#36 <https://github.com/strands-project/scitos_2d_navigation/issues/36>`_ from nilsbore/cliff
  This adds a cliff sensor to the 2d navigation stack with camera. Test.
* Fixed a potential bug where the subsampled pointclouds don't get the timestamp
* Added some comments and configurability
* Forgot to add the camera frame parameter
* Added cliff points to move_base
* Detecting negative points
* Got the transforms working
* Added first version of node that looks up camera transform and mirros negative points towards camera
* Merge pull request `#35 <https://github.com/strands-project/scitos_2d_navigation/issues/35>`_ from nilsbore/hydro-devel
  Add an optional no-go static layer to the layered costmap
* Added a no-go map to the 3d obstacle avoidance as well
* getting no go map to work
* Added no-go map layer
* Merge remote-tracking branch 'upstream/hydro-devel' into hydro-devel
* Merge pull request `#33 <https://github.com/strands-project/scitos_2d_navigation/issues/33>`_ from BFALacerda/hydro-devel
  adding layered costmaps to costmap parameters files
* adding layered costmaps to costmap parameters files
* Merge branch 'hydro-devel' of https://github.com/strands-project/scitos_2d_navigation into hydro-devel
* Added some dependencies in the package.xml, shouldn't make any difference
* Merge pull request `#32 <https://github.com/strands-project/scitos_2d_navigation/issues/32>`_ from nilsbore/hydro-devel
  Made changes to make the chest camera processing nodes work with hydro, pcl 1.7
* Set the unknown threshold back to 6, may change again later
* Tidied up the code a bit
* Merge branch 'hydro-devel' of https://github.com/nilsbore/scitos_2d_navigation into hydro-devel
* Changed stuff to work with new hydro pcl, removed unnecessary stuff
* Merge pull request `#27 <https://github.com/strands-project/scitos_2d_navigation/issues/27>`_ from BFALacerda/master
  trying to avoid planning through walls bug
* trying to avoid planning through walls bug
* Added the new footprint as a comment
* Changed the unknown threshold from the default value since it seems unreasonable, dont think it makes any difference since it would work very poorly if this was taken into consideration
* Changed the raytrace range to be longer
* Plugged a memory leak. (history_ never deleted.)
* Update README.md
* Update README.md
* Update README.md
* Merge pull request `#16 <https://github.com/strands-project/scitos_2d_navigation/issues/16>`_ from nilsbore/master
  Added optional 3d obstacle avoidance to scitos_2d_navigation. We've been running for a week and seems to work. The downsampling of the cloud takes quite a lot of cpu (about 30% of one cpu) but I can't think of any faster way to do it (approximate voxel grid atm, ideas?). This is dependent on merged pull request https://github.com/strands-project/scitos_common/pull/26 since we need good estimate of chest camera height and angle with respect to floor. Also made the costmap update at 3 hz instead of 5 to make sure it would always complete on time. Needs more testing with people around. As mentioned, with previous usage this won't make any difference.
* Changed update rates of costmaps and allowed smaller distances for obstacle adding
* Added a few comments
* Added some improvements that should make the planner work at a better rate
* Forgot to remove launch of clearing wall node
* Removed clearing wall since it shouldn't be needed any more, changed cutoffs to be less generous
* Merge branch 'master' of https://github.com/nilsbore/scitos_2d_navigation
* Merge remote-tracking branch 'upstream/master'
* Fixed bug where I accidentally exchanged clearing and obstacle cloud
* Added brunos change to disallow rotation in move_base_3d
* Merge remote-tracking branch 'upstream/master'
* Merge pull request `#15 <https://github.com/strands-project/scitos_2d_navigation/issues/15>`_ from BFALacerda/master
  disallowing rotate recovery
* Moved to using correct camera frame since Rares fixed his code
* Added possibility to don't add obstacles too close to the camera
* Commented move_base_3d launch file
* Made it possible to change camera topic and changed clear_sensor to use the cloud with removed edges, missed that before
* Commented some source files
* Stupid tabs
* Changed to have two different move_base files for with and without camera, switched by using argument with_camera parameter to scitos_2d_nav
* Ros apparently only handles double params
* Made camera topics and desired cutoff of point cloud configurable in move_base launch file
* Added node for removing edges of cloud
* Using more robust filtering parameters, will be heavy on robot
* Added voxel_grid variant that doesn't add voxel if too few points are in there
* disallowing rotate recovery
* more filters for the subsampling, homework for the weekend
* Added depth camera to obstacle avoidance, node for subsampling the cloud to make the ray tracing feasible
* Merge pull request `#10 <https://github.com/strands-project/scitos_2d_navigation/issues/10>`_ from BFALacerda/master
  new parameters
* new parameters for dwa planner
* Changed parameters, most of them to default values
* Merge pull request `#8 <https://github.com/strands-project/scitos_2d_navigation/issues/8>`_ from BFALacerda/master
  changed file structure
* Edited yaml files because of identation problem
* Merge branch 'master' of https://github.com/BFALacerda/scitos_2d_navigation into meu
* changed launch file to get configuration
* changed file structure
* Merge pull request `#7 <https://github.com/strands-project/scitos_2d_navigation/issues/7>`_ from BFALacerda/master
  changed parameters to improve navigation
* changed parameters to improve navigation
* Merge pull request `#5 <https://github.com/strands-project/scitos_2d_navigation/issues/5>`_ from nilsbore/master
  Changed name of maps directory to example_maps and added map as argument to launch file
* Merge remote-tracking branch 'upstream/master'
* Changed maps to example_maps and passed the map as map parameter to scitos_2d_nav.launch
* Merge pull request `#4 <https://github.com/strands-project/scitos_2d_navigation/issues/4>`_ from nilsbore/master
  Separate move_base from navigation launch file, rename nav.launch to scitos_2d_nav.launch
* Separated out move base from the nav launch file, renamed the nav.launch file
* Merge pull request `#2 <https://github.com/strands-project/scitos_2d_navigation/issues/2>`_ from kunzel/master
  Individual launch file for AMCL
* isolated amcl from launch file in order to include it anywhere, eg in the simulation
* Merge pull request `#1 <https://github.com/strands-project/scitos_2d_navigation/issues/1>`_ from nilsbore/master
  New package scitos_2d_navigation, this basically just moves our stuff from 3d_mapping to the new structure.
* Update README.md
* Update README.md
* Added move base params and changed package path in nav.launch
* Added a new package scitos_2d_navigation_config for the move base params
* Added dummy maps to be able to run at all.
* Initialized repo as catkin package, added base launch file, will need modification
* Initial commit with the nav launch file, will change path to move base
* Initial commit
* Contributors: BFALacerda, Bruno Lacerda, Jaime Pulido Fentanes, Lars Kunze, Marc Hanheide, Nick Hawes, Nils Bore, lucasb-eyer
