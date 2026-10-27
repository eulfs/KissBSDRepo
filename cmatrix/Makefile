REPO = https://github.com/abishekvashok/cmatrix.git
DIR = /tmp/dist/CMATRIX

.PHONY: all install uninstall

all:
	@mkdir -p /tmp/dist
	@if [ -d "$(DIR)" ]; then \
		cd "$(DIR)" && git pull; \
	else \
		git clone "$(REPO)" "$(DIR)"; \
	fi
	@cd "$(DIR)" && autoreconf -i
	@cd "$(DIR)" && CC=cc ./configure --prefix=/usr/local
	@cd "$(DIR)" && $(MAKE)

install: all
	@cd "$(DIR)" && $(MAKE) install

uninstall:
	@if [ -d "$(DIR)" ]; then \
		cd "$(DIR)" && $(MAKE) uninstall; \
	fi
