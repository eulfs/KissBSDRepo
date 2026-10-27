REPO = https://github.com/mtoyoda/sl.git
DIR = /tmp/dist/SL
BINDIR = /usr/local/bin

.PHONY: all install uninstall

all:
	@mkdir -p /tmp/dist
	@if [ -d "$(DIR)" ]; then \
		cd "$(DIR)" && git pull; \
	else \
		git clone "$(REPO)" "$(DIR)"; \
	fi
	@cd "$(DIR)" && $(MAKE) CC=cc

install: all
	@cd "$(DIR)" && mkdir -p $(BINDIR)
	@cd "$(DIR)" && cp sl $(BINDIR)/sl
	@cd "$(DIR)" && chmod 755 $(BINDIR)/sl

uninstall:
	@rm -f $(BINDIR)/sl
