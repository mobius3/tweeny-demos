# This file is part of the Tweeny library.
#
# Copyright (c) 2016-2018 Leonardo G. Lucena de Freitas
# Copyright (c) 2016 Guilherme R. Costa
#
# Permission is hereby granted, free of charge, to any person obtaining a copy of
# this software and associated documentation files (the "Software"), to deal in
# the Software without restriction, including without limitation the rights to
# use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
# the Software, and to permit persons to whom the Software is furnished to do so,
# subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in all
# copies or substantial portions of the Software.

# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
# FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
# COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
# IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
# CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# The purpose of this file is to include all examples subdirectories.

find_package(SDL2 QUIET)

macro(add_tweeny_demo)
  set(TARGET ${ARGV0})
  set(SOURCES "${ARGN}")
  list(REMOVE_AT SOURCES 0)
  string(TOUPPER ${TARGET} TARGET_UPPER)
  option(TWEENY_EXAMPLE_${TARGET_UPPER} "Build the ${TARGET} example." ON)
  if (TWEENY_EXAMPLE_${TARGET_UPPER})
    add_executable(${TARGET} ${SOURCES})
    target_link_libraries(${TARGET} PRIVATE tweeny)
  endif ()
endmacro()

if (CMAKE_SYSTEM_NAME STREQUAL "Emscripten")
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -s ALLOW_MEMORY_GROWTH=1")
  set(CMAKE_EXECUTABLE_SUFFIX ".html")
endif ()

add_tweeny_demo(multitype multitype/multitype.cpp)
add_tweeny_demo(easings easings/easings.cpp)
add_tweeny_demo(loop loop/loop.cpp)