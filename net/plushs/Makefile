COMMENT=		simple hostname scanner

DISTNAME=		plushs-1.2
REVISION=		3
CATEGORIES=		net
SITES=			${SITE_SOURCEFORGE:=plushs/}

HOMEPAGE=		https://plushs.sourceforge.net

PERMIT_PACKAGE=	Yes
WANTLIB=		c

SEPARATE_BUILD=		Yes
CONFIGURE_STYLE=	gnu

NO_TEST=		Yes

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/plushs
	${INSTALL_DATA} ${WRKSRC}/README ${PREFIX}/share/doc/plushs
	${INSTALL_DATA} ${WRKSRC}/patterns.list ${PREFIX}/share/doc/plushs

.include <bsd.port.mk>
