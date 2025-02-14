include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
include_directories(${PROJECT_SOURCE_DIR}/modules/A1/include)

aux_source_directory(src SRC)
add_library(m1 ${SRC})

target_include_directories(m1 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_link_libraries(
    m1
    
    a1
    a2
    m2
    kalman
    math
    ${OpenCV_LIBS}
)