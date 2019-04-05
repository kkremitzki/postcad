# Target:   postcad_lib
# Type:     Library
file(GLOB SOURCE *.cpp)
add_library(postcad_lib SHARED ${SOURCE})
set_target_properties(postcad_lib PROPERTIES
    "OUTPUT_NAME" "postcad"
    "INCLUDE_DIRECTORIES" "${CMAKE_CURRENT_SOURCE_DIR}/include"
)
install(TARGETS postcad_lib EXPORT postcad DESTINATION ${CMAKE_SOURCE_DIR}/lib)
export(TARGETS postcad_lib FILE ${CMAKE_BINARY_DIR}/postcad-config.cmake)
