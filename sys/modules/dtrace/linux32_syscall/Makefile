# $FreeBSD: src/sys/modules/dtrace/sdt/Makefile,v 1.1.4.1 2009/08/03 08:13:06 kensmith Exp $

.include "../../Makefile.inc"

.PATH: ${NETBSDSRCDIR}/external/cddl/osnet/dev/systrace

KMOD=		dtrace_syscall_linux32
SRCS=		systrace.c

CPPFLAGS+=	-I${NETBSDSRCDIR}/external/cddl/osnet/sys \
		-I${NETBSDSRCDIR}/external/cddl/osnet/dist/uts/common \
		-I${NETBSDSRCDIR}/external/cddl/osnet/dev/dtrace

WARNS=		4

CPPFLAGS+=	-Wno-unknown-pragmas

CPPFLAGS+=	${${ACTIVE_CC} == "gcc" :? -Wno-discarded-qualifiers :}
CPPFLAGS+=	${${ACTIVE_CC} == "clang" :? -Wno-incompatible-pointer-types-discards-qualifiers :}

.include <bsd.kmodule.mk>
