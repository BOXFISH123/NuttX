############################################################################
# boards/arm/kl/freedom-kl25z/src/Makefile
#
#   Copyright (C) 2013-2014 Gregory Nutt. All rights reserved.
#   Author: Gregory Nutt <gnutt@nuttx.org>
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
#
# 1. Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
# 2. Redistributions in binary form must reproduce the above copyright
#    notice, this list of conditions and the following disclaimer in
#    the documentation and/or other materials provided with the
#    distribution.
# 3. Neither the name NuttX nor the names of its contributors may be
#    used to endorse or promote products derived from this software
#    without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
# "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
# LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS
# FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE
# COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT,
# INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
# BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS
# OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED
# AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
# LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
# ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
# POSSIBILITY OF SUCH DAMAGE.
#
############################################################################

-include $(TOPDIR)/Make.defs

ASRCS =
CSRCS = kl_boardinitialize.c

ifeq ($(CONFIG_LIB_BOARDCTL),y)
CSRCS += kl_appinit.c
endif

ifeq ($(CONFIG_KL_TSI),y)
CSRCS += kl_tsi.c
endif

ifeq ($(CONFIG_KL_SPI0),y)
CSRCS += kl_spi.c
else
ifeq ($(CONFIG_KL_SPI1),y)
CSRCS += kl_spi.c
endif
endif

ifeq ($(CONFIG_HAVE_CXX),y)
CSRCS += kl_cxxinitialize.c
endif

ifeq ($(CONFIG_ARCH_LEDS),y)
CSRCS += kl_led.c
endif

ifeq ($(CONFIG_KL_USBOTG),y)
CSRCS += kl_usb.c
endif

ifeq ($(CONFIG_PWM),y)
CSRCS += kl_pwm.c
endif

ifeq ($(CONFIG_SENSORS_QENCODER),y)
CSRCS += kl_qencoder.c
endif

ifeq ($(CONFIG_WATCHDOG),y)
CSRCS += kl_watchdog.c
endif

ifeq ($(CONFIG_SENSORS_ADXL345),y)
CSRCS += kl_adxl345.c
endif

include $(TOPDIR)/boards/Board.mk
