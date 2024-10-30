project(minilua)

add_library(minilua SHARED minilua.h minilua.c)

target_compile_definitions(minilua PRIVATE  LUA_BUILD_AS_DLL=1)


add_executable(example ./tests/example.c)
target_link_libraries(example minilua)
