# $OpenBSD: Makefile,v 1.6 2020/02/06 20:00:18 rsadowski Exp $

COMMENT =		BitTorrent client with web interface
PKGNAME =		qbittorrent-nox-${VER}

WANTLIB += ${COMPILER_LIBCXX} Qt5Core Qt5Network Qt5Xml boost_system
WANTLIB += boost_system-mt c crypto m ssl torrent-rasterbar z

LIB_DEPENDS +=		net/libtorrent-rasterbar \
			devel/boost

CONFIGURE_ARGS +=	--disable-gui

# remove include directives which cause incorrect gmake behavior
pre-build:
	@cd ${WRKBUILD}/src && \
		sed -ie "/^\-include/d" Makefile

pre-install:
	${SUBST_CMD} ${WRKSRC}/conf.pri

.include <bsd.port.mk>
