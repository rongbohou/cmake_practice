
#设定可执行二进制文件的目录
SET( EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin) 

#设定存放编译出来的库文件的目录
SET( LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib) 
ADD_EXECUTABLE(hello main.cpp)

# 简化版
#PROJECT(HELLO)
#ADD_EXECUTABLE(main main.cpp)

