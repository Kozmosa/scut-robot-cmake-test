file(GLOB COMMON_MATH_SOURCES "src/*.cpp")
add_library(math
    ${COMMON_MATH_SOURCES}
)

target_include_directories(math
    PUBLIC
    include
)

find_package(OpenCV REQUIRED)
if(OpenCV_FOUND)
  include_directories(${OpenCV_INCLUDE_DIRS})
endif()

target_link_libraries(math
    PUBLIC
    ${OpenCV_LIBS}
)