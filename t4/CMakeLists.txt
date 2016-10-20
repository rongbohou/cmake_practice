PROJECT(HELLO)

#增加子文件夹,ADD_SUBDIRECTORY( source_dir binary_dir), source_dir 当前工程的源文件，binary_dir 为中间二进制和目标二进制存放位置 下指令的lib在 /build/lib

ADD_SUBDIRECTORY( ${PROJECT_SOURCE_DIR}/src lib)




