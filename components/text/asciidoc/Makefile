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
# Copyright 2016 Alexander Pyhalov
#

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME= 	asciidoc
COMPONENT_VERSION= 	8.6.9
COMPONENT_SUMMARY= 	Text based document generation tool
COMPONENT_SRC= 		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= 	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH= \
  sha256:78db9d0567c8ab6570a6eff7ffdf84eadd91f2dfc0a92a2d0105d323cab4e1f0
COMPONENT_ARCHIVE_URL= \
  http://sourceforge.net/projects/asciidoc/files/asciidoc/$(COMPONENT_VERSION)/$(COMPONENT_ARCHIVE)/download
COMPONENT_PROJECT_URL = http://www.methods.co.nz/asciidoc/

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

# Missing files in build dir for configure without this.
COMPONENT_PRE_CONFIGURE_ACTION =        ($(CP) -a  $(SOURCE_DIR)/* $(@D))

CONFIGURE_OPTIONS +=  --sysconfdir=/etc

CONFIGURE_ENV += PYTHON=$(PYTHON)

build: $(BUILD_32)

install: $(INSTALL_32)

REQUIRED_PACKAGES += runtime/python-27
