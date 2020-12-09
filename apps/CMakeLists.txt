######## Build main executable ########
add_executable(${PROJECT_NAME} fast_calib.cpp)

# Set compile options and features
target_compile_options(${PROJECT_NAME} PUBLIC -g -Wall -O3)

target_link_libraries(${PROJECT_NAME} Eigen3::Eigen)

# TODO: Better alternative to include the generated project config
# (Generally do not include the header files from build directory)
target_include_directories(${PROJECT_NAME} PRIVATE ${PROJECT_BINARY_DIR})
