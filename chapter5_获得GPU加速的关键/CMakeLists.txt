cmake_minimum_required(VERSION 3.30)
project(add2gpu_test LANGUAGES CXX CUDA)

# 添加可执行文件
add_executable(add2gpu add2gpu.cu)

# 设置 CUDA 编译选项
target_compile_options(add2gpu PRIVATE "$<$<COMPILE_LANGUAGE:CUDA>:--allow-unsupported-compiler>")

# 设置 C++ 标准（如果混编 CUDA/C++）
set_target_properties(add2gpu PROPERTIES
    CXX_STANDARD 14
    CXX_STANDARD_REQUIRED ON
)