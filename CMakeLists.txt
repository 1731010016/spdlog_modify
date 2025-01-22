# 指定CMake版本
 cmake_minimum_required(VERSION 3.10) 
  # 指定项目名称 
project(spdlog_modify)  
 # 设置C++标准
set(CMAKE_CXX_STANDARD 14)


# 添加子模块路径
add_subdirectory(3rdparty/spdlog)


# 添加源文件
add_executable(spdlog_modify "src/main.cpp")
# 链接 spdlog 库
#target_link_libraries(spdlog_modify PRIVATE spdlog::spdlog)

target_link_libraries(spdlog_modify PRIVATE spdlog::spdlog_header_only)