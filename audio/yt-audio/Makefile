# $OpenBSD: Makefile,v 1.1.1.1 2020/01/22 07:45:46 pirofti Exp $

COMMENT =		youtube-dl wrapper to manage youtube audio

MODPY_EGG_VERSION =	0.1
DISTNAME =		yt-audio-${MODPY_EGG_VERSION}
CATEGORIES =		audio

MAINTAINER =		Paul Irofti <pirofti@openbsd.org>

# MIT
PERMIT_PACKAGE =	Yes

MODULES =		lang/python
MODPY_VERSION =		${MODPY_DEFAULT_VERSION_3}

RUN_DEPENDS =		www/youtube-dl \
			graphics/ffmpeg

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes
MODPY_PYTEST =		Yes

.include <bsd.port.mk>
