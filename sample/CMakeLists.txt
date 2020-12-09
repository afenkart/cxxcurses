
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}/bin")

set(SOURCE_FILES main.cpp)

add_executable(cxxcurses_sample ${SOURCE_FILES})
target_link_libraries(cxxcurses_sample PRIVATE cxxcurses)
target_compile_features(cxxcurses_sample INTERFACE cxx_std_17)

target_include_directories(cxxcurses_sample
  PRIVATE
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/../include>
    $<INSTALL_INTERFACE:include/${PROJECT_NAME}>
  )
