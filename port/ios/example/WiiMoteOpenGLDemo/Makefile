# uses Dustin Howett's theos-build system
# http://bit.ly/af0Evu
# http://hwtt.net/ths
ARCHS = arm64
TARGET = appletv
export GO_EASY_ON_ME=1
export SDKVERSION=10.2
THEOS_DEVICE_IP=apple-tv.local 


include $(THEOS)/makefiles/common.mk



BTSTACK_ROOT=../../../..

APPLICATION_NAME = WiiMoteOpenGLDemo

VPATH += ../../CocoaTouch/src

WiiMoteOpenGLDemo_FILES = $(wildcard *.c) $(wildcard *.m) $(wildcard Classes/*.m)
WiiMoteOpenGLDemo_FILES += ../../CocoaTouch/src/BTstackManager.m ../../CocoaTouch/src/BTDiscoveryViewController.m ../../CocoaTouch/src/BTDevice.m
WiiMoteOpenGLDemo_CFLAGS = -I ~/Projects/btstack/src/ -I ~/Projects/btstack/platform/daemon/src  -I. -I../.. -I Classes -I ~/Projects/btstack/port/ios/CocoaTouch/include/BTstack/ -I ~/Projects/btstack/platform/corefoundation -I $(BTSTACK_ROOT)/include -I ../../CocoaTouch/include
WiiMoteOpenGLDemo_LDFLAGS = -L../../.theos/_/usr/lib/ -lbtstack
WiiMoteOpenGLDemo_FRAMEWORKS = Foundation UIKit CoreGraphics  OpenGLES QuartzCore
WiiMoteOpenGLDemo_CODESIGN_FLAGS=-Sent.plist

include $(FW_MAKEDIR)/application.mk
