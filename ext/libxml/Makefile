
SHELL = /bin/sh

#### Start of system configuration section. ####

srcdir = .
topdir = /System/Library/Frameworks/Ruby.framework/Versions/1.8/usr/lib/ruby/1.8/universal-darwin9.0
hdrdir = $(topdir)
VPATH = $(srcdir):$(topdir):$(hdrdir)
prefix = $(DESTDIR)/System/Library/Frameworks/Ruby.framework/Versions/1.8/usr
exec_prefix = $(prefix)
sitedir = $(DESTDIR)/Library/Ruby/Site
rubylibdir = $(libdir)/ruby/$(ruby_version)
docdir = $(datarootdir)/doc/$(PACKAGE)
dvidir = $(docdir)
datarootdir = $(prefix)/share
archdir = $(rubylibdir)/$(arch)
sbindir = $(exec_prefix)/sbin
psdir = $(docdir)
localedir = $(datarootdir)/locale
htmldir = $(docdir)
datadir = $(datarootdir)
includedir = $(prefix)/include
infodir = $(DESTDIR)/usr/share/info
sysconfdir = $(prefix)/etc
mandir = $(DESTDIR)/usr/share/man
libdir = $(exec_prefix)/lib
sharedstatedir = $(prefix)/com
oldincludedir = $(DESTDIR)/usr/include
pdfdir = $(docdir)
sitearchdir = $(sitelibdir)/$(sitearch)
bindir = $(exec_prefix)/bin
localstatedir = $(prefix)/var
sitelibdir = $(sitedir)/$(ruby_version)
libexecdir = $(exec_prefix)/libexec

CC = gcc
LIBRUBY = $(LIBRUBY_SO)
LIBRUBY_A = lib$(RUBY_SO_NAME)-static.a
LIBRUBYARG_SHARED = -l$(RUBY_SO_NAME)
LIBRUBYARG_STATIC = -l$(RUBY_SO_NAME)

RUBY_EXTCONF_H = extconf.h
CFLAGS   =  -fno-common -arch ppc -arch i386 -Os -pipe -fno-common -I/usr/include/libxml2 -I. -I/System/Library/Frameworks/Ruby.framework/Versions/1.8/usr/lib/ruby/1.8/universal-darwin9.0 -I. -I/usr/local/include 
INCFLAGS = -I. -I. -I/System/Library/Frameworks/Ruby.framework/Versions/1.8/usr/lib/ruby/1.8/universal-darwin9.0 -I. -I/usr/local/include
CPPFLAGS = -DRUBY_EXTCONF_H=\"$(RUBY_EXTCONF_H)\" 
CXXFLAGS = $(CFLAGS) 
DLDFLAGS = -L. -arch ppc -arch i386  
LDSHARED = cc -arch ppc -arch i386 -pipe -bundle -undefined dynamic_lookup
AR = ar
EXEEXT = 

RUBY_INSTALL_NAME = ruby
RUBY_SO_NAME = ruby
arch = universal-darwin9.0
sitearch = universal-darwin9.0
ruby_version = 1.8
ruby = /System/Library/Frameworks/Ruby.framework/Versions/1.8/usr/bin/ruby
RUBY = $(ruby)
RM = rm -f
MAKEDIRS = mkdir -p
INSTALL = /usr/bin/install -c
INSTALL_PROG = $(INSTALL) -m 0755
INSTALL_DATA = $(INSTALL) -m 644
COPY = cp

#### End of system configuration section. ####

preload = 

libpath = . $(libdir) /System/Library/Frameworks/Ruby.framework/Versions/1.8/usr/lib
LIBPATH =  -L"." -L"$(libdir)" -L"/System/Library/Frameworks/Ruby.framework/Versions/1.8/usr/lib"
DEFFILE = 

CLEANFILES = mkmf.log
DISTCLEANFILES = 

