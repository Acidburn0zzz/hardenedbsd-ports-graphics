# Created by: jabley@automagic.org
# $FreeBSD$

PORTNAME=	xml2rfc
PORTVERSION=	2.5.1
CATEGORIES=	textproc
MASTER_SITES=	http://tools.ietf.org/tools/xml2rfc2/cli/

MAINTAINER=	marcus@FreeBSD.org
COMMENT=	Tool to create RFCs and related documents from XML, as per RFC2629

LICENSE=	BSD3CLAUSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}lxml>=2.2.8:devel/py-lxml \
		${PYTHON_PKGNAMEPREFIX}requests>=2.5.0:www/py-requests

USES=		python
USE_PYTHON=	distutils autoplist

.include <bsd.port.mk>
