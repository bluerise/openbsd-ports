ONLY_FOR_ARCHS =	amd64 i386 macppc

# custom JIT
USE_NOBTCFI =		Yes

BROKEN-i386 =		code/qcommon/vm_x86.c:(.text+0x18): undefined reference to `callMask'

COMMENT-main =		OpenArena client
COMMENT-server =	OpenArena server
COMMENT-data =		OpenArena data for client/server

MULTI_PACKAGES =	-main -server -data

CATEGORIES =		games x11

V =			0.8.8
E_V =			${V}# 	engine version

PKGNAME =		openarena-${V}

REVISION-main =		3
REVISION-server =	2
REVISION-data =		0

PKG_ARCH-data = 	*

DISTNAME =		openarena-${V}
DISTFILES =		${DISTNAME}.zip 
DISTFILES.a =		openarena-engine-source-${E_V}.tar.bz2

HOMEPAGE =		https://www.openarena.ws/
MS_PREFIX =		https://download.tuxfamily.org/openarena/rel/
SITES =			${MS_PREFIX}${V:S/.//g}/ \
			${MS_PREFIX}${E_V:S/.//g}/source/
SITES.a =		https://files.poulsander.com/~poul19/public_files/oa/dev088/ \
			http://openbsd.fi/distfiles/

# GPLv2 but contains software with other (free) licenses as well
PERMIT_PACKAGE =	Yes

WANTLIB-main =		GL c m pthread sndio ogg>=5 SDL>=7 vorbis>=7 \
			vorbisfile>=5 curl
WANTLIB-server =	c m

LIB_DEPENDS-main =	audio/libogg \
			audio/libvorbis \
			devel/sdl \
			net/curl
RUN_DEPENDS-main =	${BASE_PKGPATH},-data
RUN_DEPENDS-server =	${BASE_PKGPATH},-data

USE_GMAKE =		Yes
MAKE_FLAGS =		USE_OPENAL=0 \
			FULLBINEXT='' \
			V=1 \
			NO_STRIP=1 \
			DEFAULT_BASEDIR=${LOCALBASE}/share/openarena

.if ${MACHINE_ARCH} == "powerpc"
MAKE_FLAGS += 		ARCH=ppc \
			COMPILE_ARCH=ppc
.endif

.if ${MACHINE_ARCH} == "i386"
MAKE_FLAGS +=		PIE_CFLAGS=-fno-pie PIE_LDFLAGS=-nopie
.endif

NO_TEST =		Yes
WRKDIST =		${WRKDIR}/openarena-engine-source-${E_V}
ALL_TARGET =		release

DEBUG_PACKAGES =	-main -server

post-extract:
	find ${WRKDIR} -name '*.orig' -delete
	mkdir ${WRKSRC}/code/sndio
	cp ${FILESDIR}/snd_sndio.c ${WRKSRC}/code/sndio

do-install:
	${INSTALL_PROGRAM} \
		${WRKDIST}/build/release-openbsd/openarena-* \
		${PREFIX}/bin/
	${INSTALL_DATA_DIR} ${PREFIX}/share/openarena/baseoa
	${INSTALL_DATA_DIR} ${PREFIX}/share/openarena/missionpack
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/openarena
	${INSTALL_DATA} \
		${WRKDIR}/openarena-${E_V}/README \
		${WRKDIR}/openarena-${E_V}/COPYING \
		${WRKDIR}/openarena-${E_V}/CHANGES \
		${PREFIX}/share/doc/openarena/
	${INSTALL_DATA} ${WRKDIR}/openarena-${E_V}/baseoa/* \
		${PREFIX}/share/openarena/baseoa/
	${INSTALL_DATA} ${WRKDIR}/openarena-${E_V}/missionpack/* \
		${PREFIX}/share/openarena/missionpack/


.include <bsd.port.mk>
