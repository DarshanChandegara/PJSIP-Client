cmake_minimum_required(VERSION 3.20)

set(MY_Project_Name PJSIP-Client)

project(${MY_Project_Name})

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED true)

set(SOURCES src/main.cpp)
set(CMAKE_BUILD_TYPE Debug)

add_subdirectory(src)

add_executable(${MY_Project_Name} ${SOURCES})
add_executable(ReadVideoStream src/ReadVideoStream.cpp)
add_executable(StreamAudio src/StreamAudio.cpp)

target_link_libraries(${MY_Project_Name} PUBLIC SOURCE)
target_link_libraries(ReadVideoStream PUBLIC SOURCE)
target_link_libraries(StreamAudio PUBLIC SOURCE)