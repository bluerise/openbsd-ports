COMMENT =		search backend for Mew with Hyper Estrairer

V =			0.9.25
GH_ACCOUNT =		yasuoka
GH_PROJECT =		mailest
GH_TAGNAME =		mailest-${V}
DISTNAME =		${GH_PROJECT}-${V}

CATEGORIES =		mail

MAINTAINER =		YASUOKA Masahiko <yasuoka@yasuoka.net>

# BSD and partially LGPLv2.1+
PERMIT_PACKAGE =	Yes

WANTLIB =		c event iconv pthread estraier qdbm

LIB_DEPENDS =		converters/libiconv \
			databases/qdbm \
			textproc/hyperestraier
RUN_DEPENDS =		mail/mew

NO_TEST =		Yes

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/mailest
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/mailest
	${INSTALL_DATA} ${WRKSRC}/README.md ${PREFIX}/share/doc/mailest
	${INSTALL_DATA} ${WRKSRC}/mailestd.conf \
	    ${PREFIX}/share/examples/mailest
	${INSTALL_DATA} ${FILESDIR}/dot.emacs \
	    ${PREFIX}/share/examples/mailest

.include <bsd.port.mk>
