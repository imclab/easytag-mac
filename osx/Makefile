all: EasyTAG.dmg

EasyTAG.dmg: build/EasyTAG.app build/Applications
	hdiutil create EasyTAG.dmg -volname "EasyTAG" -fs HFS+ -srcfolder build

build/EasyTAG.app: EasyTAG.bundle Info.plist gtkrc launcher.sh
	gtk-mac-bundler $<

build/Applications:
	ln -s /Applications $@

clean:
	rm -rf build EasyTAG.dmg

PHONY: clean all
