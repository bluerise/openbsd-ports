COMMENT =	Tcl UDP extension

DISTNAME =	tcludp-1.0.11
REVISION =	1
CATEGORIES =	net
HOMEPAGE =	https://sourceforge.net/projects/tcludp/
MAINTAINER =	Sebastian Reitenbach <sebastia@openbsd.org>

# BSD
PERMIT_PACKAGE =	Yes

SITES =		${SITE_SOURCEFORGE:=tcludp/}
MODULES =	lang/tcl
BUILD_DEPENDS =	${MODTCL_BUILD_DEPENDS}
RUN_DEPENDS =	${MODTCL_RUN_DEPENDS}
MAKE_FLAGS =	DTPLITE=:
FAKE_FLAGS =	PKG_DIR=tcludp
SEPARATE_BUILD =Yes
CONFIGURE_STYLE=gnu

CONFIGURE_ARGS+=--with-tcl=${MODTCL_LIBDIR} \
		--libdir=${MODTCL_TCLDIR} \
		--datadir=${PREFIX}/share/examples

WRKDIST =	${WRKDIR}/tcludp
TEST_TARGET =	test

.include <bsd.port.mk>
