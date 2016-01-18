cmake_minimum_required(VERSION 2.8)
find_package( OpenCV REQUIRED )

set(CMAKE_CXX_FLAGS "--std=c++11 ${CMAKE_CXX_FLAGS}")
set(CMAKE_CXX_FLAGS_RELEASE "-O2")
set(CMAKE_CXX_FLAGS_DEBUG  "-O0 -g")

set(source ./FaceAlignment.h ./FernCascade.cpp ./Fern.cpp ./ShapeRegressor.cpp ./Utils.cpp ./TrainDemo.cpp)
add_executable(TrainDemo.out ${source})
target_link_libraries(TrainDemo.out ${OpenCV_LIBS})

set(source ./FaceAlignment.h ./FernCascade.cpp ./Fern.cpp ./ShapeRegressor.cpp ./Utils.cpp ./TestDemo.cpp)
add_executable(TestDemo.out ${source})
target_link_libraries(TestDemo.out ${OpenCV_LIBS})


