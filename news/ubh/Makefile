COMMENT=	download and decode binaries posted to Usenet

DISTNAME=	ubh-2.5
CATEGORIES=	news
REVISION =	1

HOMEPAGE=	https://ubh.sourceforge.net/

PERMIT_PACKAGE=	Yes

SITES=		${HOMEPAGE}/download/

RUN_DEPENDS=	mail/p5-MIME-tools \
		news/p5-News-Newsrc \
		devel/p5-String-CRC32

NO_BUILD=	Yes
NO_TEST=	Yes
PKG_ARCH=	*

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/ubh
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/ubh
	${INSTALL_PROGRAM} ${WRKSRC}/ubh ${PREFIX}/bin
	${INSTALL_DATA} ${WRKSRC}/doc/ubh.html ${PREFIX}/share/doc/ubh
	cp ${WRKSRC}/examples/* ${PREFIX}/share/examples/ubh

.include <bsd.port.mk>
