#
# Copyright (C) 2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=aria-ng
PKG_VERSION:=0.1.0-b3
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://github.com/mayswind/AriaNg/releases/download/0.1.0-b3/
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).zip

PKG_LICENSE:=LGPL-3.0

include $(INCLUDE_DIR)/package.mk

define Package/aria-ng
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Download Manager
  DEPENDS:=
  TITLE:=aria-ng aria2 web frontend
  URL:=https://github.com/mayswind/AriaNg
  PKGARCH:=all
endef

define Package/aria-ng/description
	Aria-ng is Aria2 Web Frontend.
endef

define Build/Compile
endef

define Package/aria-ng/install
	$(INSTALL_DIR) $(1)/www/aria-ng
	$(CP) $(PKG_BUILD_DIR)/js $(1)/www/aria-ng
	$(CP) $(PKG_BUILD_DIR)/langs $(1)/www/aria-ng
	$(CP) $(PKG_BUILD_DIR)/css $(1)/www/aria-ng
	$(CP) $(PKG_BUILD_DIR)/fonts $(1)/www/aria-ng
	$(CP) $(PKG_BUILD_DIR)/views $(1)/www/aria-ng
	$(CP) $(PKG_BUILD_DIR)/index.html $(1)/www/aria-ng
endef

$(eval $(call BuildPackage,aria-ng))
