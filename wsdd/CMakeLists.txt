project(${CMAKE_PROJECT_NAME}_wsdd)
cmake_minimum_required(VERSION 2.6)

set(CMAKE_C_FLAGS ${CMAKE_C_FLAGS} "-fPIC")

include_directories(
	${CMAKE_SOURCE_DIR}/include
)

aux_source_directory(. WSDD_SOURCES)
file(GLOB WSDD_HEADERS "*.h")


add_library(${PROJECT_NAME} STATIC ${WSDD_SOURCES} ${WSDD_HEADERS})