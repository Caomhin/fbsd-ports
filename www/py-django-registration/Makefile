# Created by: Kevin Golding <ports@caomhin.org>
# $FreeBSD: head/www/py-django-registration/Makefile 412351 2016-04-01 14:33:55Z mat $

PORTNAME=	django-registration
PORTVERSION=	2.0.4
CATEGORIES=	www python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ports@caomhin.org
COMMENT=	User-registration application for Django

LICENSE=	BSD3CLAUSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}django18>=1.4:www/py-django18

USES=		python
USE_PYTHON=	distutils autoplist

CONFLICTS_INSTALL=	pootle-*

.include <bsd.port.mk>
