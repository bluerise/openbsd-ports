COMMENT=	MOD/S3M/MTM tracker that does its own DSP
DISTNAME=	nspmod-0.1
REVISION=	1
CATEGORIES=	audio
SITES=		${SITE_SUNSITE:=apps/sound/players/}

PERMIT_PACKAGE=	Yes

WANTLIB=		c sndio

MAKE_ENV=	CC=${CC}

NO_TEST=	Yes

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/nspmod ${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/nspmod.1 ${PREFIX}/man/man1

.include <bsd.port.mk>
