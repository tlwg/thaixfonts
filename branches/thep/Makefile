all:
	mkdir -p pcf
	cd dbthaitext_tis620 ; ../scripts/genpcf ; cd ..
	cd etlthai_bdf ; ../scripts/genpcf ; cd ..
	cd manop_bdf ; ../scripts/genpcf ; cd ..
	cd nectec ; ../scripts/genpcf ; cd ..
	cd phaisarn ; ../scripts/genpcf ; cd ..
	cd yenbut_bdf ; ../scripts/genpcf ; cd ..
	cd pcf ; ../scripts/makefont ; cd ..

clean:
	rm -rf pcf

install:
	mkdir -p /usr/share/fonts/TIS-620/misc
	cp -f pcf/* /usr/share/fonts/TIS-620/misc

