cmake_minimum_required(VERSION 3.21)
project(eos_portable_archvive VERSION 1.0.0)

add_library(eos_portable_archvive INTERFACE)
add_library(eos::portable_archive ALIAS eos_portable_archvive)

target_include_directories(
	eos_portable_archvive
INTERFACE
	"${CMAKE_CURRENT_SOURCE_DIR}"
)

target_link_libraries(
	eos_portable_archvive
INTERFACE
	Boost::serialization
	Boost::math
	Boost::program_options
)
