# SPDX-License-Identifier: BSD-3-Clause
# Copyright(c) 2010-2014 Intel Corporation

include $(RTE_SDK)/mk/rte.vars.mk

ifeq ($(CONFIG_RTE_LIBRTE_FIB),y)

APP = testfib

CFLAGS += -O3
CFLAGS += $(WERROR_FLAGS)
CFLAGS += -DALLOW_EXPERIMENTAL_API

LDFLAGS += -lresolv

# all source are stored in SRCS-y
SRCS-y := main.c

include $(RTE_SDK)/mk/rte.app.mk

endif
