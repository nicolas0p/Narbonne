add_library(asio STATIC "${CMAKE_CURRENT_SOURCE_DIR}/asio/asio/src/asio.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/asio/asio/include/asio.hpp")

target_compile_definitions(
    asio PUBLIC ASIO_STANDALONE
)
