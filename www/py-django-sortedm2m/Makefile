# Created by: Kevin Golding <ports@caomhin.org>
# $FreeBSD: head/www/py-django-sortedm2m/Makefile 415797 2016-05-24 16:08:13Z amdmi3 $

PORTNAME=	django-sortedm2m
PORTVERSION=	1.2.2
CATEGORIES=	www python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ports@caomhin.org
COMMENT=	Replacement for Django's many to many field

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

RUN_DEPENDS=	${PYTHON_SITELIBDIR}/django/bin/django-admin.py:www/py-django18

NO_ARCH=	yes
USES=		python
USE_PYTHON=	distutils autoplist

.include <bsd.port.mk>
