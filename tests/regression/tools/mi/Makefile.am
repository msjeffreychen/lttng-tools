AM_CPPFLAGS = -I$(top_srcdir)/include

noinst_PROGRAMS = validate_xml extract_xml
validate_xml_SOURCES = validate_xml.c
validate_xml_CPPFLAGS = $(XML_CPPFLAGS) $(AM_CPPFLAGS)
validate_xml_LDADD = $(XML_LIBS)

extract_xml_SOURCES = extract_xml.c
extract_xml_CPPFLAGS = $(XML_CPPFLAGS) $(AM_CPPFLAGS)
extract_xml_LDADD = $(XML_LIBS)

noinst_SCRIPTS = test_mi
EXTRA_DIST = test_mi

all-local:
	@if [ x"$(srcdir)" != x"$(builddir)" ]; then \
		for script in $(EXTRA_DIST); do \
			cp -f $(srcdir)/$$script $(builddir); \
		done; \
	fi

clean-local:
	@if [ x"$(srcdir)" != x"$(builddir)" ]; then \
		for script in $(EXTRA_DIST); do \
			rm -f $(builddir)/$$script; \
		done; \
	fi
