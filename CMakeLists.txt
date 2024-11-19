#
# Copyright 2024 NXP
#
# SPDX-License-Identifier: MIT
#


if(CONFIG_MCUX_COMPONENT_middleware.aws_iot.device_shadow.template)
    mcux_add_source(
        SOURCES template/shadow_config.h
    )
    mcux_add_include(
        TARGET_FILES ['shadow_config.h']
        INCLUDES template
    )
endif()

if(CONFIG_MCUX_COMPONENT_middleware.aws_iot.device_shadow)
    mcux_add_source(
        SOURCES source/shadow.c
                source/include/shadow.h
                source/include/shadow_config_defaults.h
    )
    mcux_add_include(
        INCLUDES source/include
    )
endif()
