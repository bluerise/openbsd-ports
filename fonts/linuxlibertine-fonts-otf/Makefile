COMMENT =		high-quality libre OTF fonts (serif, 19th century book type)

DISTNAME =		LinLibertineOTF_${V}_${D}
PKGNAME =		linuxlibertine-fonts-otf-${V}
V =			5.3.0
D =			2012_07_02
REVISION =		0

CATEGORIES =		fonts

HOMEPAGE =		http://www.linuxlibertine.org/

# GPLv2 / SIL OFL 1.1
PERMIT_PACKAGE =	Yes

SITES =			${SITE_SOURCEFORGE:=linuxlibertine/}
EXTRACT_SUFX =		.tgz

NO_BUILD =		Yes
NO_TEST =		Yes

PKG_ARCH =	*

FONTSDIR =	${PREFIX}/share/fonts/linuxlibertine
DOCDIR =	${PREFIX}/share/doc/linuxlibertine-fonts-otf

do-install:
	${INSTALL_DATA_DIR} ${FONTSDIR} ${DOCDIR}
	${INSTALL_DATA} ${WRKDIR}/*.otf ${FONTSDIR}
	${INSTALL_DATA} ${WRKDIR}/README ${WRKDIR}/*.txt ${DOCDIR}

.include <bsd.port.mk>
