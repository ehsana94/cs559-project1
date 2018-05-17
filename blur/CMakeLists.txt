include_directories(${PROJECT_SOURCE_DIR}/shared/include)
add_executable(blur src/main.cpp)
target_link_libraries(blur ImageProcessing)


