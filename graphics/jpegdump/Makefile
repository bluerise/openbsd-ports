COMMENT =	dump raw jpeg exif information
CATEGORIES =	graphics devel

SITES =		https://svn.xiph.org/experimental/giles/

# GPLv2+
PERMIT_PACKAGE =	Yes

V =		1.0
DISTFILES =	jpegdump.c
DIST_SUBDIR =	jpegdump-$V
DISTNAME =	jpegdump-$V
EXTRACT_CASES = *.c) ln -s ${FULLDISTDIR}/$$archive ${WRKDIR};;
REVISION =	1

WRKDIST =	${WRKDIR}

WANTLIB +=	c

do-build:
	cd ${WRKBUILD} && ${CC} ${CFLAGS} -o jpegdump jpegdump.c

do-install:
	${INSTALL_PROGRAM} ${WRKBUILD}/jpegdump ${PREFIX}/bin

.include <bsd.port.mk>
