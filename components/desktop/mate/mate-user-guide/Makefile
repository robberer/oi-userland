#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL)". You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2016 Alexander Pyhalov
#

include ../../../../make-rules/shared-macros.mk

COMPONENT_NAME=		mate-user-guide
COMPONENT_MJR_VERSION=	1.18
COMPONENT_MNR_VERSION=	0
COMPONENT_VERSION=	$(COMPONENT_MJR_VERSION).$(COMPONENT_MNR_VERSION)
COMPONENT_PROJECT_URL=	http://mate-desktop.org
COMPONENT_SUMMARY=	MATE documentation
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.xz
COMPONENT_ARCHIVE_HASH=	\
    sha256:abe2ee40b9788c887abccc7554564bd951eb26ed08c89b4fe59e0d95b2216b38
COMPONENT_ARCHIVE_URL=	http://pub.mate-desktop.org/releases/$(COMPONENT_MJR_VERSION)/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE= FDLv1.1
COMPONENT_LICENSE_FILE= COPYING
COMPONENT_CLASSIFICATION = Desktop (GNOME)/Documentation
COMPONENT_FMRI =	desktop/mate/mate-user-guide


include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

PATH=$(PATH.gnu)

COMPONENT_PREP_ACTION = cd $(@D) && autoreconf -f -i

# Missing files in build dir for configure without this.
COMPONENT_PRE_CONFIGURE_ACTION =	($(CLONEY) $(SOURCE_DIR) $(@D))
CONFIGURE_SCRIPT = $(@D)/configure

CONFIGURE_OPTIONS+=	--sysconfdir=/etc

# common targets
build:		$(BUILD_32)

install:	$(INSTALL_32)

test:		$(NO_TESTS)

REQUIRED_PACKAGES += library/perl-5/xml-parser-522
REQUIRED_PACKAGES += runtime/perl-522
REQUIRED_PACKAGES += text/gnu-gettext
REQUIRED_PACKAGES += text/gnu-grep
REQUIRED_PACKAGES += text/intltool
