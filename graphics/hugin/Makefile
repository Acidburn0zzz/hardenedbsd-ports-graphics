# Created by: Carlos Eduardo G. Carvalho <cartola@openit.com.br>
# $FreeBSD$

PORTNAME=	hugin
PORTVERSION=	2016.2.0
DISTVERSION=	2016.2.0
WRKSRC=		${WRKDIR}/hugin-2016.2.0
PORTREVISION=	1
CATEGORIES=	graphics
MASTER_SITES=	SF/${PORTNAME}/${PORTNAME}/${PORTNAME}-${PORTVERSION:R}

MAINTAINER=	grog@FreeBSD.org
COMMENT=	GUI for Panorama Tools, to stitch panoramic images

LIB_DEPENDS=	libIlmImf.so:graphics/OpenEXR \
		libImath.so:graphics/ilmbase \
		libboost_thread.so:devel/boost-libs \
		liblcms2.so:graphics/lcms2 \
		libexiv2.so:graphics/exiv2 \
		libfftw3.so:math/fftw3 \
		libpano13.so:graphics/libpano13 \
		libsqlite3.so:databases/sqlite3 \
		libvigraimpex.so:graphics/vigra \
		libpng.so:graphics/png \
		libtiff.so:graphics/tiff
# gmake is really needed at _runtime_.   Do not remove it from this list.
RUN_DEPENDS=	enblend>=4.1.4:graphics/enblend \
		exiftool:graphics/p5-Image-ExifTool \
		gmake:devel/gmake

BROKEN_FreeBSD_9=	does not build

USES=		cmake compiler:c++11-lib desktop-file-utils \
		gettext jpeg pkgconfig shared-mime-info tar:bzip2
CMAKE_ARGS=	-DwxWidgets_CONFIG_EXECUTABLE=${WX_CONFIG}
USE_WX=		3.0+
USE_GL=		glew glut
INSTALLS_ICONS=	yes

OPTIONS_DEFINE=		PANOMATIC AUTOPANOSIFTC PYTHON
OPTIONS_DEFAULT=	PANOMATIC AUTOPANOSIFTC PYTHON
OPTIONS_SUB=		yes

PANOMATIC_DESC=		Install graphics/panomatic
PANOMATIC_RUN_DEPENDS=	panomatic:graphics/panomatic

AUTOPANOSIFTC_DESC=	Install graphics/autopano-sift-c
AUTOPANOSIFTC_RUN_DEPENDS=	autopano:graphics/autopano-sift-c

PYTHON_DESC=		Python Scripting Interface
PYTHON_USES=		python
PYTHON_BUILD_DEPENDS=	swig2.0:devel/swig20
PYTHON_CMAKE_ON=	-DBUILD_HSI=ON
PYTHON_CMAKE_OFF=	-DBUILD_HSI=OFF

.include <bsd.port.mk>
