# this uses rpetrich's lipoplastic feature not present in dhowett's repository
# you need to install Xcode 4.4.1 as /Applications/Xcode-4.4.1.app

ARCHS = arm64
TARGET = appletv
export GO_EASY_ON_ME=1
export SDKVERSION=10.2
THEOS_DEVICE_IP=btv.local 

SUBPROJECTS = src example PatchBlueTool #PrefsBundle

include $(THEOS)/makefiles/common.mk
include $(THEOS_MAKE_PATH)/aggregate.mk

distclean:
	rm -rf layout btstack_config.h src/Makefile example/Makefile Makefile
