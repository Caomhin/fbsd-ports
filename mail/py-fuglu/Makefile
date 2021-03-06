# Created by: Kevin Golding <ports@caomhin.org>
# $FreeBSD$

PORTNAME=	fuglu
PORTVERSION=	0.6.6
CATEGORIES=	mail python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ports@caomhin.org
COMMENT=	Mail scanning daemon for Postfix written in Python

LICENSE=	APACHE20

RUN_DEPENDS=	postfix:mail/postfix \
		${PYTHON_PKGNAMEPREFIX}six>0:devel/py-six

USES=	python:2.4+
USE_PYTHON=	autoplist distutils

USE_RC_SUBR=	fuglu

LOGDIR=	/var/log/fuglu
PLIST_DIRS+=	${LOGDIR}

OPTIONS_DEFINE=	BEAUTIFULSOUP CLAMAV DKIM MAGIC SPAMASSASSIN SPF SQL
OPTIONS_DEFAULT=	BEAUTIFULSOUP CLAMAV DKIM MAGIC SPAMASSASSIN SPF

BEAUTIFULSOUP_DESC=	Use BeautifulSoup for improved html processing
CLAMAV_DESC=	Use ClamAV
DKIM_DESC=	Use DKIM (in FuGlu)
MAGIC_DESC=	Use mime magic bindings for attachment detection
SPAMASSASSIN_DESC=	Use SpamAssassin
SPF_DESC=	Use SPF (in FuGlu)
SQL_DESC=	Use SQL

BEAUTIFULSOUP_RUN_DEPENDS=	${PYTHON_SITELIBDIR}/bs4/__init__.py:www/py-beautifulsoup
CLAMAV_RUN_DEPENDS=	clamd:security/clamav
DKIM_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}dkimpy>0:mail/py-dkimpy
MAGIC_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}magic>0:devel/py-magic
SPAMASSASSIN_RUN_DEPENDS=	spamassassin>=0:mail/spamassassin
SPF_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}pyspf>0:mail/py-pyspf
SQL_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}sqlalchemy10>=1.0:databases/py-sqlalchemy10

post-extract:
	@${REINPLACE_CMD} -e "s|'/etc|'etc|g" ${WRKSRC}/setup.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/compareconfig.py
	@${REINPLACE_CMD} -e "s|=/etc|=${PREFIX}/etc|g" ${WRKSRC}/conf/fuglu.conf.dist
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/fuglu/plugins/actionoverride.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/fuglu/plugins/archive.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/fuglu/plugins/attachment.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/fuglu/plugins/domainauth.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/fuglu/plugins/p_fraction.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/fuglu/plugins/p_skipper.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/fuglu/plugins/script.py
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/startscript/fuglu
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/tools/fuglu_conf
	@${REINPLACE_CMD} -e "s|'/etc|'${PREFIX}/etc|g" ${WRKSRC}/src/tools/fuglu_debug

post-install:
	@${MKDIR} ${STAGEDIR}${LOGDIR}

.include <bsd.port.mk>
