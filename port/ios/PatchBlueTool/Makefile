#TARGET := iphone:clang
#TARGET_IPHONEOS_DEPLOYMENT_VERSION = 3.0
#ARCHS = armv7
ARCHS = arm64
TARGET = appletv
export GO_EASY_ON_ME=1
export SDKVERSION=10.2
THEOS_DEVICE_IP=apple-tv.local 

TOOL_NAME = PatchBlueTool

PatchBlueTool_FILES = PatchBlueTool.c
PatchBlueTool_CODESIGN_FLAGS=-S../ent.plist
include $(THEOS)/makefiles/common.mk
include $(THEOS_MAKE_PATH)/tool.mk
