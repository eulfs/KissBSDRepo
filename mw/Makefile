REPO = https://github.com/pixelyblah/MeoW
DIR = /tmp/dist/MeoW

.PHONY: all install

all: install

install:
	@if [ -d "$(DIR)" ]; then \
		cd "$(DIR)" && git pull; \
	else \
		git clone "$(REPO)" "$(DIR)"; \
	fi
	@cd "$(DIR)" && cargo install --path . --root /usr/local
