# Created by: Kevin Golding <ports@caomhin.org>
# $FreeBSD: head/www/py-django-registration-redux/Makefile 415799 2016-05-24 16:10:21Z amdmi3 $

PORTNAME=	django-registration-redux
PORTVERSION=	1.4
CATEGORIES=	www python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ports@caomhin.org
COMMENT=	User-registration application for Django

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}django18>=0:www/py-django18

NO_ARCH=	yes
USES=		python
USE_PYTHON=	distutils autoplist

CONFLICTS_INSTALL=	pootle-* py-django-registration

.include <bsd.port.mk>
