# $OpenBSD: Makefile,v 1.8 2020/01/07 20:22:07 zhuk Exp $

QT5NAME =		QtDataVis3D
COMMENT-main =		Qt5 3D data visualization components
REVISION-main =		0

MULTI_PACKAGES =	-main -examples

SHARED_LIBS =	Qt5DataVisualization	0.1

WANTLIB += ${COMPILER_LIBCXX} GL Qt5Core Qt5Gui Qt5Network Qt5Qml
WANTLIB += Qt5Quick m

LIB_DEPENDS =		x11/qt5/qtdeclarative>=${QT5_VERSION},<${QT5_NEXT_VERSION}

FLAVORS =		debug

.include <bsd.port.mk>
