if AIGLX
GLXDRI_LIBRARY = libglxdri.la
endif

noinst_LTLIBRARIES = libglx.la $(GLXDRI_LIBRARY)

AM_CFLAGS = \
	-I@MESA_SOURCE@/include \
	@DIX_CFLAGS@ \
	@GL_CFLAGS@ \
	@XLIB_CFLAGS@ \
	@LIBDRM_CFLAGS@ \
	@DRIPROTO_CFLAGS@ \
	-I@MESA_SOURCE@/src/mesa/glapi \
	-I@MESA_SOURCE@/src/mesa/main \
	-DXFree86Server \
	@GLX_DEFINES@ \
	@GLX_ARCH_DEFINES@

# none yet
#sdk_HEADERS =

INCLUDES = \
	-I$(top_srcdir)/hw/xfree86/os-support \
	-I$(top_srcdir)/hw/xfree86/os-support/bus \
	-I$(top_srcdir)/hw/xfree86/common \
	-I$(top_srcdir)/hw/xfree86/dri \
	-I$(top_srcdir)/hw/xfree86/dri2 \
	-I$(top_srcdir)/mi


nodist_libglx_la_SOURCES = indirect_size.h \
			   glapi.c \
			   glthread.c \
			   indirect_dispatch.c \
			   indirect_dispatch.h \
			   indirect_dispatch_swap.c \
			   indirect_reqsize.c \
			   indirect_reqsize.h \
			   indirect_size_get.c \
			   indirect_size_get.h \
			   indirect_table.c

libglxdri_la_SOURCES = \
        glxdri.c \
        glxdri2.c \
        extension_string.c \
        extension_string.h

#if XQUARTZ
XQUARTZ_libglx_la_SOURCES = glcontextmodes.c
#endif

libglx_la_SOURCES = \
	$(XQUARTZ_libglx_la_SOURCES) \
        g_disptab.h \
        glxbyteorder.h \
        glxcmds.c \
        glxcmdsswap.c \
        glxcontext.h \
        glxdrawable.h \
        glxext.c \
        glxext.h \
        glxglcore.c \
        glxscreens.c \
        glxscreens.h \
        glxserver.h \
        glxutil.c \
        glxutil.h \
        indirect_program.c \
        indirect_table.h \
        indirect_texture_compression.c \
        indirect_util.c \
        indirect_util.h \
        render2.c \
        render2swap.c \
        renderpix.c \
        renderpixswap.c \
        rensize.c \
        single2.c \
        single2swap.c \
        singlepix.c \
        singlepixswap.c \
        singlesize.c \
        singlesize.h \
        swap_interval.c \
        unpack.h \
        xfont.c
