# Copyright (c) 2023 Stappler LLC <admin@stappler.dev>
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
# THE SOFTWARE.

# This application created for single purpose - build all of modules to generate clang command lists

STAPPLER_ROOT ?= ../..

LOCAL_MAKEFILE := $(lastword $(MAKEFILE_LIST))

LOCAL_OUTDIR := stappler-build
LOCAL_EXECUTABLE := sampleapp

LOCAL_MODULES_PATHS = \
	$(STAPPLER_ROOT)/core/stappler-modules.mk \
	$(STAPPLER_ROOT)/xenolith/xenolith-modules.mk

LOCAL_MODULES ?= \
	stappler_core \
	stappler_data \
	stappler_sql \
	stappler_bitmap \
	stappler_brotli_lib \
	stappler_db \
	stappler_vg \
	stappler_threads \
	stappler_zip \
	stappler_threads \
	stappler_network \
	stappler_backtrace \
	xenolith_backend_vkgui \
	xenolith_resources_assets \
	xenolith_renderer_material2d

LOCAL_ROOT = .

LOCAL_SRCS_DIRS :=
LOCAL_SRCS_OBJS :=

LOCAL_INCLUDES_DIRS :=
LOCAL_INCLUDES_OBJS :=

LOCAL_MAIN := main.cpp

include $(STAPPLER_ROOT)/build/make/universal.mk
