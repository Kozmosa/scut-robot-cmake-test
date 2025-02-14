include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

aux_source_directory(src SRC)
add_library(a1 ${SRC})

target_include_directories(a1 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_link_libraries(
    a1
    
    a2
    m1
    m2
    kalman
    math
    ${OpenCV_LIBS}
)