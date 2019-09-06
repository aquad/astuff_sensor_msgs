cmake_minimum_required(VERSION 3.5)
project(radar_msgs)

find_package(ament_cmake REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)

rosidl_generate_interfaces(radar_msgs
  "msg/RadarDetection.msg"
  "msg/RadarDetectionStamped.msg"
  "msg/RadarDetectionArray.msg"
  "msg/RadarTrack.msg"
  "msg/RadarTrackStamped.msg"
  "msg/RadarTrackArray.msg"
  # high level Tx
  "msg/RadarStatus.msg"
  "msg/RadarErrorStatus.msg"
  DEPENDENCIES builtin_interfaces std_msgs geometry_msgs
)

ament_package()
