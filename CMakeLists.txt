include("../../Config/set_utf8_compiler_encoding.cmake")

add_library(ImGuiColorTextEdit STATIC
    TextEditor.cpp
    TextEditor.h
    TextDiff.cpp
    TextDiff.h
    dtl.h
)

set_utf8_for_target(ImGuiColorTextEdit)

target_include_directories(ImGuiColorTextEdit PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:include>
)
target_link_libraries(ImGuiColorTextEdit PUBLIC FCT_IMGUI)
