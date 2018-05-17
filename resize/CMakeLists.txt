include_directories(${PROJECT_SOURCE_DIR}/shared/include)
add_executable(resizer src/main.cpp)
target_link_libraries(resizer ImageProcessing)


