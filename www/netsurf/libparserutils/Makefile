COMMENT =		utility library for parser building

NETSURF_PROJECT =	libparserutils
NETSURF_VERSION =	0.2.5

CATEGORIES =		devel
SHARED_LIBS =		parserutils 2.1 #0.2.5

WANTLIB =		iconv

LIB_DEPENDS =		converters/libiconv

MAKE_FLAGS +=		LDFLAGS="${LDFLAGS} -L${LOCALBASE}/lib -liconv"

pre-build:
	echo "CFLAGS += -I${LOCALBASE}/include" \
		> ${WRKSRC}/Makefile.config.override

.include <bsd.port.mk>
