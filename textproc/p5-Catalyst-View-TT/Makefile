COMMENT=	Template Toolkit views for Catalyst

DISTNAME =	Catalyst-View-TT-0.46
CATEGORIES=	textproc

# Perl
PERMIT_PACKAGE=	Yes

MODULES=	cpan
PKG_ARCH=	*

RUN_DEPENDS=	devel/p5-Data-Dump \
		devel/p5-Class-Accessor \
		devel/p5-MRO-Compat \
		devel/p5-Path-Class \
		textproc/p5-Template-Timer \
		www/p5-Catalyst-Runtime
TEST_DEPENDS=	textproc/p5-Template-Provider-Encoding

MAKE_ENV=	TEST_POD=Yes

CONFIGURE_STYLE =	modinst

.include <bsd.port.mk>
