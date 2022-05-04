cmake_minimum_required(VERSION 3.5)
project(hri_msgs)

# Default to C99
if(NOT CMAKE_C_STANDARD)
  set(CMAKE_C_STANDARD 99)
endif()

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(std_msgs REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/SoftBiometrics.msg"
  "msg/BodyPosture.msg"
  "msg/Gesture.msg"
  "msg/Expression.msg"
  "msg/FacialActionUnits.msg"
  "msg/FacialLandmarks.msg"
  "msg/Gaze.msg"
  "msg/Group.msg"
  "msg/Skeleton2D.msg"
  "msg/PointOfInterest2D.msg"
  "msg/IdsList.msg"
  "msg/IdsMatch.msg"

  DEPENDENCIES std_msgs
)


ament_package()