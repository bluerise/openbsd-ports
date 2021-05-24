# $OpenBSD$

COMMENT =		open-source real-time strategy game engine
V =			20210514
DISTNAME =		openage-${V}
CATEGORIES =		games x11
HOMEPAGE =		https://www.openra.net
MAINTAINER =		Patrick Wildt <patrick@blueri.se>

# GPLv3 (openage)
PERMIT_PACKAGE =	Yes

DIST_SUBDIR =		openra

#WANTLIB +=	SDL2 freetype openal

GH_ACCOUNT = 		SFTtech
GH_PROJECT = 		openage
GH_COMMIT = 		3e26e3470b0f97ad1c51fe6c6c3a3b2af8354c4e
#DISTFILES =		${DISTNAME}${EXTRACT_SUFX} \
#			nuget-${DISTNAME}${EXTRACT_SUFX}:0
#EXTRACT_SUFX =		.tar.xz

MODULES =		devel/cmake \
			lang/python \
			x11/qt5 \

BUILD_DEPENDS =		math/py-numpy${MODPY_FLAVOR} \
			lang/cython${MODPY_FLAVOR} \
			graphics/py-Pillow${MODPY_FLAVOR} \
			math/eigen3 \
			games/nyan \
			textproc/py-toml${MODPY_FLAVOR} \

LIB_DEPENDS =		devel/sdl2 \
			devel/sdl2-image \
			audio/opusfile \


#CONFIGURE_ARGS +==	DCMAKE_PREFIX_PATH=${LOCALBASE}/include/eigen3 \

#BUILD_DEPENDS =		devel/msbuild \
#			net/curl
#RUN_DEPENDS =		devel/desktop-file-utils \
#			misc/shared-mime-info \
#			net/libmaxminddb,-db \
#			x11/gtk+3,-guic
#LIB_DEPENDS =		audio/openal \
#USE_GMAKE =		Yes
# Target 'test' only checks the official mods for erroneous yaml files
NO_TEST =		Yes
#ALL_TARGET =	version all

# Without GIT_COMMIT, build breaks because of empty $(GitHeadSha)
#MAKE_ENV =		NUGET_PACKAGES=${WRKDIR}/nuget-${DISTNAME} \
#			GIT_COMMIT=3c930fa8721935cf0e381fd349f6f50cf2bc223d
# pass a different $HOME so that the build's NuGet doesn't try to write in $HOME
#MAKE_FLAGS =		HOME=${WRKSRC}/nugethome

#SUBST_VARS +=		LOCALSTATEDIR

.include <bsd.port.mk>
