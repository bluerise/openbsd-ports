# Original from: Kyle Wheeler <kyle@memoryhole.net>

COMMENT =		natural-expression command-line calculator

DISTNAME =		wcalc-2.5
REVISION =		4
CATEGORIES =		math
HOMEPAGE =		https://w-calc.sourceforge.net/
# GPLv2+
PERMIT_PACKAGE =	Yes

WANTLIB += c curses gmp>=7 m mpfr>=0.2 readline

SITES =			${SITE_SOURCEFORGE:=w-calc/}

LIB_DEPENDS =		devel/gmp devel/mpfr

USE_GMAKE =		Yes
CONFIGURE_STYLE =	gnu
CONFIGURE_ENV +=	LDFLAGS="-L${LOCALBASE}/lib" \
			CPPFLAGS="-I${LOCALBASE}/include"

.include <bsd.port.mk>
