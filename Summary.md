# Summary

summary for project.

### app/planning integrated

combine all the components together, planner, controller, map and so on.

launch/test_now.launch is a launch file for test.

./devel/setup.zsh

roslaunch planning_integrated test_now.launch

### aux_tools

this launch a UI which can send cmd to agent by click and press w,s,a,d.

w: accelerate

s: decelerate

a: change lane to left

d: change lane to right

### core

#### common
##### lane

use OOQP to optimize the lane.

#### behavior_planner

##### MPDM_planner

- this method doesn't use DCP-Tree.
- questionable!

- this planner only assume that ego vehicle will behavior immediately. can make that plan like accelerate then cut in.

#### forward_simulator

- multimodal_forward.h
  - define that agent aggressive level.

- onlane_forward_simulation.h
  - use idm or ctx_idm to forward simulation all agent state.

#### motion_predictor

#### phy_simulator

#### route_planner

#### semantic_map_manager

### toolchain/qgis_projects

### util

#### ai agent planner

#### eudm_planner

#### ssc_planner