COMMENT=	access to PostgreSQL databases perl

VERSION=	1.9.0
DISTNAME=	pgsql_perl5-${VERSION}
PKGNAME=	p5-pgsql-${VERSION}
REVISION=	6
CATEGORIES=	databases perl5
SITES=		${SITE_PERL_CPAN:=Pg/}

LIB_DEPENDS =	databases/postgresql

PERMIT_PACKAGE=	Yes

WANTLIB += c perl pq>=3

CONFIGURE_ENV+=	POSTGRES_HOME="${LOCALBASE}" \
		POSTGRES_LIB="${LOCALBASE}/lib" \
		POSTGRES_INCLUDE="${LOCALBASE}/include/postgresql"

CONFIGURE_STYLE=perl

# needs a database properly set up
NO_TEST=	Yes

.include <bsd.port.mk>
