#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2015 Aurelien Larcher
#

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=           xwininfo
COMPONENT_VERSION=        1.1.3
COMPONENT_FMRI=           x11/diagnostic/xwininfo
COMPONENT_CLASSIFICATION= System/X11
COMPONENT_SUMMARY=  xwininfo - window information utility for X
COMPONENT_SRC=      $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=  $(COMPONENT_SRC).tar.bz2
COMPONENT_ARCHIVE_HASH= \
  sha256:218eb0ea95bd8de7903dfaa26423820c523ad1598be0751d2d8b6a2c23b23ff8
COMPONENT_ARCHIVE_URL= \
  https://www.x.org/releases/individual/app/xwininfo-1.1.3.tar.bz2
COMPONENT_PROJECT_URL = https://www.x.org/
COMPONENT_LICENSE=      MIT License
COMPONENT_LICENSE_FILE= xwininfo.license

include $(WS_TOP)/make-rules/prep.mk
include $(WS_TOP)/make-rules/configure.mk
include $(WS_TOP)/make-rules/ips.mk

PATH=/usr/gnu/bin:/usr/bin

build: $(BUILD_32_and_64)

install: $(INSTALL_32_and_64)

test: $(NO_TESTS)


REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += x11/library/libxcb
