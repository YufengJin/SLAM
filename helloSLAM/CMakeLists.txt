# 声明要求的 cmake 最低版本
cmake_minimum_required( VERSION 2.8 )

# 声明一个 cmake 工程
project( helloSLAM )

# 设置编译模式
set( CMAKE_BUILD_TYPE "Debug" )

# 添加一个可执行程序
# 语法：add_executable( 程序名 源代码文件 ）
add_subdirectory(lib)

# 查找目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)


add_executable( helloSLAM ${DIR_SRCS})
# 将库文件链接到可执行程序上
target_link_libraries( helloSLAM PrintFunction )
