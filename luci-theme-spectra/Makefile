#
# Copyright (C) 2008-2019 Jerrykuku
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

LUCI_TITLE:=Spectra Theme
LUCI_DEPENDS:=+curl +luci-app-spectra-config
PKG_VERSION:=27.472.65783~d87c578

LUCI_MINIFY_CSS:=0

include $(TOPDIR)/feeds/luci/luci.mk

define Package/$(LUCI_PKGNAME)/install
    $(INSTALL_DIR) $(1)/usr/libexec/spectra
    $(INSTALL_BIN) ./root/usr/libexec/spectra/bing_wallpaper $(1)/usr/libexec/spectra/
    $(INSTALL_BIN) ./root/usr/libexec/spectra/online_wallpaper $(1)/usr/libexec/spectra/
    chmod 0755 $(1)/usr/libexec/spectra/bing_wallpaper
    chmod 0755 $(1)/usr/libexec/spectra/online_wallpaper
endef

# call BuildPackage - OpenWrt buildroot signature
