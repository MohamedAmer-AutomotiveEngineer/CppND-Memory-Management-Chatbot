cmake_minimum_required(VERSION 3.11.3)

set(CMAKE_CXX_STANDARD 17)
SET(wxWidgets_ROOT_DIR "C:/wxWidgets-3.1.4")
SET(wxWidgets_LIB_DIR "C:/wxWidgets-3.1.4/build/lib/vc_x64_dll")
SET(wxWidgets_LIBRARIES "C:/wxWidgets-3.1.4/lib")
SET(wxWidgets_INCLUDE_DIRS "C:/wxWidgets-3.1.4/include/wx")

set(wxWidgets_INCLUDE_DIRS "C:/wxWidgets-3.1.4/include")
set(wxWidgets_LIBRARIES "C:/wxWidgets-3.1.4/build/lib/vc_x64_dll")

project(Membot)

find_package(wxWidgets REQUIRED COMPONENTS core base)
include(${wxWidgets_USE_FILE})

file(GLOB project_SRCS src/*.cpp)

add_executable(membot ${project_SRCS})
target_link_libraries(membot ${wxWidgets_LIBRARIES})
target_include_directories(membot PRIVATE ${wxWidgets_INCLUDE_DIRS})
