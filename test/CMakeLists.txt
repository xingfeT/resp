#
# This file is part of the CMake build system for RESP
#
# Copyright (c) 2016 Nous Xiong (348944179 at qq dot com)
#
# Distributed under the Boost Software License, Version 1.0. (See accompanying
# file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)
#
# See https://github.com/nousxiong/resp for latest version.
#

file (GLOB_RECURSE RESP_UNIT_TEST_FILES "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")

include_directories (${CMAKE_CURRENT_SOURCE_DIR})

add_executable (resp_ut ${RESP_UNIT_TEST_FILES})
target_link_libraries(resp_ut boost_system)
install (TARGETS resp_ut RUNTIME DESTINATION bin)
