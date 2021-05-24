# $OpenBSD$

COMMENT =		Modding API with a typesafe hierarchical key-value database
DISTNAME =		nyan-0.2.0
CATEGORIES =		games
HOMEPAGE =		https://github.com/SFTtech/nyan

GH_ACCOUNT =		SFTtech
GH_PROJECT =		nyan
GH_COMMIT =		4dbc2b53c5a2f96dd5b269879f36d0523afbde6a

# GPLv3+
PERMIT_PACKAGE =	Yes

SHARED_LIBS +=		nyan			0.1

MODULES =		devel/cmake

BUILD_DEPENDS =		devel/libexecinfo

CXXFLAGS +=		-I${LOCALBASE}/include
LDFLAGS +=		-lc

NO_TEST =		Yes

pre-build:
			rm -f ${WRKSRC}/version

.include <bsd.port.mk>
