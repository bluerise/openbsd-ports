COMMENT =		html/xml templating engine

MODPY_EGG_VERSION =	2.0.1
DISTNAME =		meld3-${MODPY_EGG_VERSION}
PKGNAME =		py-${DISTNAME:L}
REVISION =		3

CATEGORIES =		www textproc

HOMEPAGE =		https://github.com/supervisor/meld3

# MIT
PERMIT_PACKAGE =	Yes

MODPY_PI =		Yes

MODULES =		lang/python

FLAVORS =		python3
FLAVOR =		python3

MODPY_PYBUILD =		setuptools

DOCS =		${PREFIX}/share/doc/${MODPY_PY_PREFIX}meld3

post-install:
	${INSTALL_DATA_DIR} ${DOCS}
	${INSTALL_DATA} ${WRKSRC}/README.txt ${DOCS}

.include <bsd.port.mk>
