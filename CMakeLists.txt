cmake_minimum_required(VERSION 3.1.0)

project(2048)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt5Widgets REQUIRED)

set(SOURCES
    main.cpp
    ui/mainwindow.cpp
    realization/tile.cpp
    realization/board.cpp
    realization/game.cpp
    ui/qgameboard.cpp
    ui/qtile.cpp
    ui/qresetbutton.cpp
    realization/observer.cpp
    realization/subject.cpp
    ui/qgameoverwindow.cpp
)

set(HEADERS
    ui/mainwindow.h
    realization/tile.h
    realization/board.h
    realization/game.h
    ui/qgameboard.h
    ui/qtile.h
    ui/qresetbutton.h
    realization/observer.h
    realization/subject.h
    ui/qgameoverwindow.h
    ui/qwinwindow.h
)

add_executable(${PROJECT_NAME} ${SOURCES} ${HEADERS})
target_link_libraries(${PROJECT_NAME} Qt5::Widgets)
