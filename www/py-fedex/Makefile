# Created by: Kevin Golding <ports@caomhin.org>
# $FreeBSD: head/www/py-fedex/Makefile 412351 2016-04-01 14:33:55Z mat $

PORTNAME=	fedex
PORTVERSION=	2.3.1
CATEGORIES=	www python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ports@caomhin.org
COMMENT=	Light wrapper around Fedex's Web Services SOAP API using suds

LICENSE=	BSD3CLAUSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}suds>=0:net/py-suds

NO_ARCH=	yes
USES=		python:2
USE_PYTHON=	autoplist distutils

.include <bsd.port.mk>
