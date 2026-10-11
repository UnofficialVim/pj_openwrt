include $(TOPDIR)/rules.mk

PKG_NAME:=alien-fan
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/alien-fan
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=LM63 fan control for the AmpliFi Alien
  DEPENDS:=+i2c-tools
  PKGARCH:=all
endef

define Package/alien-fan/description
  Drives the LM63 fan PWM from the hottest thermal zone and clears the chip's loud spin-up burst.
endef

define Build/Compile
endef

define Package/alien-fan/install
	$(INSTALL_DIR) $(1)/usr/sbin $(1)/etc/init.d
	$(INSTALL_BIN) ./files/alien-fan $(1)/usr/sbin/alien-fan
	$(INSTALL_BIN) ./files/alien-fan.init $(1)/etc/init.d/alien-fan
endef
