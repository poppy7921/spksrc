PKG_NAME = Jackett
PKG_VERS = 0.16.979
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME).Binaries.LinuxAMDx64.$(PKG_EXT)
PKG_DIST_FILE = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/Jackett/Jackett/releases/download/v$(PKG_VERS)
PKG_DIR = jackett
# https://github.com/Jackett/Jackett/archive/v0.16.979.tar.gz
DEPENDS =

HOMEPAGE = https://github.com/Jackett/Jackett
COMMENT  = Jackett works as a proxy server: it translates queries from apps into tracker-site-specific http queries, parses the html response, then sends results back to the requesting software. Jackett is a single repository of maintained indexer scraping & translation logic - removing the burden from other apps.
LICENSE  = GNU GPL v2

CONFIGURE_TARGET = nop
COMPILE_TARGET = nop
INSTALL_TARGET = jackett_install

include ../../mk/spksrc.cross-cc.mk

jackett_install:
	mkdir -p $(STAGING_INSTALL_PREFIX)/share/$(PKG_DIR)
	tar -cf - -C $(WORK_DIR)/$(PKG_NAME) . | tar -xf - -C $(STAGING_INSTALL_PREFIX)/share/$(PKG_DIR)
	# dotnet publish Jackett.Server -f netcoreapp3.1 --self-contained -r linux-x64 -c Debug
	# ./Jackett.Server/bin/Debug/netcoreapp3.1/linux-x64/jackett
