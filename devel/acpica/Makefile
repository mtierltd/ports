# $OpenBSD: Makefile,v 1.28 2020/02/17 22:38:35 daniel Exp $

COMMENT =		reference implementation of ACPI tools
DISTNAME =		acpica-unix-20200214
PKGNAME =		${DISTNAME:S/-unix//}

CATEGORIES =		devel

HOMEPAGE =		https://acpica.org/

MAINTAINER =		Stuart Henderson <sthen@openbsd.org>

# BSD-ish (or GPLv2 or Intel's own license: triple-licensed)
PERMIT_PACKAGE =	Yes

WANTLIB =		c pthread

MASTER_SITES =		https://acpica.org/sites/acpica/files/

USE_GMAKE =		Yes
BUILD_DEPENDS =		devel/bison
MAKE_FLAGS =		CC="${CC}" HOST=_LINUX
FAKE_FLAGS =		DESTDIR=

do-test:
	cd ${WRKSRC}/tests/templates && sh templates.sh 1

.include <bsd.port.mk>
