# Copyright 2023 The IREE Authors
#
# Licensed under the Apache License v2.0 with LLVM Exceptions.
# See https://llvm.org/LICENSE.txt for license information.
# SPDX-License-Identifier: Apache-2.0 WITH LLVM-exception

iree_cc_library(
  NAME
    registration
  HDRS
    "driver_module.h"
  SRCS
    "driver_module.c"
  DEPS
    iree::base
    iree::base::internal::flags
    iree::base::core_headers
    iree::hal
    iree::hal::drivers::metal
  DEFINES
    "IREE_HAVE_HAL_METAL_DRIVER_MODULE=1"
  PUBLIC
)
