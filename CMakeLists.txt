cmake_minimum_required(VERSION 3.16)

set(CMAKE_CXX_STANDARD 23)

project(SDL-WINDOW VERSION 1.0.0)

add_executable(SDL-WINDOW main.cpp)

# Variables storing SDL framework locations
set(SDL2
  /Library/Frameworks/SDL2.framework)
set(SDL2_image
  /Library/Frameworks/SDL2_image.framework)
set(SDL2_ttf
  /Library/Frameworks/SDL2_ttf.framework)

target_link_libraries(
  SDL-WINDOW PRIVATE
  ${SDL2}/Versions/A/SDL2
  ${SDL2_image}/Versions/A/SDL2_image
  ${SDL2_ttf}/Versions/A/SDL2_ttf
)

target_include_directories(
  SDL-WINDOW PRIVATE
  ${SDL2}/Versions/A/Headers
  ${SDL2_image}/Versions/A/Headers
  ${SDL2_ttf}/Versions/A/Headers
)