#
# project: fips-libpng
#
cmake_minimum_required(VERSION 3.21)

if (NOT FIPS_IMPORT)
    project(fips-libpng)

# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

fips_setup()
endif()    


fips_begin_lib(libpng)
target_include_directories(libpng PRIVATE ../fips-zlib/zlib)
fips_src(libpng/ NO_RECURSE)
fips_end_lib()