# $OpenBSD: Makefile,v 1.8 2020/01/01 23:04:32 bluhm Exp $

COMMENT =	test for trailing space in source files

DISTNAME =	Test-TrailingSpace-0.0302

CATEGORIES =	devel

MAINTAINER =		Alexander Bluhm <bluhm@openbsd.org>

# MIT
PERMIT_PACKAGE =	Yes

MODULES =		cpan
BUILD_DEPENDS =		devel/p5-Module-Build>=0.28
RUN_DEPENDS =		devel/p5-File-Find-Object-Rule>=0.0301

CONFIGURE_STYLE =	modbuild

PKG_ARCH =		*

.include <bsd.port.mk>
