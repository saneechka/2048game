cmake_minimum_required(VERSION 3.1.0)

project(2048)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt5Widgets REQUIRED)

set(SOURCES
    main.cpp
    gui/mainwindow.cpp
    core/tile.cpp
    core/board.cpp
    core/game.cpp
    gui/qgameboard.cpp
    gui/qtile.cpp
    gui/qresetbutton.cpp
    core/observer.cpp
    core/subject.cpp
    gui/qgameoverwindow.cpp
)

set(HEADERS
    gui/mainwindow.h
    core/tile.h
    core/board.h
    core/game.h
    gui/qgameboard.h
    gui/qtile.h
    gui/qresetbutton.h
    core/observer.h
    core/subject.h
    gui/qgameoverwindow.h
    gui/qwinwindow.h
)

add_executable(${PROJECT_NAME} ${SOURCES} ${HEADERS})
target_link_libraries(${PROJECT_NAME} Qt5::Widgets)
