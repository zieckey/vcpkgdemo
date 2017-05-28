add_library(hello SHARED hello.c)
add_library(hello_static STATIC hello.c)
set_target_properties(hello_static PROPERTIES OUTPUT_NAME "hello")

install (TARGETS hello hello_static DESTINATION "lib")
install (FILES hello.h DESTINATION "include")

