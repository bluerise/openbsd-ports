COMMENT=		library to access data on a CDDB server

DISTNAME=		libcddb-1.3.2
CATEGORIES=		audio devel
SHARED_LIBS +=	cddb                 0.1      # .4.3
REVISION=		1

HOMEPAGE=		https://libcddb.sourceforge.net/

# LGPL
PERMIT_PACKAGE=	Yes

SITES=			${SITE_SOURCEFORGE:=libcddb/}
EXTRACT_SUFX=		.tar.bz2

LIB_DEPENDS=		converters/libiconv

WANTLIB=		c iconv


CONFIGURE_STYLE=	gnu
CONFIGURE_ARGS+=	--without-cdio
CONFIGURE_ENV=		CPPFLAGS="-I${LOCALBASE}/include" \
			LDFLAGS="-L${LOCALBASE}/lib"

.include <bsd.port.mk>
