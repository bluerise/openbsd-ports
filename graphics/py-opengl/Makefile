COMMENT =		Python bindings for OpenGL
MODPY_EGG_VERSION =	3.1.7
DISTNAME =		PyOpenGL-${MODPY_EGG_VERSION}
PKGNAME =		py-opengl-${MODPY_EGG_VERSION}
REVISION =		1

CATEGORIES =		graphics
HOMEPAGE =		https://pyopengl.sourceforge.net/

# BSD
PERMIT_PACKAGE =	Yes

MODULES =		lang/python

FLAVORS =		python3
FLAVOR =		python3

MODPY_PI =		Yes
MODPY_PYBUILD =		setuptools

LIB_DEPENDS =		graphics/freeglut

# multi version py2+3 test infrastructure using virtualenv,
# not handled in this port yet
NO_TEST =	Yes

.include <bsd.port.mk>
