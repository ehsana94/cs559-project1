#find_package(Curses REQUIRED)


include_directories(include)
include_directories(${PROJECT_SOURCE_DIR}/shared/include)
#include_directories(${CURSES_INCLUDE_DIR})

add_library(ImagePainting src/ImagePainting.cpp)
target_link_libraries(ImagePainting ImageProcessing) 

add_executable(main src/main.cpp)

target_link_libraries(main ImagePainting )
#target_link_libraries(main ${CURSES_LIBRARIES})  


add_custom_command(TARGET main PRE_BUILD
                   COMMAND ${CMAKE_COMMAND} -E copy_directory
                       ${CMAKE_CURRENT_SOURCE_DIR}/brushes $<TARGET_FILE_DIR:main>/brushes)
