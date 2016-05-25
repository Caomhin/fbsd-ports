# Created by: Kevin Golding <ports@caomhin.org>
# $FreeBSD: head/www/py-django-happenings/Makefile 412351 2016-04-01 14:33:55Z mat $

PORTNAME=	django-happenings
PORTVERSION=	0.3.3
CATEGORIES=	www python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ports@caomhin.org
COMMENT=	Event calendar app for Django

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}django18>=0:www/py-django18 \
		${PYTHON_PKGNAMEPREFIX}pytz>0:devel/py-pytz

USES=		python
USE_PYTHON=	distutils autoplist

.include <bsd.port.mk>
