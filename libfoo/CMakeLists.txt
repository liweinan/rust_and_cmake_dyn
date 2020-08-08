cmake_minimum_required(VERSION 3.0)
project(LibFoo C)

add_library(foo SHARED foo.c)

install(TARGETS foo DESTINATION .)