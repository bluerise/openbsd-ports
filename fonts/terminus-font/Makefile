COMMENT =		fixed width fonts especially for long hacking sessions

DISTNAME =		terminus-font-4.49.1
REVISION =		2
CATEGORIES =		fonts x11

HOMEPAGE =		https://terminus-font.sourceforge.net/

MAINTAINER =		LEVAI Daniel <leva@ecentrum.hu>

# SIL OFL 1.1
PERMIT_PACKAGE =		Yes

SITES =			${SITE_SOURCEFORGE:=terminus-font/}

MODULES +=		lang/python
MODPY_RUNDEP =		No
MAKE_FLAGS =		INT=${MODPY_BIN}

CONFIGURE_STYLE =	simple
NO_TEST =		Yes
USE_X11 =		Yes

ALL_TARGET =		pcf pcf-8bit raw otb

FONTDIR =		${PREFIX}/share/fonts/terminus

USE_GMAKE =		Yes

FLAVORS =		symquotes centered_tilde
FLAVOR ?=

.if ${FLAVOR:Mcentered_tilde}
FLAVOR_PATCHES += ${WRKSRC}/alt/td1.diff
.endif

.if ${FLAVOR:Msymquotes}
FLAVOR_PATCHES += ${WRKSRC}/alt/gq2.diff
.endif

PATCH_LIST = patch-* ${FLAVOR_PATCHES}

PKG_ARCH =	*

post-build:
	${GZIP_CMD} ${WRKSRC}/*.pcf

do-install:
	${X11BASE}/bin/mkfontdir ${WRKSRC}
	egrep '\.pcf\.gz' ${WRKSRC}/fonts.dir | \
		sed 's/\.pcf\.gz//g' > ${WRKSRC}/fonts.alias
	${INSTALL_DATA_DIR} ${FONTDIR}
	${INSTALL_DATA} ${WRKSRC}/*.pcf.gz ${FONTDIR}
	${INSTALL_DATA} ${WRKSRC}/*.otb ${FONTDIR}
	${INSTALL_DATA} ${WRKBUILD}/fonts.alias ${FONTDIR}/fonts.alias-terminus

	${INSTALL_DATA_DIR} ${PREFIX}/share/misc/pcvtfonts
	${INSTALL_DATA} ${WRKBUILD}/fonts.alias ${FONTDIR}/fonts.alias-terminus
	cd ${WRKSRC}; for i in *.raw; do \
		${INSTALL_DATA} $$i ${PREFIX}/share/misc/pcvtfonts/$${i%.raw}; \
	done

.include <bsd.port.mk>
