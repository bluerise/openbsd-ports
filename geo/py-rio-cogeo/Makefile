COMMENT =	cloud optimized GeoTiff creation plugin for rasterio

MODPY_EGG_VERSION =	1.1.10
DISTNAME =	rio-cogeo-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME:S/.dev/pre/}
REVISION =	4

CATEGORIES =	geo

# BSD
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

FLAVORS =	python3
FLAVOR =	python3

MODPY_PYBUILD =	setuptools
MODPY_PI =	Yes

RUN_DEPENDS =	geo/py-rasterio${MODPY_FLAVOR} \
		geo/py-mercantile${MODPY_FLAVOR} \
		geo/py-supermercado${MODPY_FLAVOR} \
		math/py-numpy${MODPY_FLAVOR}>=1.15

# test_read_no_band requires hdf5 support in GDAL
# requires datafiles only on github...
NO_TEST =	Yes

.include <bsd.port.mk>
