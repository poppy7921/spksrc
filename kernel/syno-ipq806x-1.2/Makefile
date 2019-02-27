ARCH ?= ipq806x
TCVERSION ?= 1.2
PKG_NAME = ipq806x
PKG_ARCH = $(PKG_NAME)
PKG_EXT = tar.xz
PKG_DIST_NAME = linux-4.4.x.$(PKG_EXT)
PKG_DIST_SITE = https://seby.io/download/synology-rt2600ac

PKG_DIST_FILE = $(PKG_NAME)-$(PKG_DIST_NAME)
PKG_EXTRACT = linux-4.4.x
SYNO_CONFIG = synoconfigs/$(ARCH)
BASE_ARCH = arm

HOMEPAGE = https://www.synology.com/

include ../../mk/spksrc.kernel-modules.mk
