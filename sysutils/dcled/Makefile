COMMENT =	userland driver for Dream Link USB LED Message Board

V =		2.2
DISTNAME =	dcled-${V}
EXTRACT_SUFX =	.tgz
REVISION =	0

CATEGORIES =	sysutils

HOMEPAGE =	http://www.last-outpost.com/~malakai/dcled/

PERMIT_PACKAGE = Yes

SITES=		http://www.last-outpost.com/~malakai/dcled/

WANTLIB += c m pthread usb-1.0

LIB_DEPENDS =	devel/libusb1

NO_TEST =	Yes

FONTDIR =	${PREFIX}/share/dcled
CFLAGS +=	-DFONTDIR=\"${FONTDIR}\"
CFLAGS +=	-DDCLEDVERSION=\"${V}\"

do-build:
	cd ${WRKSRC} && \
	${CC} ${CFLAGS} `pkg-config --cflags --libs libusb-1.0` -lm dcled.c -o dcled

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/dcled ${PREFIX}/bin
	${INSTALL_DATA_DIR} ${FONTDIR}
	${INSTALL_DATA} ${WRKSRC}/fonts/*.dlf ${FONTDIR}

.include <bsd.port.mk>
