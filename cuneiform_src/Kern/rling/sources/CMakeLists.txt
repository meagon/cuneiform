add_definitions(-DRLINGS_EXPORTS -DRLING_SECONDARY)

add_library(rlings ${LIBTYPE}
cpp/crled.cpp
cpp/crling.cpp
#SOURCE=.\CRLing.rc
cpp/crlmemory.cpp
cpp/dll.cpp
cpp/rlcontrol.cpp
c/rling_ma.c
c/spel2dic.c
c/spel2voc.c
c/spelabc.c
c/spelart.c
c/spelbuf.c
c/spelchk.c
c/speldat1.c
c/speldat2.c
c/speldici.c
c/speldict.c
c/speldvoc.c
c/speledf1.c
c/speledf2.c
c/speledio.c
c/spelfun.c
c/spelloop.c
c/spelout.c
c/spelq.c
c/spelset.c
c/spelspec.c
c/udictini.c
c/udictuti.c
)
set_property(TARGET rlings PROPERTY COMPILE_DEFINITIONS RLING_SECONDARY)

target_link_libraries(rlings cstr cfcompat)

library_hook(rlings)
