COMMENT =	library of general purpose APIs

DISTNAME =	libowfat-0.32
REVISION =	0
EXTRACT_SUFX =	.tar.xz

SHARED_LIBS=	owfat 0.1

CATEGORIES=	devel

HOMEPAGE=	https://www.fefe.de/libowfat/

MAINTAINER=	Jan Klemkow <j.klemkow@wemelug.de>

# GPLv2 only
PERMIT_PACKAGE =	Yes

WANTLIB =	c pthread

SITES =		https://www.fefe.de/libowfat/

MAKE_FLAGS =	CC="${CC}" \
		OPT_REG="${CFLAGS}" OPT_PLUS="${CFLAGS}" \
		SO_VERSION="${LIBowfat_VERSION}"
FAKE_FLAGS =	prefix=${PREFIX} \
		INCLUDEDIR=${PREFIX}/include \
		MAN3DIR=${PREFIX}/share/libowfat/man/man3

USE_GMAKE =	Yes

NO_TEST =	Yes

CFLAGS +=	-fpic
MAKE_FILE=	GNUmakefile

.include <bsd.port.mk>
