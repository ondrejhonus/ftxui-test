cmake_minimum_required(VERSION 3.10.0)
project(ftxui-test VERSION 0.1.0 LANGUAGES C CXX)

include(FetchContent)
FetchContent_Declare(ftxui
  GIT_REPOSITORY https://github.com/ArthurSonzogni/FTXUI
  GIT_TAG v5.0.0
)
FetchContent_MakeAvailable(ftxui)

add_executable(ftxui-test src/main.cpp)
target_link_libraries(ftxui-test PRIVATE ftxui::screen ftxui::dom ftxui::component)

