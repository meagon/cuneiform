add_library(cfcompat ${LIBTYPE} cfcompat.c)
target_link_libraries(cfcompat ${DL_LIB})
set_property(TARGET cfcompat PROPERTY COMPILE_DEFINITIONS __CFCOMPAT__)

library_hook(cfcompat)
