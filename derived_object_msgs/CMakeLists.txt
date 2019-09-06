cmake_minimum_required(VERSION 3.5)
project(derived_object_msgs)

find_package(ament_cmake REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)
find_package(shape_msgs REQUIRED)
find_package(radar_msgs REQUIRED)

rosidl_generate_interfaces(derived_object_msgs
  "msg/CipvTrack.msg"
  "msg/LaneModels.msg"
  "msg/Lane.msg"
  "msg/ObjectArray.msg"
  "msg/Object.msg"
  "msg/ObjectWithCovarianceArray.msg"
  "msg/ObjectWithCovariance.msg"
  "msg/SolidPrimitiveWithCovariance.msg"
  DEPENDENCIES builtin_interfaces std_msgs geometry_msgs shape_msgs radar_msgs
)

ament_package()
