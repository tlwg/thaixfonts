MAINTAINERCLEANFILES = Makefile.in

SUBDIRS = dbthaitext etlthai manop nectec phaisarn yenbut

fontdir = $(DESTDIR)/@fontdir@

install-data-local:
	if test -e $(fontdir)/fonts.alias ; then \
		mv -f $(fontdir)/fonts.alias $(fontdir)/fonts.alias.old; \
		cat $(fontdir)/fonts.alias.old $(top_srcdir)/thai.alias \
			> $(fontdir)/fonts.alias; \
	else \
		cp -f $(top_srcdir)/thai.alias $(fontdir)/fonts.alias; \
	fi; \
	$(MKFONTDIR) $(fontdir)

uninstall-local:
	if test -e $(fontdir)/fonts.alias.old ; then \
		mv -f $(fontdir)/fonts.alias.old $(fontdir)/fonts.alias; \
	else \
		rm -f $(fontdir)/fonts.alias; \
	fi; \
	$(MKFONTDIR) $(fontdir)

