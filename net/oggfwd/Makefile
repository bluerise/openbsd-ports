COMMENT=	pipe an Ogg stream to an Icecast server

DISTNAME=	oggfwd-0.2
REVISION=	2
CATEGORIES=	net multimedia

HOMEPAGE=	http://v2v.cc/~j/ffmpeg2theora/oggfwd/

# GPLv2
PERMIT_PACKAGE=	Yes

WANTLIB=	c m ogg pthread theora vorbis shout>=5 speex>=4

SITES=		http://v2v.cc/~j/oggfwd/

LIB_DEPENDS=	net/libshout \
		audio/speex

NO_TEST=	Yes

.include <bsd.port.mk>
