COMMENT=		C-language sources to HTML converter

DISTNAME=		c2html-0.9.6
CATEGORIES=		textproc www

# Old versions seem to stay there...
SITES=			${SITE_SUNSITE:=apps/www/converters/}

# GPLv2
PERMIT_PACKAGE=	Yes

WANTLIB =		c

CONFIGURE_STYLE=	gnu

NO_TEST=		Yes

do-install:
	@ ${INSTALL_PROGRAM} ${WRKSRC}/c2html ${PREFIX}/bin
	@ ${INSTALL_MAN} ${WRKSRC}/c2html.1 ${PREFIX}/man/man1
	@ ${INSTALL_DATA_DIR} ${PREFIX}/share/doc/c2html
.for file in COPYING README
	@ ${INSTALL_DATA} ${WRKSRC}/${file} ${PREFIX}/share/doc/c2html
.endfor

.include <bsd.port.mk>
