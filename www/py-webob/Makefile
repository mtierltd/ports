# $OpenBSD: Makefile,v 1.15 2019/11/08 23:37:32 kmos Exp $

COMMENT =	wsgi request and response object

MODPY_EGG_VERSION = 1.7.2
DISTNAME =	WebOb-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME:L}
REVISION =	1

CATEGORIES =	www devel

HOMEPAGE =	https://webob.org/

# MIT
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

MODPY_PI =	Yes
MODPY_SETUPTOOLS =	Yes
MODPY_PYTEST =		Yes

TEST_DEPENDS =	www/py-webtest${MODPY_FLAVOR}

FLAVORS=	python3
FLAVOR?=

DOCS =		differences.txt do-it-yourself.txt index.txt whatsnew-*.txt \
		reference.txt
EXAMPLES =	comment-example.txt file-example.txt jsonrpc-example.txt \
		wiki-example.txt

post-extract:
	find ${WRKSRC} -perm 0666 -exec chmod 0644 {} \;

PYPKGNAME =	${MODPY_PY_PREFIX}webob

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/${PYPKGNAME}
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/${PYPKGNAME}
	cd ${WRKSRC}/docs && ${INSTALL_DATA} ${DOCS} \
	    ${PREFIX}/share/doc/${PYPKGNAME}
	cd ${WRKSRC}/docs && ${INSTALL_DATA} ${EXAMPLES} \
	    ${PREFIX}/share/examples/${PYPKGNAME}

.include <bsd.port.mk>
