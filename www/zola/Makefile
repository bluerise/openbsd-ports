# ring-v0.17 does not support this arch
NOT_FOR_ARCHS =	sparc64

COMMENT =	static site generator

GH_ACCOUNT =	getzola
GH_PROJECT =	zola
GH_TAGNAME =	v0.18.0

HOMEPAGE =	https://www.getzola.org

CATEGORIES =	www

MAINTAINER =	Peter H. Ezetta <protocall7@gmail.com>

# MIT
PERMIT_PACKAGE =	Yes

WANTLIB +=	${MODCARGO_WANTLIB} m onig

LIB_DEPENDS +=	textproc/oniguruma

MODULES =	devel/cargo

CONFIGURE_STYLE =	cargo

SEPARATE_BUILD =	Yes

.include "crates.inc"
.include <bsd.port.mk>
