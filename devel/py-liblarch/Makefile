COMMENT=	Python library to easily handle data structure

MODPY_EGG_VERSION=	3.2.0
GH_ACCOUNT=	getting-things-gnome
GH_PROJECT=	liblarch
GH_TAGNAME=	v${MODPY_EGG_VERSION}
PKGNAME=	py-liblarch-${MODPY_EGG_VERSION}
REVISION=	2

CATEGORIES=	devel

# GPLv3+
PERMIT_PACKAGE=	Yes

MODULES=	lang/python
MODPY_PYBUILD=	setuptools
# failures in test_liblarch.py: Trace/BPT trap
MODPY_PYTEST_ARGS= -v

RUN_DEPENDS=	devel/py-gobject3${MODPY_FLAVOR}
TEST_DEPENDS=	devel/py-nose${MODPY_FLAVOR}

TEST_IS_INTERACTIVE=	x11

FLAVORS=	python3
FLAVOR=		python3

.include <bsd.port.mk>
