COMMENT =	proxy for Asterisk Manager Interface

# there is an active fork in davies147/astmanproxy, but it uses various
# linuxisms (pthread_timedjoin_np, prctl)
GH_ACCOUNT =	davetroy
GH_PROJECT =	astmanproxy
GH_COMMIT =	f4b952a717b7e982b585bf0daa86398add394a88
DISTNAME =	astmanproxy-1.22pre20081208
REVISION =	2

CATEGORIES =	telephony

HOMEPAGE =	http://www.voip-info.org/tiki-index.php?page=AstManProxy

MAINTAINER =	Stuart Henderson <stu.ports@spacehopper.org>

# GPLv2
PERMIT_PACKAGE =	Yes

WANTLIB =	c crypto pthread ssl

MAKE_ENV =	CFLAGS="${CFLAGS}"

MAKE_FLAGS =	CC="${CC}" SYSCONFDIR=${SYSCONFDIR} \
		LIBDIR=${WRKINST}/${PREFIX}/lib/astmanproxy \
		MODDIR=${PREFIX}/lib/astmanproxy/modules \
		CONFDIR=${SYSCONFDIR}/astmanproxy \
		PERMDIR=${SYSCONFDIR}/astmanproxy

FAKE_FLAGS =	PREFIX=${PREFIX} \
		MODDIR=${WRKINST}${PREFIX}/lib/astmanproxy/modules \
		CONFDIR_REAL=${WRKINST}/${PREFIX}/share/examples/astmanproxy \
		PERMDIR_REAL=${WRKINST}/${PREFIX}/share/examples/astmanproxy

USE_GMAKE =	Yes
NO_TEST =	Yes
ALL_TARGET =	astmanproxy
DEBUG_PACKAGES = ${BUILD_PACKAGES}

pre-configure:
	${SUBST_CMD} ${WRKSRC}/configs/astmanproxy.conf

post-install:
	${INSTALL_DATA} ${WRKSRC}/configs/ssl.conf \
	    ${PREFIX}/share/examples/astmanproxy/proxy-ssl.conf
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/astmanproxy/
	${INSTALL_DATA} ${WRKSRC}/README ${WRKSRC}/doc/* \
	    ${PREFIX}/share/doc/astmanproxy

.include <bsd.port.mk>
