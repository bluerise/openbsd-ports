COMMENT =		vertical shoot-em-up with nontraditional elements

DISTNAME =		garden-1.0.9
REVISION =		5

CATEGORIES =		games

HOMEPAGE =		https://garden.sourceforge.net

MAINTAINER =		Anthony J. Bentley <anthony@anjbe.name>

# GPLv3+
PERMIT_PACKAGE =	Yes

WANTLIB += X11 Xcursor Xext Xfixes Xpm Xrender Xxf86dga Xxf86vm
WANTLIB += alleg c m pthread sndio xcb

SITES =			${SITE_SOURCEFORGE:=garden/}

BUILD_DEPENDS =		devel/desktop-file-utils
RUN_DEPENDS =		devel/desktop-file-utils \
			x11/gtk+4,-guic
LIB_DEPENDS =		games/allegro

CONFIGURE_STYLE =	gnu
CONFIGURE_ENV =		CPPFLAGS="${CPPFLAGS} -I${LOCALBASE}/include"
CFLAGS += -fgnu89-inline -fcommon

.include <bsd.port.mk>
