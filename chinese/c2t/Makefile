COMMENT=	translate GB/Big5 encoding to tone pinyin

DISTNAME=	zh-c2t-1.0
REVISION=	3
CATEGORIES=	chinese

PERMIT_PACKAGE=	Yes

WANTLIB=		c

SITES=	ftp://ftp.cuhk.hk/pub/chinese/ifcss/software/unix/convert/
SITES.dict=	ftp://ftp.cuhk.hk/pub/chinese/ifcss/software/x-win/cxterm/dict/gb/
DISTFILES=	c2t.tar.gz 
DISTFILES.dict= TONEPY.tit
EXTRACT_ONLY=	c2t.tar.gz

WRKDIST=	${WRKDIR}

NO_TEST=	Yes

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/chinese/gb
	${INSTALL_PROGRAM} ${WRKSRC}/c2t ${PREFIX}/bin
	${INSTALL_DATA} ${FULLDISTDIR}/TONEPY.tit ${PREFIX}/share/chinese/gb
	${INSTALL_MAN} ${WRKSRC}/c2t.1 ${PREFIX}/man/man1

.include <bsd.port.mk>
