COMMENT=	deductive database system similar to Prolog

DISTNAME=	datalog-2.6
REVISION=	2
SHARED_LIBS +=  datalog                   0.0 # 0.0
CATEGORIES=	lang

HOMEPAGE=	https://datalog.sourceforge.net/

# LGPLv2.1+
PERMIT_PACKAGE=	Yes

WANTLIB += ${MODLUA_WANTLIB}
WANTLIB += c curses m readline

SITES=			${SITE_SOURCEFORGE:=datalog/}

MODULES=		lang/lua

# keep same version as bundled
MODLUA_VERSION=		5.3
MODLUA_SA=		Yes

CONFIGURE_STYLE=	gnu
CONFIGURE_ARGS=		--with-lua \
			--with-lua-suffix=${MODLUA_VERSION}
# configure is wrong, the --with-lua-suffix option IS used
CONFIGURE_ENV=		CPPFLAGS="${CPPFLAGS} -I${MODLUA_INCL_DIR}" \
			LDFLAGS="${LDFLAGS} -L${LOCALBASE}/lib"

# Some extra checks in addition to the check target
post-test:
	cd ${WRKSRC} && /bin/sh try.sh

.include <bsd.port.mk>
