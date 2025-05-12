cmake_minimum_required(VERSION 3.10)
project(CasinoNumberGuessingGame)

set(CMAKE_CXX_STANDARD 14)

include_directories(src)

add_executable(casino_game src/main.cpp src/game.cpp src/player.cpp)

add_executable(test_game tests/test_game.cpp src/game.cpp src/player.cpp)
 

# 假设 casino_game 是一个可执行文件
install(TARGETS casino_game
        RUNTIME DESTINATION bin)


# 如果你还有头文件
install(FILES ${CMAKE_SOURCE_DIR}/src/res.h
        DESTINATION include)