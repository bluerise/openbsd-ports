COMMENT =		yet another SQLite wrapper

DISTNAME =		ksql-0.3.5
CATEGORIES =		databases

MAINTAINER =		James Turner <james@calminferno.net>

HOMEPAGE =		https://kristaps.bsd.lv/ksql/
SITES =			https://kristaps.bsd.lv/ksql/snapshots/

# ISC
PERMIT_PACKAGE =	Yes

# not directly linked to this static lib, but depends on API
LIB_DEPENDS =		databases/sqlite3

CONFIGURE_STYLE =	simple
CONFIGURE_ARGS =	PREFIX="${WRKINST}${PREFIX}" CPPFLAGS="-I${LOCALBASE}/include"

ALL_TARGET =		libksql.a
FAKE_FLAGS =		DESTDIR=""

.include <bsd.port.mk>
