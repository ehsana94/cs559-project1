include_directories(include)

add_library(TargaImage src/TargaImage.cpp)
add_library(libtarga src/libtarga.cpp)
add_library(ImageProcessing src/ImageProcessing.cpp)

target_link_libraries(TargaImage libtarga) 
target_link_libraries(ImageProcessing libtarga TargaImage) 


