COMMENT =	Komi the Space Frog

DISTNAME =	komi-1.04
REVISION =	3
CATEGORIES =	games

HOMEPAGE =	https://komi.sourceforge.net/

# GPLv2
PERMIT_PACKAGE =	Yes

SITES =		${SITE_SOURCEFORGE:=komi/}

WANTLIB =	SDL c pthread SDL_mixer>=3

LIB_DEPENDS =	devel/sdl-mixer

NO_TEST =	Yes

pre-configure:
	${SUBST_CMD} ${WRKSRC}/Makefile

.include <bsd.port.mk>
