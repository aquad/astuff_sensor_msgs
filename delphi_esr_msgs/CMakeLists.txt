cmake_minimum_required(VERSION 3.5)
project(delphi_esr_msgs)

if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

find_package(ament_cmake REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)

rosidl_generate_interfaces(delphi_esr_msgs
  "msg/EsrEthTx.msg"
  # can Tx
  "msg/EsrStatus1.msg"
  "msg/EsrStatus2.msg"
  "msg/EsrStatus3.msg"
  "msg/EsrStatus4.msg"
  "msg/EsrStatus5.msg"
  "msg/EsrStatus6.msg"
  "msg/EsrStatus7.msg"
  "msg/EsrStatus8.msg"
  "msg/EsrStatus9.msg"
  "msg/EsrValid1.msg"
  "msg/EsrValid2.msg"
  "msg/EsrTrack.msg"
  "msg/EsrTrackMotionPower.msg"
  "msg/TrackMotionPower.msg"
  # can Rx
  "msg/EsrVehicle1.msg"
  "msg/EsrVehicle2.msg"
  "msg/EsrVehicle3.msg"
  "msg/EsrVehicle4.msg"
  "msg/EsrVehicle5.msg"
  DEPENDENCIES builtin_interfaces std_msgs
)

ament_package()