extout = 
extout_prefix = 
target_prefix = 
LOCAL_LIBS = 
LIBS = $(LIBRUBYARG_SHARED) -L/usr/lib -lxml2 -lz -lpthread -licucore -lm -liconv -lz -lm  -lpthread -ldl -lm  
SRCS = libxml.c ruby_xml.c ruby_xml_attr.c ruby_xml_attr_decl.c ruby_xml_attributes.c ruby_xml_cbg.c ruby_xml_document.c ruby_xml_dtd.c ruby_xml_encoding.c ruby_xml_error.c ruby_xml_html_parser.c ruby_xml_html_parser_context.c ruby_xml_html_parser_options.c ruby_xml_input_cbg.c ruby_xml_io.c ruby_xml_namespace.c ruby_xml_namespaces.c ruby_xml_node.c ruby_xml_parser.c ruby_xml_parser_context.c ruby_xml_parser_options.c ruby_xml_reader.c ruby_xml_relaxng.c ruby_xml_sax2_handler.c ruby_xml_sax_parser.c ruby_xml_schema.c ruby_xml_xinclude.c ruby_xml_xpath.c ruby_xml_xpath_context.c ruby_xml_xpath_expression.c ruby_xml_xpath_object.c ruby_xml_xpointer.c
OBJS = libxml.o ruby_xml.o ruby_xml_attr.o ruby_xml_attr_decl.o ruby_xml_attributes.o ruby_xml_cbg.o ruby_xml_document.o ruby_xml_dtd.o ruby_xml_encoding.o ruby_xml_error.o ruby_xml_html_parser.o ruby_xml_html_parser_context.o ruby_xml_html_parser_options.o ruby_xml_input_cbg.o ruby_xml_io.o ruby_xml_namespace.o ruby_xml_namespaces.o ruby_xml_node.o ruby_xml_parser.o ruby_xml_parser_context.o ruby_xml_parser_options.o ruby_xml_reader.o ruby_xml_relaxng.o ruby_xml_sax2_handler.o ruby_xml_sax_parser.o ruby_xml_schema.o ruby_xml_xinclude.o ruby_xml_xpath.o ruby_xml_xpath_context.o ruby_xml_xpath_expression.o ruby_xml_xpath_object.o ruby_xml_xpointer.o
TARGET = libxml_ruby
DLLIB = $(TARGET).bundle
EXTSTATIC = 
STATIC_LIB = 

RUBYCOMMONDIR = $(sitedir)$(target_prefix)
RUBYLIBDIR    = $(sitelibdir)$(target_prefix)
RUBYARCHDIR   = $(sitearchdir)$(target_prefix)

TARGET_SO     = $(DLLIB)
CLEANLIBS     = $(TARGET).bundle $(TARGET).il? $(TARGET).tds $(TARGET).map
CLEANOBJS     = *.o *.a *.s[ol] *.pdb *.exp *.bak

all:		$(DLLIB)
static:		$(STATIC_LIB)

clean:
		@-$(RM) $(CLEANLIBS) $(CLEANOBJS) $(CLEANFILES)

distclean:	clean
		@-$(RM) Makefile $(RUBY_EXTCONF_H) conftest.* mkmf.log
		@-$(RM) core ruby$(EXEEXT) *~ $(DISTCLEANFILES)

realclean:	distclean
install: install-so install-rb

install-so: $(RUBYARCHDIR)
install-so: $(RUBYARCHDIR)/$(DLLIB)
$(RUBYARCHDIR)/$(DLLIB): $(DLLIB)
	$(INSTALL_PROG) $(DLLIB) $(RUBYARCHDIR)
install-rb: pre-install-rb install-rb-default
install-rb-default: pre-install-rb-default
pre-install-rb: Makefile
pre-install-rb-default: Makefile
$(RUBYARCHDIR):
	$(MAKEDIRS) $@

site-install: site-install-so site-install-rb
site-install-so: install-so
site-install-rb: install-rb

.SUFFIXES: .c .m .cc .cxx .cpp .C .o

.cc.o:
	$(CXX) $(INCFLAGS) $(CPPFLAGS) $(CXXFLAGS) -c $<

.cxx.o:
	$(CXX) $(INCFLAGS) $(CPPFLAGS) $(CXXFLAGS) -c $<

.cpp.o:
	$(CXX) $(INCFLAGS) $(CPPFLAGS) $(CXXFLAGS) -c $<

.C.o:
	$(CXX) $(INCFLAGS) $(CPPFLAGS) $(CXXFLAGS) -c $<

.c.o:
	$(CC) $(INCFLAGS) $(CPPFLAGS) $(CFLAGS) -c $<

$(DLLIB): $(OBJS)
	@-$(RM) $@
	$(LDSHARED) -o $@ $(OBJS) $(LIBPATH) $(DLDFLAGS) $(LOCAL_LIBS) $(LIBS)



$(OBJS): ruby.h defines.h $(RUBY_EXTCONF_H)
