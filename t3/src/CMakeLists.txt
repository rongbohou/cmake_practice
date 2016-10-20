ADD_LIBRARY( hello SHARED hello.cpp )
ADD_LIBRARY( hello_static hello.cpp )
# 添加动态库版本号
SET_TARGET_PROPERTIES(hello PROPERTIES VERSION 1.2 SOVERSION 1)

SET_TARGET_PROPERTIES(hello_static PROPERTIES OUTPUT_NAME "hello")
GET_TARGET_PROPERTY(OUTPUT_VALUE hello_static OUTPUT_NAME)
MESSAGE(STATUS "THIS IS THE hello_static OUTPUT_NAME:" ${OUTPUT_VALUE})

# 安装共享库和头文件        
INSTALL(FILES hello.h DESTINATION include/hello)
INSTALL(TARGETS hello hello_static
         LIBRARY DESTINATION lib
         ARCHIVE DESTINATION lib)
# 删除安装共享库和头文件        
#UNINSTALL(FILES hello.h DESTINATION include/hello)
#UNINSTALL(TARGETS hello   LIBRARY DESTINATION lib)
       
