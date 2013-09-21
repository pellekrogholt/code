cmake_minimum_required (VERSION 2.6) 

PROJECT(Cartoonifier_Desktop)

# debug or relase:
set(CMAKE_BUILD_TYPE Debug)
#set(CMAKE_BUILD_TYPE Release)


# Requires OpenCV
FIND_PACKAGE( OpenCV REQUIRED )

SET(SRC
    main_desktop.cpp
    cartoon.cpp
    ImageUtils_0.7.cpp
)

ADD_EXECUTABLE( ${PROJECT_NAME} ${SRC} )
TARGET_LINK_LIBRARIES( ${PROJECT_NAME}  ${OpenCV_LIBS} )
