cmake_minimum_required(VERSION 3.10)
project(CasinoNumberGuessingGame)

set(CMAKE_CXX_STANDARD 14)

include_directories(src)

add_executable(casino_game src/main.cpp src/game.cpp src/player.cpp)

add_executable(test_game tests/test_game.cpp src/game.cpp src/player.cpp)

# # 新增：检查二进制文件
# set(REQUIRED_BINARY "${CMAKE_SOURCE_DIR}/resources/required_binary.bin")

# if(NOT EXISTS ${REQUIRED_BINARY})
#     message(FATAL_ERROR "Required binary file ${REQUIRED_BINARY} not found. Please ensure it is placed in the resources/ directory.")
# endif()

# # 可选：将二进制文件复制到构建目录
# file(COPY ${REQUIRED_BINARY} DESTINATION ${CMAKE_BINARY_DIR}/resources)