# 加入非标准的头文件搜索路径
#INCLUDE_DIRECTORIES( /usr/include/hello  )
FIND_PATH(helloheader hello.h)
IF(helloheader)
INCLUDE_DIRECTORIES( ${helloheader}  )
ENDIF(helloheader)

# 设定可执行二进制文件的目录
SET( EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin) 

# 设定存放编译出来的库文件的目录
SET( LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib) 
ADD_EXECUTABLE(hello main.cpp)
# 为可执行文件加入库链接
TARGET_LINK_LIBRARIES( hello libhello.a)
