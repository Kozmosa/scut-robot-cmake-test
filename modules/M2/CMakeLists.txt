include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
include_directories(${PROJECT_SOURCE_DIR}/common/kalman/include)

aux_source_directory(src SRC)
add_library(m2 ${SRC})

target_include_directories(m2 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_link_libraries(
    m2
    
    a1
    a2
    m1
    kalman
    math
    ${OpenCV_LIBS}
)