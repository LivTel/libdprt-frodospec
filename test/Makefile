# $Header: /space/home/eng/cjm/cvs/libdprt-frodospec/test/Makefile,v 1.2 2008-07-17 10:49:58 cjm Exp $

include	../../../Makefile.common
include ../../Makefile.common
include ../Makefile.common

LIBNAME		= $(LIBDPRT_HOME)_$(FRODOSPEC_HOME)
INCDIR 		= $(LIBDPRT_FRODOSPEC_SRC_HOME)/include
DOCSDIR 	= $(LIBDPRT_FRODOSPEC_DOC_HOME)/test
DOCFLAGS 	= -static
BINDIR		= $(LIBDPRT_FRODOSPEC_BIN_HOME)/test/${HOSTTYPE}

CFLAGS 		= -g -I$(INCDIR) -I$(JNIINCDIR) -I$(JNIMDINCDIR) -I$(JNIGENERALINCDIR) 

SRCS 		= dprt_test.c
OBJS 		= $(SRCS:%.c=$(BINDIR)/%.o)
DOCS 		= $(SRCS:%.c=$(DOCSDIR)/%.html)

top: ${BINDIR}/dprt_test docs

${BINDIR}/dprt_test: $(BINDIR)/dprt_test.o $(LT_LIB_HOME)/$(LIBNAME).so
	$(CC) -o $@ $(BINDIR)/dprt_test.o -L$(LT_LIB_HOME) -ldprt_frodospec -ldprt_jni_general $(TIMELIB) -lm -lc

$(BINDIR)/%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

docs: $(DOCS)

$(DOCS) : $(SRCS)
	-$(CDOC) -d $(DOCSDIR) -h $(INCDIR) $(DOCFLAGS) $(SRCS)

depend:
	makedepend $(MAKEDEPENDFLAGS) -p$(BINDIR)/ -- $(CFLAGS) -- $(SRCS)

clean:
	-$(RM) $(RM_OPTIONS) ${BINDIR}/dprt_test $(OBJS) $(TIDY_OPTIONS)

tidy:
	-$(RM) $(RM_OPTIONS) $(TIDY_OPTIONS)

backup: tidy
	-$(RM) $(RM_OPTIONS) $(LIBDPRT_BIN_HOME)/test/dprt_test

checkin:
	-$(CI) $(CI_OPTIONS) $(SRCS)

checkout:
	$(CO) $(CO_OPTIONS) $(SRCS)

#
# $Log: not supported by cvs2svn $
# Revision 1.1  2005/03/11 11:56:57  cjm
# Initial revision
#
#

# DO NOT DELETE

/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/stdio.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/iso/stdio_iso.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/feature_tests.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/isa_defs.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/va_list.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/stdio_tag.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/stdio_impl.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/stdlib.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/iso/stdlib_iso.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/strings.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/types.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/machtypes.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/int_types.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/select.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/time.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/sys/time.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/string.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/iso/string_iso.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /space/home/dev/src/libdprt/frodospec/include/dprt.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /space/home/dev/src/libdprt/jni_general/include/dprt_jni_general.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/local/j2sdk1.4.2_12/include/jni.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/stdarg.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/include/iso/stdarg_iso.h
/space/home/dev/bin/libdprt/frodospec/test/sun4/dprt_test.o: /usr/local/j2sdk1.4.2_12/include/solaris/jni_md.h
