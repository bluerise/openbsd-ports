COMMENT=	get images from USB cameras using the OV511(+) chipsets

DISTNAME=	vid-1.0.1
REVISION=	7
CATEGORIES=	graphics

HOMEPAGE=	https://ovtvid-bsd.sourceforge.net/

# GPL
PERMIT_PACKAGE=	Yes

SITES=		${SITE_SOURCEFORGE:=ovtvid-bsd/}

LIB_DEPENDS=	graphics/netpbm
WANTLIB=	c m netpbm

MAKE_FLAGS=	CFLAGS="${CFLAGS}" CPPFLAGS="-I${LOCALBASE}/include" \
		LIBS="-L${LOCALBASE}/lib -lnetpbm -lm"
ALL_TARGET=	default

NO_TEST=	Yes

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/vid ${PREFIX}/bin
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/vid
	${INSTALL_DATA} ${WRKSRC}/README ${PREFIX}/share/doc/vid/README

.include <bsd.port.mk>
