# $OpenBSD: Makefile,v 1.41 2019/12/17 09:26:26 ajacoutot Exp $

COMMENT=		GTK+3 remote desktop client

# XXX development moves to GitLab: https://gitlab.com/Remmina/Remmina;
# XXX before updating, ensure freerdp works:
# cf. http://openbsd-archive.7691.n7.nabble.com/x11-freerdp-update-to-2-0-0-rc4-tp360502p360567.html
GH_TAGNAME=		v1.2.30
GH_PROJECT=		Remmina
GH_ACCOUNT=		FreeRDP
PKGNAME=		remmina-${GH_TAGNAME:S/v//}
REVISION=		9

CATEGORIES=		x11 net

HOMEPAGE=		https://www.remmina.org/

# GPLv2
PERMIT_PACKAGE=		Yes

WANTLIB += ICE SM X11 Xext atk-1.0 avahi-client avahi-common avahi-ui-gtk3
WANTLIB += c cairo cairo-gobject crypto freerdp-client2 freerdp2
WANTLIB += gcrypt gdk-3 gdk_pixbuf-2.0 gio-2.0 glib-2.0 gmodule-2.0
WANTLIB += gobject-2.0 gthread-2.0 gtk-3 harfbuzz intl json-glib-1.0
WANTLIB += pango-1.0 pangocairo-1.0 pthread secret-1 soup-2.4
WANTLIB += spice-client-glib-2.0 spice-client-gtk-3.0 ssh ssl
WANTLIB += vncclient vte-2.91 winpr2 xkbfile

MODULES=		devel/cmake

BUILD_DEPENDS=		devel/gettext,-tools \
			devel/spice-protocol

LIB_DEPENDS=		devel/gettext,-runtime \
			devel/libsoup \
			devel/json-glib \
			devel/vte3 \
			net/avahi,,-gtk3 \
			net/libvncserver \
			security/libssh \
			x11/freerdp \
			x11/spice-gtk \
			x11/gnome/libsecret

RUN_DEPENDS=		devel/desktop-file-utils \
			misc/shared-mime-info \
			x11/gtk+3,-guic

# Appindicator is only used by Ubuntu's Unity.
CONFIGURE_ARGS +=	-DWITH_APPINDICATOR=OFF \
			-DCMAKE_C_FLAGS="-I${X11BASE}/include -I${LOCALBASE}/include ${CFLAGS}"

# telepathy support is removed in newer releases
CONFIGURE_ARGS +=	-DWITH_TELEPATHY=OFF

DEBUG_PACKAGES=		${BUILD_PACKAGES}

.include <bsd.port.mk>
