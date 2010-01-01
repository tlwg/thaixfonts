MAINTAINERCLEANFILES = Makefile.in

SUBDIRS = etlthai manop nectec poonlap yenbut

EXTRA_DIST = Make.rule thai.alias

font_DATA = thai.alias

install-data-hook:
	@if test -n "$(DESTDIR)" ; then \
		echo "***" ; \
		echo "*** Warning: Seems to be binary package building." ; \
		echo "***          So, font list/alias is not generated" ; \
		echo "***" ; \
		exit 0; \
	else \
		if test -e $(DESTDIR)$(fontdir)/fonts.alias ; then \
			cat $(DESTDIR)$(fontdir)/thai.alias \
				>> $(DESTDIR)$(fontdir)/fonts.alias; \
		else \
			cp -f $(DESTDIR)$(fontdir)/thai.alias \
				$(DESTDIR)$(fontdir)/fonts.alias; \
		fi; \
		$(MKFONTDIR) $(DESTDIR)$(fontdir); \
	fi

uninstall-hook:
	if test -e $(DESTDIR)$(fontdir)/fonts.alias.old ; then \
		mv -f $(DESTDIR)$(fontdir)/fonts.alias.old \
			$(DESTDIR)$(fontdir)/fonts.alias; \
	else \
		rm -f $(DESTDIR)$(fontdir)/fonts.alias; \
	fi
	$(MKFONTDIR) $(DESTDIR)$(fontdir)
	if test `head -1 $(DESTDIR)$(fontdir)/fonts.dir` -eq 0; then \
		$(RM) $(DESTDIR)$(fontdir)/fonts.dir; \
		$(RMDIR) $(DESTDIR)$(fontdir); \
	fi

