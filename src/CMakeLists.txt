cmake_minimum_required(VERSION 3.27)
project(executable)

add_subdirectory(battery)

add_executable(executable main.cpp)
target_link_libraries(executable battery)
install(TARGETS executable DESTINATION ${OXYGEN_INSTALL_BIN_DIR})
