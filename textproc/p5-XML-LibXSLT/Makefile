# $OpenBSD: Makefile,v 1.53 2020/01/21 19:27:58 bluhm Exp $

COMMENT =	interface to the GNOME libxslt library

DISTNAME =	XML-LibXSLT-1.99

CATEGORIES =	textproc

MAINTAINER =		Alexander Bluhm <bluhm@openbsd.org>

# Perl
PERMIT_PACKAGE =	Yes

WANTLIB =		c exslt>=7 gcrypt gpg-error iconv intl lzma m perl \
			pthread xml2>=6 xslt>=1 z

MODULES =		cpan
RUN_DEPENDS =		textproc/p5-XML-LibXML>=1.70
LIB_DEPENDS =		textproc/libxml \
			textproc/libxslt>1.1.27
TEST_DEPENDS =		devel/p5-Test-Pod \
			devel/p5-Test-TrailingSpace

.include <bsd.port.mk>
