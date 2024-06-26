COMMENT =	emulator for Steam online features

# commit from 2023-05-08
GL_V =		0.2.5pl3
GL_ACCOUNT =	Mr_Goldberg
GL_PROJECT =	goldberg_emulator
GL_COMMIT =	475342f0d8b2bd7eb0d93bd7cfdd61e3ae7cda24
DISTNAME =	${GL_PROJECT}-${GL_V}{${GL_COMMIT}}
PKGNAME =	${GL_PROJECT}-${GL_V}
REVISION =	0

SHARED_LIBS +=	steam_api	3.0	# 2023-05-08 (sdk 1.57)
CATEGORIES =	games
HOMEPAGE =	https://gitlab.com/${GL_ACCOUNT}/${GL_PROJECT}
MAINTAINER =	Thomas Frohwein <thfr@openbsd.org>

# LGPLv3+
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} m protobuf-lite
SITES =	https://gitlab.com/${GL_ACCOUNT}/${GL_PROJECT}/-/archive/${GL_COMMIT}/
FIX_CRLF_FILES =	sdk_includes/isteamuser.h \
			sdk_includes/steamclientpublic.h \
			sdk_includes/steam_gameserver.h

# C++17 (abseil)
COMPILER =		base-clang ports-gcc
CXXFLAGS +=		-std=c++17

LIB_DEPENDS =		devel/protobuf
USE_GMAKE =		Yes
NO_TEST =		Yes
WRKDIST =		${WRKDIR}/${GL_PROJECT}-${GL_COMMIT}
SUBST_VARS +=		CXXFLAGS

do-gen:
	${SUBST_CMD} ${WRKSRC}/Makefile

do-install:
	${INSTALL_DATA} ${WRKBUILD}/libsteam_api.so \
		${PREFIX}/lib/libsteam_api.so.${LIBsteam_api_VERSION}
	${INSTALL_DATA_DIR} ${PREFIX}/include/goldberg_emulator/steam/
	cp ${WRKBUILD}/sdk_includes/*.h \
		${PREFIX}/include/goldberg_emulator/steam/

.include <bsd.port.mk>
