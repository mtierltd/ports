# $OpenBSD: Makefile,v 1.9 2018/06/29 22:16:27 espie Exp $

COMMENT =	app template generator for KDE development
DISTNAME =	kapptemplate-${MODKDE4_VERSION}
REVISION =	4

CATEGORIES =	devel
HOMEPAGE =	http://projects.kde.org/projects/kde/kdesdk/kapptemplate

WANTLIB =  c m pthread
WANTLIB += ${COMPILER_LIBCXX}
WANTLIB += lib/qt4/QtDBus lib/qt4/QtGui lib/qt4/QtNetwork lib/qt4/QtSvg
WANTLIB += lib/qt4/QtXml
WANTLIB += ${KDE4LIB}/kdeui ${KDE4LIB}/kio

BUILD_DEPENDS =	archivers/gtar
RUN_DEPENDS =	devel/desktop-file-utils \
		x11/gtk+3,-guic

.include <bsd.port.mk>
