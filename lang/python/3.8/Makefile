# $OpenBSD: Makefile,v 1.3 2019/12/28 18:34:39 kmos Exp $

# IMPORTANT!  If you make any changes to the Python ports, be sure
# to also update files/CHANGES.OpenBSD for your change.  This is a
# requirement of the PSF license, if it constitutes a change to
# Python itself.

VERSION =		3.8
PATCHLEVEL =		.1
SHARED_LIBS =		python3.8 0.0
VERSION_SPEC =		>=3.8,<3.9

CONFIGURE_ARGS +=	--with-ensurepip=no
CONFIGURE_ARGS +=	--enable-loadable-sqlite-extensions

CONFIGURE_STYLE = autoconf

PORTROACH =             limit:^3\.8

TEST_IS_INTERACTIVE =	Yes

.include <bsd.port.mk>
