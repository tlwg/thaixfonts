MAINTAINERCLEANFILES = Makefile.in

SUBDIRS = dbthaitext etlthai manop nectec phaisarn yenbut

EXTRA_DIST = Make.rule

fontdir = @fontdir@

font_DATA = thai.alias

install-data-local:
	if test -e $(DESTDIR)$(fontdir)/fonts.alias ; then \
		mv -f $(DESTDIR)$(fontdir)/fonts.alias \
			$(DESTDIR)$(fontdir)/fonts.alias.old; \
		cat $(DESTDIR)$(fontdir)/fonts.alias.old \
			$(DESTDIR)$(fontdir)/thai.alias \
			> $(DESTDIR)$(fontdir)/fonts.alias; \
	else \
		cp -f $(DESTDIR)$(fontdir)/thai.alias \
			$(DESTDIR)$(fontdir)/fonts.alias; \
	fi
	$(MKFONTDIR) $(DESTDIR)$(fontdir)

uninstall-local:
	if test -e $(DESTDIR)$(fontdir)/fonts.alias.old ; then \
		mv -f $(DESTDIR)$(fontdir)/fonts.alias.old \
			$(DESTDIR)$(fontdir)/fonts.alias; \
	else \
		rm -f $(DESTDIR)$(fontdir)/fonts.alias; \
	fi
	$(MKFONTDIR) $(DESTDIR)$(fontdir)

