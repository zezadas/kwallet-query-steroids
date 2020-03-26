#remove_definitions(-DQT_NO_CAST_FROM_ASCII)

set(CMAKE_AUTOMOC ON)

project(kwallet-query-steroids)

set(PROJECT_VERSION "5.18.80")

cmake_minimum_required(VERSION 3.10)


add_executable(kwallet-query-steroids main.cpp querydriver.cpp)

target_sources(kwallet-query-steroids PRIVATE)

find_package(Qt5 CONFIG REQUIRED COMPONENTS Widgets)
find_package(KF5CoreAddons)
find_package(KF5I18n)
find_package(KF5Wallet)

TARGET_LINK_LIBRARIES(kwallet-query-steroids
    KF5::Wallet
    KF5::CoreAddons
    KF5::I18n
    Qt5::Widgets
)
