cmake_minimum_required(VERSION 3.1)
project(nanogl)

set(XASH_NANOGL nanogl)
file(GLOB XASH_NANOGL_SRC "${PROJECT_SOURCE_DIR}/*.cpp")
add_library(${XASH_NANOGL} STATIC ${XASH_NANOGL_SRC})
target_compile_definitions(${XASH_NANOGL} PRIVATE __MULTITEXTURE_SUPPORT__ NANOGL_MANGLE_PREPEND)
target_include_directories(
	${XASH_NANOGL} PRIVATE
	"${PROJECT_SOURCE_DIR}"
	"${PROJECT_SOURCE_DIR}/GL"
)