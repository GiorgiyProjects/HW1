cmake_minimum_required(VERSION 3.2)


if(DEFINED ENV{GITHUB_RUN_NUMBER})
    message("build $ENV{GITHUB_RUN_NUMBER}")
    project(hello VERSION 0.0.$ENV{GITHUB_RUN_NUMBER})
else()
    project(hello)
endif()

find_package(Boost COMPONENTS unit_test_framework REQUIRED)

add_executable(hello main.cpp)
