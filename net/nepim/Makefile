COMMENT=		network pipe meter

DISTNAME=		nepim-0.53
REVISION=		2
CATEGORIES=		net sysutils

HOMEPAGE=		https://www.nongnu.org/nepim/

# GPL
PERMIT_PACKAGE=	Yes

WANTLIB= c oop>=4

SITES=			${SITE_SAVANNAH:=nepim/}

LIB_DEPENDS=		devel/liboop

USE_GMAKE=		Yes

NO_TEST=		Yes

WRKSRC=         	${WRKDIST}/src
ALL_TARGET=		default

do-configure:
	${SUBST_CMD} ${WRKSRC}/Makefile

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/nepim ${PREFIX}/bin
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/nepim
	${INSTALL_DATA} ${WRKDIST}/README ${PREFIX}/share/doc/nepim

.include <bsd.port.mk>
