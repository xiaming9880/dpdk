# SPDX-License-Identifier: BSD-3-Clause
# Copyright(c) 2016 Intel Corporation

ifeq ($(RTE_SDK),)
$(error "Please define RTE_SDK environment variable")
endif

# Default target, detect a build directory, by looking for a path with a .config
RTE_TARGET ?= $(notdir $(abspath $(dir $(firstword $(wildcard $(RTE_SDK)/*/.config)))))

include $(RTE_SDK)/mk/rte.vars.mk

# binary name
APP = ka-agent

# all source are stored in SRCS-y
SRCS-y := main.c

CFLAGS += $(WERROR_FLAGS) -I$(SRCDIR)/../
LDFLAGS += -lrt
include $(RTE_SDK)/mk/rte.extapp.mk
