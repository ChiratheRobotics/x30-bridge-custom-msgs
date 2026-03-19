cmake_minimum_required(VERSION 3.5)
project(message_transformer_cpp)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/BatteryData.msg"
)

ament_package()
