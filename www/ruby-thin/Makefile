COMMENT =	fast and very simple Ruby web server

DISTNAME =	thin-1.8.2
CATEGORIES =	www

HOMEPAGE =	http://code.macournoyer.com/thin/

# Ruby/GPLv2
PERMIT_PACKAGE =	Yes

MODULES =	lang/ruby
CONFIGURE_STYLE = ruby gem ext

BUILD_DEPENDS =	${RUN_DEPENDS}
RUN_DEPENDS =	www/ruby-rack,${MODRUBY_FLAVOR}>=1.0,<3.0 \
		devel/ruby-daemons,${MODRUBY_FLAVOR}>=1.0.9,<2.0 \
		net/ruby-eventmachine,${MODRUBY_FLAVOR}>=1.0.4,<2.0

.include <bsd.port.mk>
