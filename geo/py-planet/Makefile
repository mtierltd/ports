# $OpenBSD: Makefile,v 1.7 2020/02/25 10:02:55 landry Exp $

COMMENT =	client library and CLI for Planet's public API
#'
MODPY_EGG_VERSION =	1.4.5
DISTNAME =	planet-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME}

CATEGORIES =	geo

# Apache 2.0
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes

FLAVORS =		python3
FLAVOR =		python3

# tests not bundled; test infrastructure left here for manual fetches
#NO_TEST =	Yes

MODPY_PYTEST =	Yes
RUN_DEPENDS +=	devel/py-click${MODPY_FLAVOR} \
		www/py-requests${MODPY_FLAVOR} \
		www/py-requests-futures${MODPY_FLAVOR}
TEST_DEPENDS =	devel/py-mock${MODPY_FLAVOR} \
		www/py-requests-mock${MODPY_FLAVOR}

post-install:
	rm ${PREFIX}/LICENSE

.include <bsd.port.mk>
