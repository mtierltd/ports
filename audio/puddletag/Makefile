# $OpenBSD: Makefile,v 1.13 2019/11/19 21:21:10 sthen Exp $

COMMENT =		spreadsheet-like audio file tagger

# Python 3 info: https://github.com/keithgg/puddletag/issues/300

MODPY_EGG_VERSION =	1.2.0
DISTNAME =		puddletag-${MODPY_EGG_VERSION}
REVISION =		4

CATEGORIES =		audio

HOMEPAGE =		http://puddletag.net

# GPLv3
PERMIT_PACKAGE =	Yes

MASTER_SITES =		https://github.com/keithgg/puddletag/releases/download/v${MODPY_EGG_VERSION}/
# kn: Remove with next update
DISTFILES =		${DISTNAME}_1{${DISTNAME}}${EXTRACT_SUFX}

MODULES =		lang/python
MODPY_VERSION =		${MODPY_DEFAULT_VERSION_2}
MODPY_SETUPTOOLS =	Yes

RUN_DEPENDS =		audio/py-mutagen>=1.14 \
			devel/desktop-file-utils \
			devel/py-configobj \
			devel/py-parsing>=1.5.1 \
			x11/py-qt4>=4.5

# Author didn't write tests
NO_TEST =		Yes

post-install:
	mv ${PREFIX}/share/man/man1/puddletag.1 ${PREFIX}/man/man1/

.include <bsd.port.mk>
