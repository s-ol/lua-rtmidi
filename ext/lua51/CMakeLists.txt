add_library(lua51 SHARED
	lapi.c
	lcode.c
	ldebug.c
	ldo.c
	ldump.c
	lfunc.c
	lgc.c
	llex.c
	lmem.c
	lobject.c
	lopcodes.c
	lparser.c
	lstate.c
	lstring.c
	ltable.c
	ltm.c
	lundump.c
	lvm.c
	lzio.c
	lauxlib.c
	lbaselib.c
	ldblib.c
	liolib.c
	lmathlib.c
	loslib.c
	lstrlib.c
	ltablib.c
	loadlib.c
	linit.c
)
target_include_directories(lua51 SYSTEM PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
if(WIN32)
	target_compile_definitions(lua51 PRIVATE LUA_BUILD_AS_DLL)
endif()
