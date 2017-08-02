#
# project: fips-libpng
#
cmake_minimum_required(VERSION 2.8)

# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

fips_setup()
fips_project(fips-libpng)

fips_begin_lib(libpng)
fips_include_directories(../fips-zlib/zlib)
fips_src(libpng/ NO_RECURSE)
fips_end_lib()

fips_finish()


