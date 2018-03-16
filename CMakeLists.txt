cmake_minimum_required(VERSION 3.9)
project(crowhelloworld)
include_directories(/home/justin/git/crow/include)

set(CMAKE_CXX_STANDARD 11)

add_executable(crowhelloworld main.cpp)
find_library(LIBBOOST libboost HINTS /usr/lib/x86_64-linux-gnu/)
find_library(PTHREAD pthread HINTS /usr/lib/x86_64-linux-gnu/)
target_link_libraries(crowhelloworld ${LIBBOOST} ${PTHREAD})


