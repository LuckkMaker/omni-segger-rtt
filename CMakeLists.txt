# Copyright (c) 2024 LuckkMaker
# All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

set(SEGGER_RTT_CFG_SOURCE_FILE ${CMAKE_CURRENT_LIST_DIR}/Config/SEGGER_RTT_Conf.h)
set(SEGGER_RTT_CFG_TARGET_FILE ${OMNI_DEBUG_CFG_DIR}/SEGGER_RTT_Conf.h)
omni_add_configure_file(${SEGGER_RTT_CFG_SOURCE_FILE} ${SEGGER_RTT_CFG_TARGET_FILE})

add_library(omni-segger-rtt INTERFACE)

file(GLOB OMNI_SEGGER_RTT_SOURCES
    "RTT/SEGGER_RTT_printf.c"
    "RTT/SEGGER_RTT.c"
)

target_sources(omni-segger-rtt INTERFACE
    ${OMNI_SEGGER_RTT_SOURCES}
)

target_include_directories(omni-segger-rtt INTERFACE
    RTT
)
