# Only used by lang/flang; only supported on amd64 and arm64
ONLY_FOR_ARCHS =	amd64 arm64

COMMENT =	port of POSIX asynchronous I/O routines from DragonFly BSD
DISTNAME =	libaio_compat-5.2.2
REVISION =	0
CATEGORIES =	devel

SHARED_LIBS +=	aio_compat                0.0 # 0.0

HOMEPAGE =	https://www.dragonflybsd.org/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# BSD
PERMIT_PACKAGE =	Yes

WANTLIB += pthread

SITES =		https://mirrors.nycbug.org/pub/distfiles/

NO_TEST =	Yes

.include <bsd.port.mk>
