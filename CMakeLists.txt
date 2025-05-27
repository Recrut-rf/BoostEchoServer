cmake_minimum_required(VERSION 3.5)

project(server LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Найти пакет Boost без указания версии
find_package(Boost REQUIRED COMPONENTS system)
find_package(Threads REQUIRED)

add_executable(server main.cpp)

# Подключить библиотеку Boost
target_link_libraries(server PRIVATE Boost::system Threads::Threads)
