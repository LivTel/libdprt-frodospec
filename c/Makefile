# $Header: /space/home/eng/cjm/cvs/libdprt-frodospec/c/Makefile,v 0.15 2008-07-17 10:50:18 cjm Exp $

include	../../../Makefile.common
include	../../Makefile.common
include	../Makefile.common

LIBNAME		= $(LIBDPRT_HOME)_$(FRODOSPEC_HOME)
INCDIR 		= $(LIBDPRT_FRODOSPEC_SRC_HOME)/include
DOCSDIR 	= $(LIBDPRT_FRODOSPEC_DOC_HOME)/cdocs
BINDIR		= $(LIBDPRT_FRODOSPEC_BIN_HOME)/c/$(HOSTTYPE)
CFLAGS 		= -g $(CCHECKFLAG) -I$(INCDIR) -I$(CFITSIOINCDIR) -I$(JNIINCDIR) -I$(JNIMDINCDIR) \
		-I$(JNIGENERALINCDIR) -L$(LT_LIB_HOME)
LINTFLAGS 	= -I$(INCDIR) -I$(JNIINCDIR) -I$(JNIMDINCDIR)
DOCFLAGS 	= -static
SRCS 		= dprt.c ngat_dprt_frodospec_DpRtLibrary.c
HEADERS		= $(SRCS:%.c=%.h)
OBJS		= $(SRCS:%.c=$(BINDIR)/%.o)
DOCS 		= $(SRCS:%.c=$(DOCSDIR)/%.html)
LIBS		= -lcfitsio -ldprt_jni_general

top: shared docs

shared: $(INCDIR)/ngat_dprt_frodospec_DpRtLibrary.h $(LT_LIB_HOME)/$(LIBNAME).so

$(INCDIR)/ngat_dprt_frodospec_DpRtLibrary.h: $(DPRT_BIN_HOME)/java/ngat/dprt/frodospec/DpRtLibrary.class
	$(JAVAH) -jni -d $(INCDIR) -classpath $(DPRT_BIN_HOME)/java:$(CLASSPATH) ngat.dprt.frodospec.DpRtLibrary
	$(TOUCH) $@

$(LT_LIB_HOME)/$(LIBNAME).so: $(OBJS)
	$(CC) $(CCSHAREDFLAG) $(CFLAGS) $(OBJS) -o $@ $(TIMELIB) $(LIBS) $(SOCKETLIB)

$(BINDIR)/%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

static: $(LT_LIB_HOME)/$(LIBNAME).a

$(LT_LIB_HOME)/$(LIBNAME).a: $(OBJS)
	ar rcv $@ $?

docs: $(DOCS)

$(DOCS) : $(SRCS)
	-$(CDOC) -d $(DOCSDIR) -h $(INCDIR) $(DOCFLAGS) $(SRCS)

# dont checkout ngat_dprt_frodospec_DpRtLibrary.h - it is a machine built header
checkout:
	$(CO) $(CO_OPTIONS) $(SRCS)
	cd $(INCDIR); $(CO) $(CO_OPTIONS) dprt.h;

# dont checkin ngat_dprt_frodospec_DpRtLibrary.h - it is a machine built header
checkin:
	-$(CI) $(CI_OPTIONS) $(SRCS)
	-(cd $(INCDIR); $(CI) $(CI_OPTIONS) dprt.h;)

staticdepend:
	makedepend $(MAKEDEPENDFLAGS) -p$(BINDIR)/ -- $(CFLAGS)  -- $(SRCS)

depend:
	makedepend $(MAKEDEPENDFLAGS) -p$(BINDIR)/ -- $(CFLAGS)  -- $(SRCS)

lint:
	$(LINT)	$(LINTFLAGS) $(SRCS)

clean:
	-$(RM) $(RM_OPTIONS) $(OBJS) $(LT_LIB_HOME)/$(LIBNAME).so $(LT_LIB_HOME)/$(LIBNAME).a 
	-$(RM) $(RM_OPTIONS) $(INCDIR)/ngat_dprt_frodospec_DpRtLibrary.h $(TIDY_OPTIONS)

tidy:
	-$(RM)  $(RM_OPTIONS) $(TIDY_OPTIONS)
	-cd $(INCDIR); $(RM) $(RM_OPTIONS) $(TIDY_OPTIONS);

backup: tidy
	-$(RM) $(RM_OPTIONS) $(OBJS)

#
# $Log: not supported by cvs2svn $
#

# DO NOT DELETE

/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/stdio.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/iso/stdio_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/sys/feature_tests.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/sys/isa_defs.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/sys/va_list.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/stdio_tag.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/stdio_impl.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/stdlib.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/iso/stdlib_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/string.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/iso/string_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/math.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/iso/math_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /space/home/dev/src/cfitsio3.006/include/fitsio.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/limits.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/iso/limits_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /space/home/dev/src/cfitsio3.006/include/longnam.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /space/home/dev/src/libdprt/jni_general/include/dprt_jni_general.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/local/j2sdk1.4.2_12/include/jni.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/stdarg.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/include/iso/stdarg_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /usr/local/j2sdk1.4.2_12/include/solaris/jni_md.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/dprt.o: /space/home/dev/src/libdprt/frodospec/include/dprt.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/stdio.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/iso/stdio_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/sys/feature_tests.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/sys/isa_defs.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/sys/va_list.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/stdio_tag.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/stdio_impl.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/stdlib.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/iso/stdlib_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/string.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/iso/string_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/local/j2sdk1.4.2_12/include/jni.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/stdarg.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/include/iso/stdarg_iso.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /usr/local/j2sdk1.4.2_12/include/solaris/jni_md.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /space/home/dev/src/libdprt/frodospec/include/ngat_dprt_frodospec_DpRtLibrary.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /space/home/dev/src/libdprt/frodospec/include/dprt.h
/space/home/dev/bin/libdprt/frodospec/c/sun4/ngat_dprt_frodospec_DpRtLibrary.o: /space/home/dev/src/libdprt/jni_general/include/dprt_jni_general.h
