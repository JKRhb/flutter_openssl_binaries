cmake_minimum_required(VERSION 3.10)

# Project-level configuration.
set(PROJECT_NAME "flutter_openssl_binaries")
project(${PROJECT_NAME} LANGUAGES CXX)

# This value is used when generating builds using this plugin, so it must not be
# changed.
set(PLUGIN_NAME "flutter_openssl_binaries_plugin")

# Define the plugin library target. Its name must not be changed (see comment on
# PLUGIN_NAME above).
add_library(${PLUGIN_NAME} SHARED)

apply_standard_settings(${PLUGIN_NAME})

set_target_properties(${PLUGIN_NAME} PROPERTIES CXX_VISIBILITY_PRESET hidden)
target_compile_definitions(${PLUGIN_NAME} PRIVATE FLUTTER_PLUGIN_IMPL)

target_link_libraries(${PLUGIN_NAME} PRIVATE flutter)
target_link_libraries(${PLUGIN_NAME} PRIVATE PkgConfig::GTK)

set(flutter_openssl_binaries_bundled_libraries
    "" "${CMAKE_CURRENT_SOURCE_DIR}/lib/libcrypto.so"
    "${CMAKE_CURRENT_SOURCE_DIR}/lib/libssl.so"
    PARENT_SCOPE)
