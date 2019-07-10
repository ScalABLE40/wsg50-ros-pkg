cmake_minimum_required(VERSION 2.8.3)
project(wsg_50_common)

find_package(catkin REQUIRED COMPONENTS
  message_generation
)

add_message_files(FILES Cmd.msg Status.msg)

add_service_files(FILES Conf.srv Incr.srv Move.srv)

generate_messages()

catkin_package(
  CATKIN_DEPENDS message_runtime 
)