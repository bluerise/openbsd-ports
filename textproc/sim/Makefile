COMMENT =		tests lexical similarity in texts

DISTNAME =		sim_2_26
PKGNAME =		sim-2.26
REVISION =		2
CATEGORIES =		textproc

HOMEPAGE =		https://dickgrune.com/Programs/similarity_tester/

MAINTAINER =     	Laurent Fanis <laurent.fanis@gmail.com>

# BSD
PERMIT_PACKAGE =	Yes

WANTLIB =		c

EXTRACT_SUFX =		.zip
SITES =			https://dickgrune.com/Programs/similarity_tester/

MAKE_FLAGS =		CC=${CC} CFLAGS="${CFLAGS} -DUNIX" LDFLAGS="${LDFLAGS}"

WRKDIST =		${WRKDIR}

NO_TEST =		Yes

do-install:
		${INSTALL_PROGRAM} ${WRKSRC}/sim_* ${PREFIX}/bin
		${INSTALL_MAN} ${WRKSRC}/sim.1 ${PREFIX}/man/man1

.include <bsd.port.mk>
