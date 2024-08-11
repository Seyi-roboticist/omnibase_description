cmake_minimum_required(VERSION 3.8)
project(omnibase_description)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(xacro REQUIRED)
find_package(rclcpp REQUIRED)
find_package(rclpy REQUIRED)
find_package(std_msgs REQUIRED)


# Install
install(
	DIRECTORY launch meshes urdf xacro
	DESTINATION share/${PROJECT_NAME}
)

ament_package()