# Created by: Stas Timokhin <devel@stasyan.com>
# $FreeBSD$

PORTNAME=	cups-libs
PORTVERSION=	1.3.11
PORTREVISION=	1
CATEGORIES=	print linux

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	Common UNIX Printing System libraries

USES=		linux:f10
USE_LINUX=	gnutls
USE_LINUX_RPM=	yes
SRC_DISTFILES=	cups-${PORTVERSION}-${RPMVERSION}.src.rpm:SOURCE
RPMVERSION=	4.fc10
USE_LDCONFIG=	yes

PLIST_FILES=	usr/lib/libcups.so.2 usr/lib/libcupsimage.so.2
DESCR=		${.CURDIR}/../cups/pkg-descr

.include <bsd.port.mk>
