# see https://github.com/hfst/hfst/issues/328
NOT_FOR_ARCHS =	${BE_ARCHS}

COMMENT =	Helsinki finite state transducer

V =		3.15.0
DISTNAME =	hfst-$V

SHARED_LIBS +=  hfst                      1.0 # 50.0

CATEGORIES =	textproc

HOMEPAGE =	https://hfst.github.io/

# LGPLv3+
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} c m

SITES =			https://github.com/hfst/hfst/releases/download/v$V/

# C++11
COMPILER =		base-clang ports-gcc

CONFIGURE_STYLE =	gnu

.include <bsd.port.mk>
