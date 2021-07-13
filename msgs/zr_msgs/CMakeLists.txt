cmake_minimum_required(VERSION 2.8.3)
project(zr_msgs)

find_package(catkin REQUIRED COMPONENTS
	message_generation
	std_msgs
	geometry_msgs
)


## Generate messages in the 'msg' folder
add_message_files(
  FILES
  goal_info.msg
  external_action.msg
  lift_status.msg
  robot_status.msg
  locker_info.msg
  motor_info.msg
  battery_info.msg
  gps_anchor.msg
  gps_anchor_array.msg
  occupancy_rate.msg
  arrive.msg
  Point_id.msg
  Ev_param.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS
  message_runtime
  std_msgs
  geometry_msgs
)
