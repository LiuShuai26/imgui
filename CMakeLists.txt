cmake_minimum_required(VERSION 3.10)
project(imgui)

# Core ImGui sources only - backends are handled by sokol_imgui
set(IMGUI_SOURCES
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
)

add_library(imgui STATIC ${IMGUI_SOURCES})

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_compile_features(imgui PUBLIC cxx_std_11)
