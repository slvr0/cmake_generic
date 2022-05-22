cmake_minimum_required(VERSION 3.10.2)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)



#replace LIB_NAME with your library names
add_library(LIB_NAME
    ../include/example_file.h
    example_file.cpp
) 




#does the library require special search paths to external includes?
#target_include_directories(LIB_NAME PRIVATE path_1 path_2)

#do you have cross-linking between your libraries? in case you need to link them
#target_link_libraries(LIB_NAME PRIVATE OTHER_LIB_NAME ${PREDEF_LIBNAME})