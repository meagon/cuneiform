include_directories(sources/src/h)

add_library(cline ${LIBTYPE}
${SNP_SRC}
sources/src/main/clinebase.cpp
sources/src/cpp/clinefunc.cpp
sources/src/main/clinemain.cpp
sources/src/cpp/debug.cpp
sources/src/cpp/lcline.cpp
)

set_property(TARGET cline PROPERTY COMPILE_DEFINITIONS __CLINE__)

target_link_libraries(cline cfcompat)

library_hook(cline)
