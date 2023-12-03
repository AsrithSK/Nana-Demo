cmake_minimum_required(VERSION 3.10)

project(nana_demo)

add_executable(nana_Demo src/main.cpp)

set(NANA_INCLUDE_DIR include/)
set(NANA_LIB_DIR lib/)

message(STATUS "Nana library path: ${NANA_LIB_DIR}")

# set include directory
target_include_directories(nana_Demo PUBLIC "${NANA_INCLUDE_DIR}")


# set library directory
target_link_directories(nana_Demo PUBLIC "${NANA_LIB_DIR}")
target_link_libraries(nana_Demo nana gdi32 comdlg32 libz)


