
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}/bin")

set(SOURCE_FILES main.cpp)

add_executable(cxxcurses_sample ${SOURCE_FILES})
target_link_libraries(cxxcurses_sample PRIVATE cxxcurses)
