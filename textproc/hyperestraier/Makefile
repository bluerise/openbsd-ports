COMMENT=		high performance full-text search system

DISTNAME=		hyperestraier-1.4.13
REVISION=		6
CATEGORIES=		textproc
SHARED_LIBS=		estraier	8.38

HOMEPAGE=		http://fallabs.com/hyperestraier/index.html

MAINTAINER=		Jeremy Evans <jeremy@openbsd.org>

# LGPLv2.1+
PERMIT_PACKAGE=	Yes

SITES=			${SITE_SOURCEFORGE:=hyperestraier/}

WANTLIB=		c iconv m pthread z qdbm>=14.11

LIB_DEPENDS=		converters/libiconv \
			databases/qdbm

CONFIGURE_STYLE=	gnu

.include <bsd.port.mk>
