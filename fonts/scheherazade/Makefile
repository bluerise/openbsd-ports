V =			3.300
COMMENT =		traditional Arabic Unicode font
DISTNAME =		ScheherazadeNew-${V}
PKGNAME =		scheherazade-${V}
CATEGORIES =		fonts

HOMEPAGE =		https://software.sil.org/scheherazade/
MAINTAINER =		George Rosamond <george@nycbug.org>

# SIL OFL 1.1
PERMIT_PACKAGE =	Yes

SITES =			https://software.sil.org/downloads/r/scheherazade/
EXTRACT_SUFX =		.zip

NO_BUILD =		Yes
NO_TEST =		Yes

PKG_ARCH =		*

FONTDIR =		${PREFIX}/share/fonts/scheherazade
DOCDIR =		${PREFIX}/share/doc/scheherazade

do-install:
	${INSTALL_DATA_DIR} ${FONTDIR} ${DOCDIR}
	${INSTALL_DATA} ${WRKDIST}/*.ttf ${FONTDIR}
	${INSTALL_DATA} ${WRKDIST}/*.txt ${DOCDIR}

.include <bsd.port.mk>
